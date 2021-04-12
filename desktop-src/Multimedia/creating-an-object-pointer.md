---
title: Creazione di un puntatore a un oggetto
description: Creazione di un puntatore a un oggetto
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f57451e2781a94642e61365d3a6c694758f4056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221263"
---
# <a name="creating-an-object-pointer"></a><span data-ttu-id="203a4-103">Creazione di un puntatore a un oggetto</span><span class="sxs-lookup"><span data-stu-id="203a4-103">Creating an Object Pointer</span></span>

<span data-ttu-id="203a4-104">AVIBall usa la struttura seguente come puntatore all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="203a4-104">AVIBall uses the following structure as its object pointer.</span></span> <span data-ttu-id="203a4-105">Il primo membro di questa struttura punta alla tabella delle funzioni virtuali utilizzata da AVIBall per accedere alle relative funzioni.</span><span class="sxs-lookup"><span data-stu-id="203a4-105">The first member of this structure points to the virtual function table that AVIBall uses to access its functions.</span></span> <span data-ttu-id="203a4-106">Le applicazioni possono eseguire il cast di questa struttura al tipo di dati PAVISTREAM.</span><span class="sxs-lookup"><span data-stu-id="203a4-106">Applications can cast this structure to the PAVISTREAM data type.</span></span> <span data-ttu-id="203a4-107">I metodi che utilizzano il tipo di dati PAVISTREAM utilizzano solo il puntatore alla tabella della funzione virtuale.</span><span class="sxs-lookup"><span data-stu-id="203a4-107">Methods that use the PAVISTREAM data type use only the pointer to the virtual function table.</span></span> <span data-ttu-id="203a4-108">I membri che seguono il puntatore alla tabella di funzioni virtuali vengono usati internamente da AVIBall.</span><span class="sxs-lookup"><span data-stu-id="203a4-108">The members following the pointer to the virtual function table are used internally by AVIBall.</span></span>


```C++
typedef struct 
{ 
    IAVIStreamVtbl FAR * lpvtbl; 
 
    // Ball instance data. 
    ULONG     ulRefCount; 
    DWORD     fccType;  // is this audio/video? 
    int        width;    // size, in pixels, of each frame 
    int        height; 
    int        length;   // length, in frames 
    int        size; 
    COLORREF    color;    // ball color 
} AVIBALL, FAR * PAVIBALL; 

```



 

 




