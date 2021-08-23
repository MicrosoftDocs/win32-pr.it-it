---
title: Device-Independent colori
description: Riconoscendo la necessità di misurazioni dei colori standard e indipendenti dal dispositivo, la Commission International de l'Eclairage (International Commission on Illumination) o CIE ha creato uno spazio colore basato su \ 0034;immaginario \ 0034; colori primari.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Windows Sistema colori (WCS), spazi colori indipendenti dal dispositivo
- WCS (Windows Color System), spazi colori indipendenti dal dispositivo
- gestione dei colori delle immagini, spazi colori indipendenti dal dispositivo
- gestione dei colori, spazi colori indipendenti dal dispositivo
- colori, spazi colori indipendenti dal dispositivo
- spazi colori, indipendente dal dispositivo
- spazi colori indipendenti dal dispositivo
- Commission International de l'Eclairage (CIE)
- International Commission on Illumination (CIE)
- CIE (Commission International de l'Eclairage)
- CIE (International Commission on Illumination)
- Spazio colore CIEXYZ
- Spazio colore XYZ
- Spazio colore sRGB
- spazi colori, CIEXYZ
- spazi colori, sRGB
- spazi colori, XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8c350ca4aa4b046d35926cd7568c4fbdfe030b7d7c13b085b9f3837c5dd8418
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028789"
---
# <a name="device-independent-color-spaces"></a>Device-Independent colori

Riconoscendo la necessità di misurazioni dei colori standard e indipendenti dal dispositivo, la Commission International de l'Eclairage (International Commission on Illumination) o CIE ha creato uno spazio colore basato sui colori primari [](c.md) "immaginari". [](p.md) Non è previsto che nessun dispositivo produca colori in questo spazio colori. Viene usato come mezzo per convertire i colori da uno spazio colore a un altro. I colori principali in questo spazio colori sono i colori astratti X, Y e Z.

Lo spazio colori CIEXYZ 1931 è ampiamente usato come base per la conversione dello spazio colore. Con l'aumento di Internet, tuttavia, le considerazioni sulla larghezza di banda hanno reso ingombrante lo spazio colore XYZ. Lo scambio di immagini sulla larghezza di banda limitata di Internet richiede un modello di [colore più compatto.](c.md)

Di conseguenza, Hewlett-Packard e Microsoft hanno proposto l'adozione di uno spazio colori RGB predefinito standard noto come sRGB, in modo da consentire una gestione accurata del colore con un sovraccarico dei dati molto ridotto. Questo standard è stato approvato come standard internazionale formale dal International Electrotechnical Commission (IEC) come IEC 61966-2-1: Multimedia Systems and EquipmentColour Measurement and ManagementPart 2-1: Gestione dei coloriDefault RGB Space. È disponibile direttamente da IEC all'indirizzo <https://www.iec.ch/> . Le informazioni che illustrano i problemi tecnici coinvolti in sRGB sono disponibili su Internet all'indirizzo:

[Uno spazio colori predefinito standard per Internet - sRGB](https://www.w3.org/Graphics/Color/sRGB.html)

Una versione del file della Guida di un white paper che illustra i problemi tecnici coinvolti in sRGB, sRGB.HLP, è disponibile nella cartella Guida di \\ WCS 1.0 Programmer's Reference in Platform SDK.

Formati di file diversi possono usare o aggiungere un flag per specificare che l'immagine si trova nello spazio colore sRGB. Nel formato di bitmap indipendente dal dispositivo (DIB) di Windows, l'impostazione del membro **bV5CSType** della struttura [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) su LCS sRGB specifica che i colori DIB sono nello spazio colore \_ sRGB.

 

 




