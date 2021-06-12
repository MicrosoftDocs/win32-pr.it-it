---
title: Informazioni su DirectShow in Windows Media Format 11 SDK, un'architettura di streaming di dati di alto livello, modulare, estendibile per la piattaforma Windows.
description: Informazioni su DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK,DirectShow
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format),DirectShow
- DirectShow,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a76d7c8971c452f01176be7472e313181eb2831
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011294"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>Informazioni su DirectShow (Windows Media Format 11 SDK)

DirectShow è un'architettura di flusso dei dati di alto livello, modulare, estendibile e di streaming dei dati per la piattaforma Windows. Fornisce i componenti software sottostanti e le API (Application Programming Interface) per un'ampia gamma di applicazioni audio e video digitali attualmente disponibili sul mercato. DirectShow è disponibile come parte di Microsoft DirectX Software Development Kit. Per altre informazioni su DirectShow, vedere Microsoft Platform SDK.

In DirectShow tutti i componenti di streaming dei dati sono denominati *filtri*. Un filtro può rappresentare un dispositivo hardware, un codificatore software o un decodificatore, un renderer audio o video o qualsiasi funzionalità di elaborazione audio-video. Per consentire alle applicazioni basate su DirectShow di leggere e scrivere contenuto di Windows Media Format, incluso il contenuto protetto da Digital Rights Management (DRM), Microsoft fornisce due filtri che incapsulano parti di Windows Media Format SDK. Si tratta del [lettore ASF WM](wm-asf-reader-filter.md) e [di WM ASF Writer.](wm-asf-writer-filter.md) Questi filtri e le interfacce che espongono vengono collettivamente definiti componenti QASF, dopo la DLL in cui sono in pacchetto. La Q è l'acronimo di Quartz, un nome in codice iniziale per DirectShow.

> [!Note]  
> L'uso dei codec Windows Media Audio e Video 9 tramite i componenti QASF DirectShow richiede Microsoft Windows Millennium Edition o versione successiva o DirectX 8.0 o versione successiva.

 

Il diagramma seguente mostra un grafico di filtro DirectShow per la riproduzione Windows Media Video file.

![Grafico di riproduzione di video multimediali di Windows](images/wmv-wmasfreader.png)

Wm [ASF Reader](wm-asf-reader-filter.md) è un componente QASF, i decodificatori sono componenti di Windows Media Format SDK ospitati nel filtro wrapper DMO (un componente QASF) e i renderer sono componenti DirectShow.

 

 




