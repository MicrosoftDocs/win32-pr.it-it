---
description: La funzione StretchBlt ridimensiona una bitmap eseguendo un trasferimento a blocchi di bit da un rettangolo in un contesto di dispositivo di origine in un rettangolo in un contesto di dispositivo di destinazione.
ms.assetid: 34390ff9-8d5f-497e-87aa-a1019d01bba6
title: Ridimensionamento delle bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14975f884906fb95bf07fbf3ab5277b89c5cbfd2612864202eb64eedc5df646b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117699898"
---
# <a name="bitmap-scaling"></a>Ridimensionamento delle bitmap

La [**funzione StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) ridimensiona una bitmap eseguendo un trasferimento a blocchi di bit da un rettangolo in un contesto di dispositivo di origine in un rettangolo in un contesto di dispositivo di destinazione. Tuttavia, a differenza della funzione [**BitBlt,**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) che duplica le dimensioni del rettangolo di origine nel rettangolo di destinazione, **StretchBlt** consente a un'applicazione di specificare le dimensioni dei rettangoli di origine e di destinazione. Quando la bitmap di destinazione è più piccola della bitmap di origine, il sistema combina righe o colonne di dati a colori (o entrambi) nella bitmap prima di eseguire il rendering dell'immagine corrispondente nel dispositivo di visualizzazione. Il sistema combina i dati dei colori in base alla modalità estesa specificata, definita dall'applicazione chiamando la [**funzione SetStretchBltMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) Quando la bitmap di destinazione è più grande della bitmap di origine, il sistema ridimensiona o ingrande di conseguenza ogni pixel nell'immagine risultante.

 

 



