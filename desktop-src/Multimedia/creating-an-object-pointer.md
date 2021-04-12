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
# <a name="creating-an-object-pointer"></a>Creazione di un puntatore a un oggetto

AVIBall usa la struttura seguente come puntatore all'oggetto. Il primo membro di questa struttura punta alla tabella delle funzioni virtuali utilizzata da AVIBall per accedere alle relative funzioni. Le applicazioni possono eseguire il cast di questa struttura al tipo di dati PAVISTREAM. I metodi che utilizzano il tipo di dati PAVISTREAM utilizzano solo il puntatore alla tabella della funzione virtuale. I membri che seguono il puntatore alla tabella di funzioni virtuali vengono usati internamente da AVIBall.


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



 

 




