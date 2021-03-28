---
description: In alcune versioni di Microsoft Windows, le funzioni StretchDIBits e SetDIBitsToDevice consentono di passare le immagini JPEG e PNG come immagine di origine ai dispositivi di stampa.
ms.assetid: a38a807d-44df-40a2-8af7-0ce5e532cba2
title: Estensioni JPEG e PNG per specifiche funzioni e strutture bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625dcde0e673c85dcaef65c2f1aa825121bf871
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528321"
---
# <a name="jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures"></a>Estensioni JPEG e PNG per specifiche funzioni e strutture bitmap

In alcune versioni di Microsoft Windows, le funzioni [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) e [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) consentono di passare le immagini JPEG e PNG come immagine di origine ai dispositivi di stampa. Questa estensione non è pensata come mezzo per fornire la decompressione generale di JPEG e PNG alle applicazioni, ma piuttosto per consentire alle applicazioni di inviare immagini JPEG e PNG compresse direttamente alle stampanti con supporto hardware per immagini JPEG e PNG.

Le strutture [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)), [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) e [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) sono estese per consentire la specifica dei valori di **bicompressione** che indicano che i dati bitmap sono un'immagine JPEG o png. Questi valori di compressione sono validi solo per [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) e [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) quando il parametro *HDC* specifica un dispositivo di stampa. Per supportare lo spooling dei metafile della stampante, l'applicazione non deve basarsi sul valore restituito per determinare se il dispositivo supporta il file JPEG o PNG. L'applicazione deve emettere QUERYESCSUPPORT con l'escape corrispondente prima di chiamare **SetDIBitsToDevice** e **StretchDIBits**. Se l'escape di convalida ha esito negativo, l'applicazione deve quindi eseguire il fallback al proprio supporto JPEG o PNG per decomprimere l'immagine in una bitmap.

 

 
