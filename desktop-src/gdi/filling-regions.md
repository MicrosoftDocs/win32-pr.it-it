---
description: Un'applicazione riempie l'area interna di un'area chiamando la funzione FillRgn e fornendo un handle che identifica un pennello specifico.
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: Aree di riempimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62709869f5f25a6cde11812844efdab6162b1e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049724"
---
# <a name="filling-regions"></a>Aree di riempimento

Un'applicazione riempie l'area interna di un'area chiamando la funzione [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) e fornendo un handle che identifica un pennello specifico. Quando un'applicazione chiama FillRgn, il sistema riempie l'area con il pennello usando la modalità di riempimento corrente per il contesto di dispositivo specificato. Sono disponibili due modalità di riempimento: alternativa e avvolgimento. L'applicazione può impostare la modalità di riempimento per un contesto di dispositivo chiamando la funzione [**SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) . L'applicazione può recuperare la modalità di riempimento corrente per un contesto di dispositivo chiamando la funzione [**GetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) .

Nella figura seguente sono illustrate due aree identiche: una riempita usando la modalità alternativa e l'altra riempita usando la modalità di avvolgimento.

![illustrazione che mostra le stelle a 2 5 punte: una riempita solo nei punti, l'altra riempita completamente](images/csrgn-03.png)

## <a name="alternate-mode"></a>Modalità alternativa

Per determinare i pixel evidenziati dal sistema quando si specifica la modalità alternativa, eseguire il test seguente:

1.  Selezionare un pixel all'interno dell'area interna.
2.  Creare un raggio immaginario, nella direzione x positiva, dal pixel verso l'infinito.
3.  Ogni volta che il raggio interseca una linea di limite, incrementare un valore di conteggio.

Il sistema evidenzia il pixel se il valore del conteggio è un numero dispari.

## <a name="winding-mode"></a>Modalità di avvolgimento

Per determinare i pixel evidenziati dal sistema quando si specifica la modalità di rimozione, eseguire il test seguente:

1.  Determinare la direzione in cui ogni linea di limite viene disegnata.
2.  Selezionare un pixel all'interno dell'area interna.
3.  Creare un raggio immaginario, nella direzione x positiva, dal pixel verso l'infinito.
4.  Ogni volta che il raggio interseca una linea di limite con un componente y positivo, incrementa un valore di conteggio. Ogni volta che il raggio interseca una linea di limite con un componente y negativo, decrementa il valore del conteggio.

Il sistema evidenzia il pixel se il valore del conteggio è diverso da zero.

 

 



