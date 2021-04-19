---
description: Chiama la funzione AttachProperties per eseguire il mapping delle proprietà presenti in un pezzo di dati riconosciuti.
ms.assetid: f1949904-ceb2-4650-847f-01f597ff3620
title: Implementazione di AttachProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9cc032826a8749630c4951b46d456ca807fd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308657"
---
# <a name="implementing-attachproperties"></a><span data-ttu-id="2fa20-103">Implementazione di AttachProperties</span><span class="sxs-lookup"><span data-stu-id="2fa20-103">Implementing AttachProperties</span></span>

<span data-ttu-id="2fa20-104">Network Monitor chiama la funzione [**AttachProperties**](attachproperties.md) per eseguire il mapping delle proprietà presenti in un pezzo di dati riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="2fa20-104">Network Monitor calls the [**AttachProperties**](attachproperties.md) function to map the properties that exist in a piece of recognized data.</span></span> <span data-ttu-id="2fa20-105">La funzione [**AttachProperties**](attachproperties.md) esegue il mapping delle proprietà a una posizione specifica.</span><span class="sxs-lookup"><span data-stu-id="2fa20-105">The [**AttachProperties**](attachproperties.md) function maps the properties to a specific location.</span></span>

<span data-ttu-id="2fa20-106">Network Monitor usa il processo seguente per analizzare i dati in un frame.</span><span class="sxs-lookup"><span data-stu-id="2fa20-106">Network Monitor uses the following process to parse the data in a frame.</span></span>

-   <span data-ttu-id="2fa20-107">In primo luogo, Network Monitor chiama [RecognizeFrame](recognizeframe.md) per riconoscere tutti i protocolli esistenti in un frame.</span><span class="sxs-lookup"><span data-stu-id="2fa20-107">First, Network Monitor calls [RecognizeFrame](recognizeframe.md) to recognize all the protocols that exist in a frame.</span></span>
-   <span data-ttu-id="2fa20-108">Quindi, Network Monitor chiama [**AttachProperties**](attachproperties.md) per ogni parser che riconosce una porzione di dati.</span><span class="sxs-lookup"><span data-stu-id="2fa20-108">Then, Network Monitor calls [**AttachProperties**](attachproperties.md) for each parser that recognizes a piece of data.</span></span>

<span data-ttu-id="2fa20-109">Quando Network Monitor chiama la funzione [AttachProperties](attachproperties.md) per i dati riconosciuti, il parser chiamato deve analizzare i dati, quindi eseguire il mapping di ogni proprietà esistente a una posizione nei dati riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="2fa20-109">When Network Monitor calls the [AttachProperties](attachproperties.md) function for the recognized data, the parser that is called must parse the data, and then map each existing property to a location in the recognized data.</span></span> <span data-ttu-id="2fa20-110">Il parser determina quali proprietà esistono e dove ogni proprietà si trova nei dati.</span><span class="sxs-lookup"><span data-stu-id="2fa20-110">The parser determines which properties exist, and where each property is located in the data.</span></span> <span data-ttu-id="2fa20-111">Nella figura seguente vengono illustrati i dati riconosciuti dal parser.</span><span class="sxs-lookup"><span data-stu-id="2fa20-111">The following figure shows parser-recognized data.</span></span>

![dati riconosciuti dal parser](images/attachproperties1.png)

<span data-ttu-id="2fa20-113">Durante l'implementazione di [**AttachProperties**](attachproperties.md), è necessario chiamare una delle funzioni seguenti per ogni proprietà presente in un frame di dati.</span><span class="sxs-lookup"><span data-stu-id="2fa20-113">During the implementation of [**AttachProperties**](attachproperties.md), you must call one of the following functions for each property that exists in a data frame.</span></span>

-   <span data-ttu-id="2fa20-114">Chiamare la funzione [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) quando si desidera modificare i dati della proprietà in un frame.</span><span class="sxs-lookup"><span data-stu-id="2fa20-114">Call the [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function when you want to modify the property data in a frame.</span></span>
-   <span data-ttu-id="2fa20-115">Chiamare la funzione [**AttachPropertyInstance**](attachpropertyinstance.md) quando non si desidera modificare i dati della proprietà in un frame.</span><span class="sxs-lookup"><span data-stu-id="2fa20-115">Call the [**AttachPropertyInstance**](attachpropertyinstance.md) function when you do not want to modify the property data in a frame.</span></span>

> [!Note]  
> <span data-ttu-id="2fa20-116">Si consiglia di utilizzare i dati esistenti nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="2fa20-116">It is recommended that you use the data as it exists in the capture.</span></span>

 

<span data-ttu-id="2fa20-117">Nella procedura seguente vengono identificati i passaggi necessari per implementare [**AttachProperties**](attachproperties.md).</span><span class="sxs-lookup"><span data-stu-id="2fa20-117">The following procedure identifies the steps necessary to implement [**AttachProperties**](attachproperties.md).</span></span>

<span data-ttu-id="2fa20-118">**Per implementare AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="2fa20-118">**To implement AttachProperties**</span></span>

1.  <span data-ttu-id="2fa20-119">Determinare le proprietà esistenti e il percorso della proprietà nei dati.</span><span class="sxs-lookup"><span data-stu-id="2fa20-119">Determine which properties exist, and the property location in the data.</span></span>
2.  <span data-ttu-id="2fa20-120">Chiamare [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) per ogni proprietà con un valore che si desidera modificare.</span><span class="sxs-lookup"><span data-stu-id="2fa20-120">Call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) for each property with a value that you want to modify.</span></span>
3.  <span data-ttu-id="2fa20-121">Chiamare [**AttachPropertyInstance**](attachpropertyinstance.md) per ogni proprietà con un valore che non si desidera modificare.</span><span class="sxs-lookup"><span data-stu-id="2fa20-121">Call [**AttachPropertyInstance**](attachpropertyinstance.md) for each property with a value that you do not want to modify.</span></span> <span data-ttu-id="2fa20-122">In genere, questa è l'unica funzione che è necessario chiamare.</span><span class="sxs-lookup"><span data-stu-id="2fa20-122">Typically, this is the only function that you need to call.</span></span>

<span data-ttu-id="2fa20-123">Di seguito è riportata un'implementazione di base di [**AttachProperties**](attachproperties.md).</span><span class="sxs-lookup"><span data-stu-id="2fa20-123">The following is a basic implementation of [**AttachProperties**](attachproperties.md).</span></span> <span data-ttu-id="2fa20-124">Tenere presente che l'esempio non include il codice per determinare quali proprietà esistono o il codice per individuare le proprietà.</span><span class="sxs-lookup"><span data-stu-id="2fa20-124">Be aware that the example does not include either the code to determine which properties exist, or the code to locate the properties.</span></span>

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocolAttachProperties( HFRAME   hFrame,
                                         LPBYTE   pMacFrame,
                                         LPBYTE   pBLRPLATEFrame,
                                         DWORD    MacType,
                                         DWORD    BytesLeft,
                                         HPROTOCOL  hPreviousProtocol,
                                         DWORD    nPrevProtocolOffset,
                                         DWORD    InstData)
{
  PBLRPLATEHDR pBLRPLATEHdr = (PBLRPLATEHDR)pBLRPLATEFrame;

  // Attach summary property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SUMMARY].hProperty,
                          (WORD)BytesLeft,
                          (LPBYTE)pBLRPLATEFrame,
                          0,        // No Help file.
                          0,        // Indent level.
                          0);      // Data flag.

  // Attach signature property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SIGNATURE].hProperty,
                          sizeof(DWORD),
                          &(pBLRPLATEHdr->Signature),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.


  // Attach opcode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_OPCODE].hProperty,
                          sizeof(WORD),
                          &(pBLRPLATEHdr->Opcode),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.

  // Attach flags summary.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_SUMMARY].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);       // Data flag.

// Attach flags decode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_FLAGS].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          2,        // Indent level.
                          0);       // Data flag.

  RETURN null;

}
```

 

 



