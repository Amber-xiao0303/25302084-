# 25302084-
import os
import random
import time

#创建Student
class Student:
    def __init__(self, name,gender,class_num,student_id,college):
        #初始化学生信息
        self.name = name
        self.gender = gender
        self.class_num = class_num
        self.student_id = student_id
        self.college = college
    def __str__(self):
        #打印学生信息时，显示不是乱码
        return f"学号：{self.student_id}|姓名：{self.name}|性别：{self.gender}|班级：{self.class_num}|学院：{self.college}"
#创建ExamSystem
def _init_(self,file_path):
    self.file_path = file_path#记录学生名单路径
    self.student_list = []#存储所有学生对象
    self._load_data_from_file()#运行时自动读取文件
def _load_data_from_file(self):
    try:
        with open(self.file_path,"r",encoding="utf-8") as f:
            lines = f.readlines()
            for line in lines[1:]:#跳过表头，逐行读取信息
                line=line.strip()
                items=line.split("\t")#将每行学生变成学生对象
                stu=Student(items[1],items[2],items[3],items[4],items[5])
                self.student_list.append(stu)
    except FileNotFoundError:
        print("文件不存在！")#保证程序在找不到文件时也有显示
