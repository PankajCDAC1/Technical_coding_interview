public class binarysearch
{
        static int Binarysearch(int A[], int element , int size) {
            int low , high;
            low =0;
            high = size-1;
            while(low<=high) {
                int mid = (low + high) / 2;
                if (A[mid] == element) {
                    return mid;
                }
                if (A[mid] < element) {
                    low = mid + 1;
                } else {
                    high = mid - 1;
                }


            }
            return -1;
        }
        public static void main(String args[]){
            int A[] = new int[100];
                    A = new int[]{1, 2, 5, 7, 56, 66, 74, 77, 78, 79};
            int size = A.length;
            int element = 56;
            int searchindex = Binarysearch(A,element,size);
            System.out.print("THE ELEMENT  " + element + " was found at index of  "+ searchindex);
        }




}
