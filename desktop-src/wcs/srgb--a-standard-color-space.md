---
title: sRGB uno spazio colore standard
description: A causa delle considerazioni sulla larghezza di banda di Internet, Hewlett-Packard e Microsoft hanno proposto l'adozione di uno spazio dei colori predefinito standard noto come sRGB (IEC 61966-2-1), in modo da consentire un mapping accurato dei colori con un sovraccarico di dati molto ridotto.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Color System (WCS), spazio colore sRGB
- WCS (sistema di colori Windows), spazio colore sRGB
- Gestione colori immagine, spazio colore sRGB
- gestione dei colori, spazio colore sRGB
- colori, spazio colore sRGB
- spazio colore sRGB
- spazi colore, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3167e44f149982a809826bcb9b64b3ec6e3c24
ms.sourcegitcommit: da13d459791d115df883fa4dd348931d0902c2cc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/30/2021
ms.locfileid: "106320175"
---
# <a name="srgb-a-standard-color-space"></a>sRGB: uno spazio colore standard

A causa delle considerazioni sulla larghezza di banda di Internet, Hewlett-Packard e Microsoft hanno proposto l'adozione di uno [spazio dei colori](c.md) predefinito standard noto come *sRGB* (IEC 61966-2-1), in modo da consentire un mapping accurato dei [colori](c.md) con un sovraccarico di dati molto ridotto.

Una versione del file della Guida di un white paper illustrando i dettagli tecnici di sRGB, sRGB. hlp, è disponibile nella \\ cartella della Guida di informazioni di riferimento per programmatori WCS 1,0.

Formati di file diversi possono usare o aggiungere un flag per specificare che l'immagine è nello spazio dei colori di sRGB. Nel formato DIB (Device-Independent Bitmap) di Windows, l'impostazione del membro **bV5CSType** della struttura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) su **LCS \_ sRGB** specifica che i colori DIB si trovano nello spazio dei colori di sRGB.

WCS 1,0 fornisce supporto nativo per sRGB. Esistono due modi per usare WCS 1,0 per il rendering di un'immagine definita nello spazio dei colori sRGB:

**Per eseguire il rendering di un'immagine all'interno del contesto di dispositivo**

1.  Creare un contesto di dispositivo (DC) nel dispositivo di visualizzazione.
2.  Impostare la gestione dei colori mediante la funzione [**SetICMMode**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode) .
3.  Usare la funzione [**SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) per trasferire la DIB nel controller di dominio. Fino a quando il membro **bV5CSMType** della struttura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) è impostato su **LCS \_ sRGB**, il sistema eseguirà la gestione dei colori appropriata.

**Per eseguire il rendering di un'immagine all'esterno del contesto di dispositivo**

1.  Creare una trasformazione usando [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw). Il membro **lcsCSType** della struttura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) a cui punta il parametro *PLogColorSpace* deve essere impostato su **LCS \_ sRGB**. Il parametro *hDestProfile* indica lo spazio dei colori del dispositivo di visualizzazione.
2.  Usare la trasformazione colore creata per trovare la corrispondenza con il colore dell'immagine prima di visualizzarla nel dispositivo.

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a>Impostazioni predefinite WCS 1,0 per spazio colore di input e profilo di output

Quando non viene specificato alcuno spazio colore di input, per impostazione predefinita WCS 1,0 utilizza lo spazio colore sRGB come spazio colore di input per il [mapping dei colori](c.md).

Quando non viene specificato alcun profilo di output, ma viene specificato un dispositivo predefinito, WCS 1,0 seleziona un profilo di output predefinito. Se al dispositivo predefinito non è associato un profilo, WCS 1,0 utilizza lo spazio di colore sRGB come profilo di output.

La tabella seguente illustra le trasformazioni dei colori risultanti quando non è disponibile un dispositivo predefinito.



|                                 | Profilo di output specificato                              | Profilo di output non specificato                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| Spazio colore di input specificato     | Transform usa i profili specificati.                | Trasforma converte dallo spazio colore di input noto a sRGB. |
| Spazio colore di input non specificato | Trasforma converte da sRGB a profilo di output noto. | Si presuppone la trasformazione da sRGB a sRGB; non viene eseguita alcuna operazione. |



 

## <a name="srgb-and-embedded-profiles"></a>Profili sRGB e incorporati

A partire da ICM versione 2,0, le applicazioni che utilizzano WCS possono incorporare i profili nelle immagini. I profili incorporati consentono alle applicazioni degli utenti di mantenere un aspetto coerente dei colori anche se le immagini vengono trasmesse attraverso Internet.

Le immagini che usano lo spazio dei colori sRGB non necessitano di un profilo colori incorporato. Poiché non dispongono di un profilo incorporato, le immagini basate su sRGB sono più piccole e più facilmente trasferibili tra canali di dati con una larghezza di banda limitata.

Le applicazioni devono impostare il flag **LCS \_ sRGB** nell'intestazione bitmap dell'immagine per indicare che l'immagine usa lo spazio dei colori di sRGB. Per informazioni dettagliate, vedere [strutture di intestazione bitmap di Windows](using-structures-in-wcs-1-0.md) e [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea).

 

 