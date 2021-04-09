---
title: File SeekThumb
description: File SeekThumb
ms.assetid: 757aeb93-ebf0-4659-8cb0-686e54485ac4
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, file SeekThumbd
- Windows Media Player Mobile Skins, file SeekThumb
- interfacce, file SeekThumb
- SeekThumb i file nelle interfacce
- Thumb, file SeekThumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc9f1e9434a614dbc02e48b63508c7c2c04f553d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955604"
---
# <a name="seekthumb-file"></a>File SeekThumb

Il file SeekThumb definisce l'immagine che indica il percorso di riproduzione all'interno dell'elemento multimediale per un TrackBar Seek. È possibile usare un file e definirlo per l'uso da parte di SeekThumb e VolumeThumb. Diversamente dagli altri file grafici, i file Thumb vengono definiti nella sezione trackbars del file di definizione dell'interfaccia.

L'immagine seguente è un file SeekThumb tipico.

![file seekthumb](images/cesdksee.gif)

Questi due file di pulsanti hanno lo stesso aspetto ma hanno dimensioni leggermente diverse. L'immagine a sinistra è la visualizzazione normale visualizzata dall'utente e l'immagine corretta è l'immagine push visualizzata dall'utente quando tocca il pulsante.

> [!Note]  
> I file di SeekThumb Art creati per le interfacce usate in Windows Media Player 10 mobile o versioni successive devono avere le tre immagini seguenti (da sinistra a destra): normale, push e disabilitato.

 

Potrebbe essere necessario rendere trasparente alcune aree delle immagini Thumb. Ciò consentirà di creare immagini Thumb in forme diverse da rettangolare. Qualsiasi area di un'immagine Thumb riempita con il colore specificato dal valore RGB 255, 0, 255 verrà visualizzata trasparente nell'interfaccia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di immagine**](art-files-mobile.md)
</dt> </dl>

 

 




