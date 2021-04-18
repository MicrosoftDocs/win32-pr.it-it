---
title: Supporto per la filigrana
description: Supporto per la filigrana
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- Windows Media Format SDK, supporto per la filigrana
- Windows Media Format SDK, digital watermarking
- ASF (Advanced Systems Format), supporto per la filigrana
- ASF (Advanced Systems Format), supporto per la filigrana
- Formato Advanced Systems (ASF), digital watermarking
- ASF (Advanced Systems Format), digital watermarking
- Windows Media Format SDK, DMO
- ASF (Advanced Systems Format), DMO
- ASF (Advanced Systems Format), DMO
- Windows Media Format SDK, interfaccia IWMWatermarkInfo
- Advanced Systems Format (ASF), interfaccia IWMWatermarkInfo
- ASF (formato avanzato dei sistemi), interfaccia IWMWatermarkInfo
- watermarking, informazioni
- filigrana digitale
- DMO (DirectX Media Object), informazioni
- DMO (oggetto multimediale DirectX), informazioni
- IWMWatermarkInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "106299433"
---
# <a name="watermarking-support"></a>Supporto per la filigrana

Il watermark digitale è un modo per incorporare il copyright o altre informazioni nei dati di un flusso multimediale. Le tecniche per la filigrana variano notevolmente da una soluzione all'altra. La forma più semplice di filigrana è semplicemente l'aggiunta di un'immagine di identificazione a ogni frame di un flusso video. Le stazioni televisive utilizzano spesso questa tecnica per inserire un logo semi-trasparente in un angolo inferiore della trasmissione. Le forme più sofisticate di filigrana digitale sono impercettibili per l'utente che guarda o ascolta il contenuto.

Windows Media Format SDK supporta l'uso di digital watermarking [*DMOS*](wmformat-glossary.md). In pratica, un sistema di filigrana è molto simile a un codec: accetta esempi di supporti, esegue algoritmi sui dati e restituisce gli esempi modificati. Quando si specifica un sistema di filigrana per un flusso, l'oggetto writer include il DMO nell'elaborazione degli esempi di input.

Quando si configura un flusso per la filigrana, è necessario specificare le informazioni di configurazione di filigrana. I valori di configurazione saranno diversi a seconda del valore DMO per la filigrana. L'oggetto DMO usato dovrebbe essere dotato di istruzioni che descrivono i valori di configurazione supportati.

Per informazioni sulle impostazioni usate per specificare un sistema di filigrana, vedere [ **IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)

È possibile programmare l'applicazione per enumerare il DMOs di filigrana installato nel computer client. Per ulteriori informazioni, vedere l'interfaccia [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di scrittura di file**](file-writing-features.md)
</dt> </dl>

 

 




