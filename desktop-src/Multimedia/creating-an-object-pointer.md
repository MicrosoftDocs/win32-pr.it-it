---
title: Creazione di un puntatore a oggetto
description: Creazione di un puntatore a oggetto
ms.assetid: b66a2725-6ba1-4aea-b165-fe3f4da00375
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586ba0b8c9ee261e29f21ed58c84193f4cc89d1399c62d75d82a2c0a49075dcc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144684"
---
# <a name="creating-an-object-pointer"></a>Creazione di un puntatore a oggetto

AVIBall usa la struttura seguente come puntatore a oggetto. Il primo membro di questa struttura punta alla tabella della funzione virtuale utilizzata da AVIBall per accedere alle relative funzioni. Le applicazioni possono eseguire il cast di questa struttura al tipo di dati PAVISTREAM. I metodi che usano il tipo di dati PAVISTREAM usano solo il puntatore alla tabella della funzione virtuale. I membri che segue il puntatore alla tabella della funzione virtuale vengono usati internamente da AVIBall.


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



 

 




