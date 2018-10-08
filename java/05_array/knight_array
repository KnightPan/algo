package com.base.data_structure.array;

/**
 *  数组是一种线性表数据结构，它用一组联系的内存空间，来存储一组具有相同类型的数据
 *  通过寻址来达到随机访问(连续内存空间+相同数据类型)
 *  @author pjf
 *
 */
public class Array {

	private int[] data;
	
	private int capacity;
	
	private int size;
	
	public Array() {
		this(10);
	}
	
	public Array(int capacity) {
		if (capacity < 0) {
			throw new IllegalArgumentException("Illegal Capacity: "+capacity);
		}
		this.capacity = capacity;
		this.data = new int[capacity];
		this.size = 0;
	}
	
	public int length() {
		return size;
	}
	
	public int find(int index) {
		if(index < 0 || index >= size) {
			return -1;
		}
		return data[index];
	}
	
	public boolean delete(int index) {
		if(index < 0 || index >= size) {
			return false;
		}
		for(int i=index+1; i<size; i++) {
			data[i-1] = data[i];
		}
		--size;
		return true;
	}
	
	public boolean insert(int index, int value) {
		if(index < 0 || index >= size) {
			return false;
		}
		if(size == capacity) {
			return false;
		}
		for(int i=size; i>index; i--) {
			data[i] = data[i-1];
		}
		data[index] = value;
		size++;
		return true;
	}
	
	public boolean insertToTail(int value) {
		if(size == capacity) {
			return false;
		}
		data[size++] = value;
		return true;
	}
	
	public void print() {
		for(int i=0; i<size; i++) {
			System.out.print(data[i] + " ");
		}
		System.out.println();
	}
}
