---
title: Perché usare DirectShow
description: Perché usare DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows Media Format SDK,DirectShow
- Windows Media Format SDK, hardware
- Windows Media Format SDK,Windows Driver Model (WDM)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), hardware
- ASF (Advanced Systems Format),hardware
- Advanced Systems Format (ASF), Windows Driver Model (WDM)
- ASF (Advanced Systems Format), Windows Driver Model (WDM)
- DirectShow,about
- DirectShow,hardware
- DirectShow,Windows Driver Model (WDM)
- Windows Modello di driver (WDM)
- WDM (modello Windows Driver)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5edce48be7a806011ba59ab5a2c5328840a18399f6f7eea65d649d52c62402
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839421"
---
# <a name="why-use-directshow"></a>Perché usare DirectShow?

Esistono due motivi principali per cui un'applicazione potrebbe usare DirectShow anziché Windows Media Format SDK direttamente: per praticità dell'architettura di streaming DirectShow e per l'accesso all'hardware.

## <a name="convenience"></a>Praticità

Con DirectShow di streaming, sono disponibili solo alcune chiamate al metodo per riprodurre Windows file audio multimediali o Windows file video multimediali. Anche la creazione di file è semplificata. È sufficiente specificare un profilo usando l'interfaccia **IConfigAsfWriter** nel filtro e DirectShow carica automaticamente i componenti necessari per il rendering o la scrittura dei flussi e fornisce i meccanismi per il trasferimento e la sincronizzazione del flusso di dati multimediali. DirectShow è particolarmente utile quando si converte il contenuto da formati diversi in Windows Media Format. È possibile creare DirectShow grafici di filtro che decodificano un'ampia gamma di tipi di file e compressione e quindi alimentare i flussi decodificati nel filtro [WM ASF Writer.](wm-asf-writer-filter.md) L'esempio UncompAVItoWMV in questo SDK funziona invece solo con file AVI non compressi. È anche possibile creare e/o eseguire il rendering di flussi di testo e flussi di dati arbitrari tramite DirectShow, ma potrebbe essere necessario creare filtri DirectShow personalizzati per l'elaborazione di tali flussi.

## <a name="access-to-hardware"></a>Accesso all'hardware

DirectShow è l'unico modo per il codice dell'applicazione per accedere ai dispositivi hardware basati su Windows Driver Model (WDM), ad esempio fotocamere DV 1394, si ottimizzatori TV e webcam USB. Se l'applicazione deve acquisire i dati direttamente da un dispositivo hardware basato su WDM e transcodificarlo in un formato multimediale Windows e Windows Media Encoder SDK non soddisfa le proprie esigenze, DirectShow è l'unica alternativa. DirectShow può essere usato anche per accedere ai dispositivi legacy in base a Video per Windows.

 

 




