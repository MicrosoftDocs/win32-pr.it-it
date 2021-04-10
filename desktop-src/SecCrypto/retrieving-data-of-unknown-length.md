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
# <a name="retrieving-data-of-unknown-length"></a><span data-ttu-id="9ac61-103">Recupero di dati di lunghezza sconosciuta</span><span class="sxs-lookup"><span data-stu-id="9ac61-103">Retrieving Data of Unknown Length</span></span>

<span data-ttu-id="9ac61-104">Molte funzioni restituiscono una quantità potenzialmente elevata di dati a un indirizzo fornito come uno dei parametri dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9ac61-104">Many functions return a potentially large amount of data to an address provided as one of the parameters by the application.</span></span> <span data-ttu-id="9ac61-105">In tutti questi casi, l'operazione viene eseguita in modo analogo, se non identico.</span><span class="sxs-lookup"><span data-stu-id="9ac61-105">In all these cases, the operation is performed in a similar, if not identical, fashion.</span></span> <span data-ttu-id="9ac61-106">Il parametro che punta alla posizione dei dati restituiti utilizzerà la convenzione di notazione in cui PB o PV sono i primi due caratteri del nome del parametro.</span><span class="sxs-lookup"><span data-stu-id="9ac61-106">The parameter that points to the location of the returned data will use the notation convention where pb or pv are the first two characters of the parameter name.</span></span> <span data-ttu-id="9ac61-107">Un altro parametro avrà un PCB come i primi tre caratteri del nome del parametro.</span><span class="sxs-lookup"><span data-stu-id="9ac61-107">Another parameter will have pcb as the first three characters of the parameter name.</span></span> <span data-ttu-id="9ac61-108">Questo parametro rappresenta le dimensioni, in byte, dei dati che verranno restituiti al percorso PB o PV.</span><span class="sxs-lookup"><span data-stu-id="9ac61-108">This parameter represents the size, in bytes, of the data that will be returned to the pb or pv location.</span></span> <span data-ttu-id="9ac61-109">Si consideri, ad esempio, la specifica della funzione seguente:</span><span class="sxs-lookup"><span data-stu-id="9ac61-109">For example, consider the following function specification:</span></span>

``` syntax
#include <windows.h>

BOOL WINAPI SomeFunction(
  PCCRL_CONTEXT pCrlContext,  // in
  DWORD dwPropId,             // in
  BYTE *pbData,               // out
  DWORD *pcbData              // in/out
);
```

<span data-ttu-id="9ac61-110">In questo esempio, *pbData* è un puntatore al percorso in cui verranno restituiti i dati e *pcbData* è la dimensione, in byte, dei dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="9ac61-110">In this example, *pbData* is a pointer to the location where the data will be returned, and *pcbData* is the size, in bytes, of the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="9ac61-111">Il parametro complementare al parametro PCB può talvolta contenere un prefisso leggermente diverso, ad esempio p o PV.</span><span class="sxs-lookup"><span data-stu-id="9ac61-111">The companion parameter to the pcb parameter may sometimes carry a slightly different prefix, such as p or pv.</span></span> <span data-ttu-id="9ac61-112">Inoltre, per i parametri complementari che usano la combinazione di prefissi PWSZ e pcch, il parametro pcch è il conteggio, in caratteri ([*Unicode*](../secgloss/u-gly.md) o [*ASCII*](../secgloss/a-gly.md), come applicabile), dei dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="9ac61-112">Also, for companion parameters using the combination of prefixes pwsz and pcch, the pcch parameter is the count, in characters ([*Unicode*](../secgloss/u-gly.md) or [*ASCII*](../secgloss/a-gly.md), as applicable), of the returned data.</span></span>

 

<span data-ttu-id="9ac61-113">Se il buffer specificato dal parametro *pbData* non è abbastanza grande per contenere i dati restituiti, la funzione imposta l'errore di un \_ numero di \_ codice dati (che può essere visualizzato chiamando la funzione [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) ) e archivia le dimensioni del buffer richieste, in byte, nella variabile a cui punta *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="9ac61-113">If the buffer specified by the *pbData* parameter is not large enough to hold the returned data, the function sets the ERROR\_MORE\_DATA code (which can be seen by calling the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function) and stores the required buffer size, in bytes, in the variable pointed to by *pcbData*.</span></span>

<span data-ttu-id="9ac61-114">Se **null** è l'input per *pbData* e *pcbData* non è **null**, non viene restituito alcun errore e la funzione restituisce la dimensione, in byte, del buffer di memoria necessario nella variabile a cui punta *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="9ac61-114">If **NULL** is input for *pbData* and *pcbData* is not **NULL**, no error is returned, and the function returns the size, in bytes, of the needed memory buffer in the variable pointed to by *pcbData*.</span></span> <span data-ttu-id="9ac61-115">Questo consente a un'applicazione di determinare le dimensioni e il modo migliore per allocare un buffer per i dati restituiti.</span><span class="sxs-lookup"><span data-stu-id="9ac61-115">This lets an application determine the size of, and the best way to allocate, a buffer for the returned data.</span></span>

> [!Note]  
> <span data-ttu-id="9ac61-116">Quando **null** è l'input per *pbData* per determinare le dimensioni necessarie per garantire che i dati restituiti vengano inseriti nel buffer specificato, la seconda chiamata alla funzione che popola il buffer con i dati desiderati non può utilizzare l'intero buffer.</span><span class="sxs-lookup"><span data-stu-id="9ac61-116">When **NULL** is input for *pbData* to determine the size needed to ensure that the returned data fits in the specified buffer, the second call to the function which populates the buffer with the desired data may not use the whole buffer.</span></span> <span data-ttu-id="9ac61-117">Dopo la seconda chiamata, le dimensioni effettive dei dati restituiti sono contenute in *pcbData*.</span><span class="sxs-lookup"><span data-stu-id="9ac61-117">After the second call, the actual size of the data returned is contained in *pcbData*.</span></span> <span data-ttu-id="9ac61-118">Usare questa dimensione durante l'elaborazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="9ac61-118">Use this size when processing the data.</span></span>

 

<span data-ttu-id="9ac61-119">Nell'esempio seguente viene illustrato il modo in cui i parametri di input e output possono essere implementati a questo scopo.</span><span class="sxs-lookup"><span data-stu-id="9ac61-119">The following example shows how input and output parameters might be implemented for this purpose.</span></span>


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



 

 
