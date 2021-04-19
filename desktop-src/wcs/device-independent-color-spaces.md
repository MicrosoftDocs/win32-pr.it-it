---
title: Spazi colori Device-Independent
description: Riconoscendo la necessità di misure di colore standard, indipendenti dal dispositivo, la Commissione International de Eclairage (International Commission on Illumination), o CIE, ha creato uno spazio di colore basato su \ 0034; Imagine \ 0034; colori primari.
ms.assetid: 8597dad3-1eb8-49f9-9843-1f9068a65925
keywords:
- Windows Color System (WCS), spazi dei colori indipendenti dal dispositivo
- WCS (Windows Color System), spazi dei colori indipendenti dal dispositivo
- Gestione colori immagine, spazi colori indipendenti dal dispositivo
- gestione dei colori, spazi dei colori indipendenti dal dispositivo
- colori, spazi dei colori indipendenti dal dispositivo
- spazi dei colori, indipendenti dal dispositivo
- spazi dei colori indipendenti dal dispositivo
- Commission International de Eclairage (CIE)
- International Commission on illuminazione (CIE)
- CIE (Commission International de Eclairage)
- CIE (International Commission on Illumination)
- Spazio colore CIE XYZ
- Area colore XYZ
- spazio colore sRGB
- spazi colore, CIE XYZ
- spazi colore, sRGB
- spazi colore, XYZ
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d044379f8f04467f7be94f09d1eb1fa41816d3e
ms.sourcegitcommit: 38954f8f0d70f44bff4a943784f468ebd7ef691a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/26/2021
ms.locfileid: "106320144"
---
# <a name="device-independent-color-spaces"></a>Spazi colori Device-Independent

Riconoscendo la necessità di misure di colore standard e indipendenti dal dispositivo, la Commissione International de Eclairage (International Commission on Illumination), o CIE, ha creato uno [spazio di colore](c.md) basato su [colori primari](p.md)"immaginari". Non sono previsti dispositivi reali per produrre colori in questo spazio colore. Viene usato come mezzo per convertire i colori da uno spazio colore a un altro. I colori primari in questo spazio colore sono i colori astratti X, Y e Z.

Lo spazio colore CIE XYZ 1931 viene ampiamente usato come base per la conversione dello spazio colore. Con la crescita di Internet, tuttavia, le considerazioni sulla larghezza di banda hanno reso lo spazio dei colori XYZ poco ingombrante. Lo scambio di immagini con la larghezza di banda limitata di Internet richiede un modello di [colore](c.md)più compatto.

Di conseguenza, Hewlett-Packard e Microsoft hanno proposto l'adozione di uno spazio di colore RGB predefinito standard noto come sRGB, in modo da consentire una gestione dei colori accurata con un sovraccarico di dati molto ridotto. Questo standard è stato approvato come standard internazionale formale dal International Electrotechnical Commission (IEC) come IEC 61966-2-1: sistemi multimediali e EquipmentColour Measurement e ManagementPart 2-1: color ManagementDefault RGB Color Space. È disponibile direttamente da IEC all'indirizzo <https://www.iec.ch/> . Informazioni sui problemi tecnici relativi a sRGB sono disponibili su Internet all'indirizzo:

[Uno spazio di colore predefinito standard per Internet-sRGB](https://www.w3.org/Graphics/Color/sRGB.html)

Una versione del file della Guida di un white paper illustrare i problemi tecnici correlati a sRGB, sRGB. HLP, è disponibile nella \\ cartella della guida del riferimento per programmatori WCS 1,0 in Platform SDK.

Formati di file diversi possono usare o aggiungere un flag per specificare che l'immagine è nello spazio dei colori di sRGB. Nel formato DIB (Device-Independent Bitmap) di Windows, l'impostazione del membro **bV5CSType** della struttura [BITMAPV5HEADER](using-structures-in-wcs-1-0.md) su LCS \_ sRGB specifica che i colori DIB si trovano nello spazio dei colori di sRGB.

 

 




