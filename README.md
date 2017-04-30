# -*- coding:utf-8 -*-
def getnum(data,number):
    lendata = len(data)
    if data[lendata/2]>number:
        print 'bigger'
        return getnum(data[:lendata/2],number)
    elif data[lendata/2]<number:
        print 'smaller'
        return lendata/2+getnum(data[lendata/2:],number)
    else:
        return lendata/2

numlist = range(1000000)
print getnum(numlist,56789)
