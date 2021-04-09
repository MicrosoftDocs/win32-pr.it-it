---
title: Informazioni su DirectShow (Windows Media Format 11 SDK)
description: Informazioni su DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd77507643edb220bc71a029779c88fe56760eae
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104047745"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>Informazioni su DirectShow (Windows Media Format 11 SDK)

DirectShow è un'architettura di streaming di dati di alto livello, modulare, estendibile e modulare per la piattaforma Windows. Fornisce i componenti software e le API (Application Programming Interface) sottostanti per un'ampia gamma di applicazioni audio e video digitali sul mercato. DirectShow è disponibile come parte di Microsoft DirectX Software Development Kit. Per ulteriori informazioni su DirectShow, vedere Microsoft Platform SDK.

In DirectShow tutti i componenti del flusso di dati sono denominati *filtri*. Un filtro può rappresentare un dispositivo hardware, un codificatore software o un decodificatore, un renderer audio o video o qualsiasi funzionalità di elaborazione video audio. Per consentire alle applicazioni basate su DirectShow di leggere e scrivere contenuto in formato Windows Media, incluso il contenuto protetto da Digital Rights Management (DRM), Microsoft offre due filtri che incapsulano parti di Windows Media Format SDK. Si tratta del [lettore WM ASF](wm-asf-reader-filter.md) e del [writer ASF WM](wm-asf-writer-filter.md). Questi filtri e le interfacce che espongono sono collettivamente denominati componenti QASF, dopo la DLL in cui sono inclusi nel pacchetto. (Q sta per quarzo, un nome di codice iniziale per DirectShow).

> [!Note]  
> L'uso dei codec della serie Windows Media Audio e video 9 con i componenti DirectShow QASF richiede Microsoft Windows Millennium Edition o versione successiva o DirectX 8,0 o versione successiva.

 

Il diagramma seguente mostra un grafico filtro DirectShow per la riproduzione di file di Windows Media Video.

![grafico di riproduzione video di Windows Media](images/wmv-wmasfreader.png)

Il [lettore di WM ASF](wm-asf-reader-filter.md) è un componente qasf, i decodificatori sono componenti Windows Media Format SDK ospitati nel filtro del wrapper DMO (un componente QASF) e i renderer sono componenti DirectShow.

 

 




