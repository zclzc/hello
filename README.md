FILE * fd;
  char ch;
 fd=fopen("head.html", "r");
 if(fd==NULL){
     fprintf(cgiOut, "Cannot open file,head.html \n");
     return -1;
   }
   ch = fgetc(fd);

   while(ch != EOF){
     fprintf(cgiOut, "%c", ch);
     ch = fgetc(fd);
   }
 fclose(fd);
   
