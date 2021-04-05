---
title: Perché usare DirectShow
description: Perché usare DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, hardware
- Windows Media Format SDK, Windows Driver Model (WDM)
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), hardware
- ASF (formato avanzato dei sistemi), hardware
- ASF (Advanced Systems Format), Windows Driver Model (WDM)
- ASF (Advanced Systems Format), Windows Driver Model (WDM)
- DirectShow, informazioni
- DirectShow, hardware
- DirectShow, Windows Driver Model (WDM)
- Windows Driver Model (WDM)
- WDM (Windows Driver Model)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90fa1de01a7b136b938f9b09cc7fb2b3c229fad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710372"
---
# <a name="why-use-directshow"></a>Perché usare DirectShow?

Esistono due motivi principali per cui un'applicazione può usare direttamente DirectShow anziché Windows Media Format SDK: per praticità dell'architettura di streaming DirectShow e per l'accesso all'hardware.

## <a name="convenience"></a>Praticità

Con l'architettura di streaming DirectShow, sono necessarie solo alcune chiamate al metodo per riprodurre file Windows Media Audio o Windows Media Video. Anche la creazione di file è semplificata. È sufficiente specificare un profilo usando l'interfaccia **IConfigAsfWriter** sul filtro e DirectShow carica automaticamente i componenti necessari per il rendering o la scrittura dei flussi e fornisce i meccanismi per il trasferimento e la sincronizzazione del flusso dei dati multimediali. DirectShow è particolarmente utile per la conversione di contenuto da formati diversi in formato Windows Media. È possibile creare grafici di filtro DirectShow che decodificano una vasta gamma di tipi di file e di compressione e quindi inviano i flussi decodificati al filtro del [writer ASF WM](wm-asf-writer-filter.md) . Per confronto, l'esempio UncompAVItoWMV in questo SDK funziona solo con file AVI non compressi. I flussi di testo e i flussi di dati arbitrari possono anche essere creati e/o sottoposti a rendering tramite DirectShow, ma ciò potrebbe richiedere la creazione di filtri DirectShow personalizzati per l'elaborazione di tali flussi.

## <a name="access-to-hardware"></a>Accesso all'hardware

DirectShow è l'unico modo per il codice dell'applicazione per accedere a dispositivi hardware basati su Windows Driver Model (WDM), ad esempio fotocamere DV 1394, sintonizzatori TV e webcam USB. Se l'applicazione deve acquisire i dati direttamente da un dispositivo hardware basato su WDM e transcodificarli in formato Windows Media e Windows Media Encoder SDK non è adatto alle proprie esigenze, DirectShow è l'unica alternativa. DirectShow può essere usato anche per accedere a dispositivi legacy basati su video per Windows.

 

 




