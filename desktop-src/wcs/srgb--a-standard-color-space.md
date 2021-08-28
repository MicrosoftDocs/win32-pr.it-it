---
title: sRGB A Spazio colori standard
description: In seguito a considerazioni sulla larghezza di banda Internet, Hewlett-Packard e Microsoft hanno proposto l'adozione di uno spazio colori predefinito standard noto come sRGB (IEC 61966-2-1), in modo da consentire un mapping dei colori accurato con un sovraccarico dei dati molto ridotto.
ms.assetid: b9017702-7dca-4d79-bed0-936f97cb6109
keywords:
- Windows Sistema colori (WCS), spazio colore sRGB
- WCS (Windows Color System),sRGB color space
- gestione colori immagine,spazio colore sRGB
- gestione dei colori, spazio colore sRGB
- colori, spazio colore sRGB
- Spazio colore sRGB
- spazi colori, sRGB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0779ec79868a6ec6d78e447b7ee3473847b8fdc1ffa165897abd2dcbcb7a0793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965920"
---
# <a name="srgb-a-standard-color-space"></a>sRGB: spazio colore standard

In seguito a considerazioni sulla larghezza di banda Internet, Hewlett-Packard e [](c.md) Microsoft hanno proposto l'adozione di uno spazio colori predefinito standard noto come *sRGB* (IEC 61966-2-1), in modo da consentire un [mapping](c.md) dei colori accurato con un sovraccarico dei dati molto ridotto.

Una versione del file della Guida di un white paper che illustra i dettagli tecnici di sRGB, sRGB.hlp, è disponibile nella cartella Guida di \\ WCS 1.0 Programmer's Reference (Guida di riferimento per programmatori di WCS 1.0).

Formati di file diversi possono usare o aggiungere un flag per specificare che l'immagine si trova nello spazio colore sRGB. Nel formato di bitmap indipendente dal dispositivo (DIB) di Windows, l'impostazione del membro **bV5CSType** della struttura [**BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) su **LCS \_ sRGB** specifica che i colori DIB sono nello spazio colore sRGB.

WCS 1.0 offre supporto nativo per sRGB. Esistono due modi per usare WCS 1.0 per il rendering di un'immagine definita nello spazio colore sRGB:

**Per eseguire il rendering di un'immagine all'interno del contesto di dispositivo**

1.  Creare un contesto di dispositivo nel dispositivo di visualizzazione.
2.  Impostare la gestione dei colori [**usando la funzione SetICMMode.**](/windows/desktop/api/Wingdi/nf-wingdi-seticmmode)
3.  Usare la [**funzione SetDIBitsToDevice**](/windows/win32/api/wingdi/nf-wingdi-setdibitstodevice) per trasferire il DIB nel controller di dominio. Se il membro **bV5CSMType** della struttura [**DIBs BITMAPV5HEADER**](using-structures-in-wcs-1-0.md) è impostato su **LCS \_ sRGB,** il sistema eseguirà la gestione dei colori appropriata.

**Per eseguire il rendering di un'immagine all'esterno del contesto di dispositivo**

1.  Creare una trasformazione usando [**CreateColorTransformW.**](/windows/win32/api/icm/nf-icm-createcolortransformw) Il **membro lcsCSType** della struttura [**LOGCOLORSPACE**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) a cui punta il *parametro pLogColorSpace* deve essere impostato su **LCS \_ sRGB.** Il *parametro hDestProfile* indica lo spazio colore del dispositivo di visualizzazione.
2.  Usare la trasformazione colore creata in modo che il colore corrisponda all'immagine prima di visualizzarla nel dispositivo.

## <a name="wcs-10-defaults-for-input-color-space-and-output-profile"></a>Impostazioni predefinite di WCS 1.0 per lo spazio colore di input e il profilo di output

Quando non viene specificato alcuno spazio colore di input, per impostazione predefinita WCS 1.0 usa lo spazio colore sRGB come spazio colore di input per il [mapping dei colori](c.md).

Quando non viene specificato alcun profilo di output, ma viene specificato un dispositivo predefinito, WCS 1.0 seleziona un profilo di output predefinito. Se al dispositivo predefinito non è associato un profilo, WCS 1.0 usa lo spazio colore sRGB come profilo di output.

La tabella seguente illustra le trasformazioni di colore risultanti quando non è disponibile un dispositivo predefinito.



|  &nbsp;                               | Profilo di output specificato                              | Profilo di output non specificato                             |
|---------------------------------|-------------------------------------------------------|----------------------------------------------------------|
| Spazio colore di input specificato     | Transform usa i profili specificati.                | Transform converte lo spazio colore di input noto in sRGB. |
| Spazio colore di input non specificato | Transform converte da sRGB a profilo di output noto. | Si presuppone la trasformazione da sRGB a sRGB. non viene eseguita alcuna operazione. |



 

## <a name="srgb-and-embedded-profiles"></a>sRGB e profili incorporati

A partire ICM versione 2.0, le applicazioni che utilizzano WCS possono incorporare i profili nelle immagini. I profili incorporati consentono alle applicazioni degli utenti di mantenere un aspetto di colore coerente anche se le immagini vengono trasmesse su Internet.

Le immagini che usano lo spazio colore sRGB non necessitano di un profilo colori incorporato. Poiché non hanno un profilo incorporato, le immagini basate su sRGB sono più piccole e più facilmente trasferibili tra i canali di dati con larghezza di banda limitata.

Le applicazioni devono impostare il flag **LCS \_ sRGB** nell'intestazione bitmap dell'immagine per indicare che l'immagine usa lo spazio colore sRGB. Per informazioni dettagliate, [vedere Windows di intestazione bitmap](using-structures-in-wcs-1-0.md) e [**LOGCOLORSPACE.**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea)

 

 