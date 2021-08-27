---
description: In alcune versioni di Microsoft Windows le funzioni StretchDIBits e SetDIBitsToDevice consentono di passare immagini JPEG e PNG come immagine di origine ai dispositivi della stampante.
ms.assetid: a38a807d-44df-40a2-8af7-0ce5e532cba2
title: Estensioni JPEG e PNG per strutture e funzioni bitmap specifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd7dcd2713b737d86f90ab0d49fdf4eed1216f807a4debdffa1963e43a42a9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115291"
---
# <a name="jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures"></a>Estensioni JPEG e PNG per strutture e funzioni bitmap specifiche

In alcune versioni di Microsoft Windows le funzioni [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) e [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) consentono di passare immagini JPEG e PNG come immagine di origine ai dispositivi della stampante. Questa estensione non è concepita come mezzo per fornire la decompressione JPEG e PNG generale alle applicazioni, ma piuttosto per consentire alle applicazioni di inviare immagini compresse JPEG e PNG direttamente alle stampanti con supporto hardware per immagini JPEG e PNG.

Le [**strutture BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) e [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) vengono estese per consentire la specifica di **valori biCompression** che indicano che i dati bitmap sono un'immagine JPEG o PNG. Questi valori di compressione sono validi solo per [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) e [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) quando il *parametro hdc* specifica una periferica di stampa. Per supportare lo spooling metafile della stampante, l'applicazione non deve basarsi sul valore restituito per determinare se il dispositivo supporta il file JPEG o PNG. L'applicazione deve eseguire QUERYESCSUPPORT con l'escape corrispondente prima di **chiamare SetDIBitsToDevice** **e StretchDIBits**. Se l'escape di convalida ha esito negativo, l'applicazione deve eseguire il fall back sul proprio supporto JPEG o PNG per decomprimere l'immagine in una bitmap.

 

 
