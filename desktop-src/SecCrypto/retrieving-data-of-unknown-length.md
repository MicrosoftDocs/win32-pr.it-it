---
description: Molte funzioni restituiscono una quantità potenzialmente elevata di dati a un indirizzo fornito come uno dei parametri dall'applicazione.
ms.assetid: ef99edef-39b2-4d78-9c01-13720215d47f
title: Recupero di dati di lunghezza sconosciuta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd30620018f3c4871bd27299c3dd21ae42936c51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880506"
---
# <a name="retrieving-data-of-unknown-length"></a>Recupero di dati di lunghezza sconosciuta

Molte funzioni restituiscono una quantità potenzialmente elevata di dati a un indirizzo fornito come uno dei parametri dall'applicazione. In tutti questi casi, l'operazione viene eseguita in modo analogo, se non identico. Il parametro che punta alla posizione dei dati restituiti utilizzerà la convenzione di notazione in cui PB o PV sono i primi due caratteri del nome del parametro. Un altro parametro avrà un PCB come i primi tre caratteri del nome del parametro. Questo parametro rappresenta le dimensioni, in byte, dei dati che verranno restituiti al percorso PB o PV. Si consideri, ad esempio, la specifica della funzione seguente:

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

In questo esempio, *pbData* è un puntatore al percorso in cui verranno restituiti i dati e *pcbData* è la dimensione, in byte, dei dati restituiti.

> [!Note]  
> Il parametro complementare al parametro PCB può talvolta contenere un prefisso leggermente diverso, ad esempio p o PV. Inoltre, per i parametri complementari che usano la combinazione di prefissi PWSZ e pcch, il parametro pcch è il conteggio, in caratteri ([*Unicode*](../secgloss/u-gly.md) o [*ASCII*](../secgloss/a-gly.md), come applicabile), dei dati restituiti.

 

Se il buffer specificato dal parametro *pbData* non è abbastanza grande per contenere i dati restituiti, la funzione imposta l'errore di un \_ numero di \_ codice dati (che può essere visualizzato chiamando la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ) e archivia le dimensioni del buffer richieste, in byte, nella variabile a cui punta *pcbData*.

Se **null** è l'input per *pbData* e *pcbData* non è **null**, non viene restituito alcun errore e la funzione restituisce la dimensione, in byte, del buffer di memoria necessario nella variabile a cui punta *pcbData*. Questo consente a un'applicazione di determinare le dimensioni e il modo migliore per allocare un buffer per i dati restituiti.

> [!Note]  
> Quando **null** è l'input per *pbData* per determinare le dimensioni necessarie per garantire che i dati restituiti vengano inseriti nel buffer specificato, la seconda chiamata alla funzione che popola il buffer con i dati desiderati non può utilizzare l'intero buffer. Dopo la seconda chiamata, le dimensioni effettive dei dati restituiti sono contenute in *pcbData*. Usare questa dimensione durante l'elaborazione dei dati.

 

Nell'esempio seguente viene illustrato il modo in cui i parametri di input e output possono essere implementati a questo scopo.


```C++
//-------------------------------------------------------------------
// Copyright (C) Microsoft.  All rights reserved.
#include <stdio.h>
#include <windows.h>
#include <Wincrypt.h>
#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void MyHandleError(char *s);

void main()
{

// Set up SomeFunction variables.
PCCRL_CONTEXT pCrlContext; // Initialized elsewhere.
DWORD dwPropId;            // Initialized elsewhere.
DWORD cbData;
BYTE  *pbData;

// Call SomeFunction to set cbData, the size of 
// the buffer needed for pbData.
if(SomeFunction(
     pCrlContext, 
     dwPropId, 
     NULL, 
     &cbData))
{
       printf("The function succeeded.\n");
}
else
{

// The function call failed. Handle the error.
       MyHandleError("Function call failed.");
}

// The call succeeded; the size for the needed buffer, in bytes, 
// now resides in cbData.

// Malloc memory for the size of the message.
if(pbData = (BYTE*)malloc(cbData))
{
   printf("Memory has been allocated.\n");
}
else
{

   // The allocation failed. Write an error message and exit.
   MyHandleError("Malloc operation failed. ");
}

// The space for the buffer has been allocated.
// Call SomeFunction to fill the buffer with the data.
if(SomeFunction(
      pCrlContext, 
      dwPropId, 
      pbData, 
      &cbData))
{
       printf("The function succeeded.\n");
}
else
{

   // The second function call failed. Handle the error.
   MyHandleError("The second call to the function failed.");
}

// The function succeeded; the data is now in the buffer
// pointed to by pbData. Note that cbData is
// updated with the actual size of the data returned. Use this size 
// to process bytes of pbData.

// When you have finished using the allocated memory, free it.
free(pbData);

} // End of main

//  This example uses the function MyHandleError, a simple error
//  handling function, to print an error message to the 
//  standard error (stderr) file and exit the program. 
//  For most applications, replace this function with one 
//  that does more extensive error reporting.
void MyHandleError(char *s)
{
    fprintf(stderr,"An error occurred in running the program.\n");
    fprintf(stderr,"%s\n",s);
    fprintf(stderr,"Error number %x.\n",GetLastError());
    fprintf(stderr,"Program terminating.\n");
    exit(1);
}
```



 

 
