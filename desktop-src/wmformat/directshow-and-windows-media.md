---
title: DirectShow e Windows Media
description: DirectShow e Windows Media
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714215"
---
# <a name="directshow-and-windows-media"></a>DirectShow e Windows Media

In alternativa all'uso esclusivo di Windows Media Format SDK, le applicazioni possono anche leggere e scrivere contenuto basato su Windows Media usando l'architettura di streaming Microsoft® DirectShow®, come descritto nelle sezioni seguenti.



| Sezione                                                                                   | Descrizione                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni su DirectShow](about-directshow.md)                                                  | Descrive DirectShow in termini generali e indica dove ottenere ulteriori informazioni su di esso.                                                     |
| [Perché usare DirectShow?](why-use-directshow.md)                                             | Viene descritto il modo in cui DirectShow semplifica determinate attività nella creazione e nella riproduzione di contenuto basato su Windows Media.                              |
| [Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)                    | Viene descritto come riprodurre file ASF con DirectShow.                                                                                           |
| [Creazione di file ASF in DirectShow](creating-asf-files-in-directshow.md)                  | Viene descritto come creare file ASF usando DirectShow.                                                                                         |
| [\_Notifica degli eventi dello stato WMT in DirectShow](wmt-status-notification-in-directshow.md) | Vengono descritti gli eventi di **\_ stato WMT** gestiti dai filtri ASF Reader e writer ASF e il modo in cui le applicazioni possono ricevere questi eventi. |
| [Supporto DRM in DirectShow](drm-support-in-directshow.md)                                | Viene descritto come leggere e scrivere file protetti da DRM tramite DirectShow.                                                                     |
| [Informazioni di riferimento su DirectShow QASF](directshow-qasf-reference.md)                                | Contiene la documentazione di riferimento per i componenti DirectShow che supportano Windows Media.                                              |



 

Tre applicazioni di esempio nell'SDK illustrano l'uso di DirectShow: DSCopy, DSPlay e DSSeekFM. Per altre informazioni, vedere [applicazioni di esempio](sample-applications.md).

> [!Note]  
> Per le applicazioni che usano i componenti di QASF inclusi in questo SDK è necessario che sia installato Microsoft DirectX® 8,1 o versione successiva del Runtime SDK nei sistemi Windows® 2000, Windows 98 e Windows 95. In particolare, questo runtime è richiesto dal filtro wrapper DMO che ospita i codec Windows Media in un grafico filtro DirectShow.

 

 

 




