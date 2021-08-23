---
title: DirectShow e Windows multimediali
description: DirectShow e Windows multimediali
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Media Format SDK,DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b975347d26414dda0c1f54c0b71ac852541bd58c314e3724725c3768ddfc7bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027909"
---
# <a name="directshow-and-windows-media"></a>DirectShow e Windows multimediali

In alternativa all'uso esclusivo di Windows Media Format SDK, le applicazioni possono anche leggere e scrivere contenuti basati su contenuti multimediali di Windows usando l'architettura di streaming Microsoft® DirectShow®, come descritto nelle sezioni seguenti.



| Sezione                                                                                   | Descrizione                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni DirectShow](about-directshow.md)                                                  | Descrive DirectShow in termini generali e indica dove ottenere altre informazioni.                                                     |
| [Perché usare DirectShow?](why-use-directshow.md)                                             | Descrive come DirectShow alcune attività nella creazione e nella riproduzione di Windows contenuti basati su file multimediali.                              |
| [Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)                    | Viene descritto come riprodurre file ASF usando DirectShow.                                                                                           |
| [Creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md)                  | Viene descritto come creare file ASF usando DirectShow.                                                                                         |
| [WmT \_ STATUS Event Notification in DirectShow](wmt-status-notification-in-directshow.md) | Descrive gli eventi **WMT \_ STATUS** gestiti dai filtri LETTORE ASF e ASF Writer e come le applicazioni possono ricevere tali eventi. |
| [Supporto DRM in DirectShow](drm-support-in-directshow.md)                                | Viene descritto come leggere e scrivere file protetti da DRM tramite DirectShow.                                                                     |
| [DirectShow Informazioni di riferimento su QASF](directshow-qasf-reference.md)                                | Contiene la documentazione di riferimento per i componenti DirectShow che supportano Windows multimediali.                                              |



 

Tre applicazioni di esempio nell'SDK illustrano l'uso di DirectShow: DSCopy, DSPlay e DSSeekFM. Per altre informazioni, vedere [Applicazioni di esempio.](sample-applications.md)

> [!Note]  
> Le applicazioni che usano i componenti QASF inclusi in questo SDK richiedono l'installazione del runtime di Microsoft DirectX® 8.1 o versione successiva SDK nei sistemi Windows® 2000, Windows 98 e Windows 95. In particolare, questo runtime è richiesto dal filtro wrapper DMO che ospita i codec Windows media in un grafico DirectShow filtro.

 

 

 




