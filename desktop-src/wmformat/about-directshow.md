---
title: Informazioni sui DirectShow in Windows Media Format 11 SDK, un'architettura di alto livello, modulare, estendibile, di streaming dei dati per la Windows.
description: Informazioni DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK,DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow,about
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aeb5dc9ebc613f7820a8ba4c4f5877ce9ac27068f1c4e873f9e8b00ec2f3b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840412"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>Informazioni DirectShow (Windows Media Format 11 SDK)

DirectShow è un'architettura di alto livello, modulare, estendibile e di streaming dei dati per la Windows piattaforma. Fornisce i componenti software sottostanti e le API (Application Programming Interface) per un'ampia gamma di applicazioni audio e video digitali attualmente sul mercato. DirectShow è disponibile come parte di Microsoft DirectX Software Development Kit. Per altre informazioni sui DirectShow, vedere Microsoft Platform SDK.

In DirectShow, tutti i componenti di streaming dei dati sono denominati *filtri*. Un filtro può rappresentare un dispositivo hardware, un codificatore software o un decodificatore, un renderer audio o video o qualsiasi funzionalità di elaborazione audio-video. Per consentire alle applicazioni basate su DirectShow di leggere e scrivere contenuto Windows Media Format, incluso il contenuto protetto da Digital Rights Management (DRM), Microsoft fornisce due filtri che incapsulano parti di Windows Media Format SDK. Si tratta del [lettore ASF WM](wm-asf-reader-filter.md) e [di WM ASF Writer.](wm-asf-writer-filter.md) Questi filtri e le interfacce che espongono vengono definiti collettivamente come componenti QASF, dopo la DLL in cui sono in pacchetto. La Q è l'acronimo di Quartz, un nome in codice iniziale per DirectShow.

> [!Note]  
> L'uso dei codec Windows Media Audio e Video Serie 9 tramite i componenti QASF di DirectShow richiede Microsoft Windows Millennium Edition o versioni successive o DirectX 8.0 o versione successiva.

 

Il diagramma seguente mostra un grafico DirectShow filtro per la riproduzione Windows file video multimediali.

![Grafico di riproduzione di video windows media](images/wmv-wmasfreader.png)

Wm [ASF Reader](wm-asf-reader-filter.md) è un componente QASF, i decodificatori sono componenti di Windows Media Format SDK ospitati nel filtro wrapper DMO (un componente QASF) e i renderer sono DirectShow componenti.

 

 




