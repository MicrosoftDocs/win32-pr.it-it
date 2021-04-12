---
description: La funzione StretchBlt ridimensiona una bitmap eseguendo un trasferimento a blocchi di bit da un rettangolo in un contesto di dispositivo di origine in un rettangolo in un contesto di dispositivo di destinazione.
ms.assetid: 34390ff9-8d5f-497e-87aa-a1019d01bba6
title: Ridimensionamento bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4011b06e6a7269be29e1834e90928c4f531b1023
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130847"
---
# <a name="bitmap-scaling"></a>Ridimensionamento bitmap

La funzione [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt) ridimensiona una bitmap eseguendo un trasferimento a blocchi di bit da un rettangolo in un contesto di dispositivo di origine in un rettangolo in un contesto di dispositivo di destinazione. Tuttavia, a differenza della funzione [**BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) , che duplica le dimensioni del rettangolo di origine nel rettangolo di destinazione, **StretchBlt** consente a un'applicazione di specificare le dimensioni dei rettangoli di origine e di destinazione. Quando la bitmap di destinazione è inferiore alla bitmap di origine, il sistema combina righe o colonne di dati di colore (o entrambi) nella bitmap prima di eseguire il rendering dell'immagine corrispondente sul dispositivo di visualizzazione. Il sistema combina i dati dei colori in base alla modalità di estensione specificata, definita dall'applicazione chiamando la funzione [**SetStretchBltMode**](/windows/desktop/api/Wingdi/nf-wingdi-setstretchbltmode) . Quando la bitmap di destinazione è più grande della bitmap di origine, il sistema ridimensiona o esalta ogni pixel nell'immagine risultante di conseguenza.

 

 



