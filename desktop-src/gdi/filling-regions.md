---
description: Un'applicazione riempie l'interno di un'area chiamando la funzione FillRgn e fornendo un handle che identifica un pennello specifico.
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: Riempimento di aree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d909643155b027f72b4235db366e640d7e53dacd4825b85090f9958aec1c94c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015401"
---
# <a name="filling-regions"></a>Riempimento di aree

Un'applicazione riempie l'interno di un'area chiamando la [**funzione FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) e fornendo un handle che identifica un pennello specifico. Quando un'applicazione chiama FillRgn, il sistema riempie l'area con il pennello usando la modalità di riempimento corrente per il contesto di dispositivo specificato. Esistono due modalità di riempimento: alternativa e tortuosa. L'applicazione può impostare la modalità di riempimento per un contesto di dispositivo chiamando la [**funzione SetPolyFillMode.**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) L'applicazione può recuperare la modalità di riempimento corrente per un contesto di dispositivo chiamando la [**funzione GetPolyFillMode.**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode)

La figura seguente mostra due aree identiche: una riempita in modalità alternativa e l'altra riempita con la modalità di avvolgimento.

![illustrazione che mostra due stelle a cinque punte: una riempita solo nei punti, l'altra riempita completamente](images/csrgn-03.png)

## <a name="alternate-mode"></a>Modalità alternativa

Per determinare i pixel evidenziati dal sistema quando viene specificata la modalità alternativa, eseguire il test seguente:

1.  Selezionare un pixel all'interno dell'area.
2.  Disegna un raggio immaginario, nella direzione x positiva, da quel pixel verso l'infinito.
3.  Ogni volta che il raggio interseca una linea limite, incrementare un valore di conteggio.

Il sistema evidenzia il pixel se il valore del conteggio è un numero dispari.

## <a name="winding-mode"></a>Modalità di avvolgimento

Per determinare i pixel evidenziati dal sistema quando viene specificata la modalità di avvolgimento, eseguire il test seguente:

1.  Determinare la direzione in cui viene disegnata ogni linea limite.
2.  Selezionare un pixel all'interno dell'area.
3.  Disegna un raggio immaginario, nella direzione x positiva, dal pixel verso l'infinito.
4.  Ogni volta che il raggio interseca una linea limite con un componente y positivo, incrementare un valore di conteggio. Ogni volta che il raggio interseca una linea limite con un componente y negativo, decrementa il valore di conteggio.

Il sistema evidenzia il pixel se il valore del conteggio è diverso da zero.

 

 



