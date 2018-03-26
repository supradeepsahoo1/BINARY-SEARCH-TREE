# BINARY-SEARCH-TREE
#include <iostream>

using namespace std;



struct node{

	int info;

	node *par;

	node *left;

	node *right;

} *root;



class BST{

public:	

 

	BST()

	{

		root=NULL;

	};

	

	int insert(int x)

{

	node *temp= new node;

	temp->info=x;

	temp->par=temp->left=temp->right=NULL;

	node *curr=new node;

	curr= root;

	if(root==NULL)

	{

		root=temp;

	}

	else

	{

	while(1)

	{

	 if(x<curr->info)

	 {

	 	if(curr->left==NULL)

	 	{

	 		temp->par=curr;

	 		curr->left=temp;

	 		break;

	 	}

	 

	 	else

	 	{

	 		curr=curr->left;

	 		

	    }

	   

	}

	else if(x>curr->info)

	{

	if(curr->right==NULL)

	 	{

	 		temp->par=curr;

	 		curr->right=temp;

	 		break;

	 	}

	 

	 	else

	 	{

	 		curr=curr->right;

	 		

	    }

	    	

	}

}

return 0;

}}



int display(node *temp)



{

 if(temp==NULL)

 {

 	cout<<"Tree is empty.\n";

 }

 else

 {

 display(temp->left);

 cout<<temp->info;

 display(temp->right);

 }

 

 return 0;

   

}

   

	

};



int main() 

{



BST b;

b.insert(5);

b.insert(1);

b.insert(3);

b.display(root);



return 0;

}
