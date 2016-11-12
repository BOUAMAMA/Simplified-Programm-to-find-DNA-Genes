# Simplified-Programm-to-find-DNA-Genes
Program to find Genes in a DNA String
import edu.duke.*;
import java.io.*;
public class Part1 {
  
  public String findSimpleGene(String dna){
        
       int StartIndex= dna.indexOf("ATG");
       if (StartIndex == -1) {
           return "";
        }
       int StopIndex= dna.indexOf("TAA", StartIndex+3);
       if (StopIndex== -1) {
           return "";
        }
       String result = dna.substring(StartIndex, StopIndex+3);
       if(result.length() %3 ==0) {
       return result;
    }
    return result;
}
  public void testSimpleGene() {
      String dna="AGTAAATTTGGGGGTAA";
      System.out.println("DNA is" + dna);
      String result = findSimpleGene(dna);
      System.out.println("Gene is" + result);
    
   
   dna="ATGATTTGGATAGTGT";
      System.out.println("DNA is" + dna);
      result = findSimpleGene(dna);
      System.out.println("Gene is" + result);
  
     dna="ATGGTTAAATGTTAA";
      System.out.println("DNA is" + dna);
      result = findSimpleGene(dna);
      System.out.println("Gene is" + result);
   
     dna="ATGGTTAAATGTAA";
      System.out.println("DNA is" + dna);
      result = findSimpleGene(dna);
      System.out.println("gene is" + result);
    }
}
