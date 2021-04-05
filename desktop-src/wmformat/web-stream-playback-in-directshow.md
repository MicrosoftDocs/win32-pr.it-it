---
title: Riproduzione del flusso Web in DirectShow
description: Riproduzione del flusso Web in DirectShow
ms.assetid: cc307c24-2bd2-43de-ba81-1cf5b05524b2
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, riproduzione del flusso Web
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (Advanced Systems Format), riproduzione del flusso Web
- ASF (formato avanzato dei sistemi), riproduzione del flusso Web
- DirectShow, riproduzione del flusso Web
- Flussi Web, DirectShow
- Flussi Web, riproduzione in DirectShow
- flussi, riproduzione del flusso Web in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a696e8184554195cf6e9c841b2fb59c4281e377a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955291"
---
# <a name="web-stream-playback-in-directshow"></a>Riproduzione del flusso Web in DirectShow

Microsoft DirectShow supporta i flussi Web (vedere [flussi Web](web-streams.md) per altre informazioni) negli scenari di riproduzione dei file tramite il filtro di [lettura ASF WM](wm-asf-reader-filter.md) , ma è necessario scrivere un filtro DirectShow personalizzato per acquisire e salvare in modo permanente il flusso.

> [!Note]  
> Per riprodurre i flussi Web nel contenuto trasmesso da un server che esegue Servizi Windows Media, utilizzare il controllo ActiveX® della serie Windows Media Player 9 incorporato in una pagina Web.

 

Quando si specifica un file contenente flussi di tipo \_ filetransfer WMMEDIATYPE, il lettore WM ASF creerà un pin di output per tale file. Il blocco di formato sarà una struttura del [**\_ \_ formato webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) . Se non è disponibile alcun filtro downstream in grado di gestire tale tipo di supporto, il pin rimarrà non connesso, ma il file continuerà a riprodurre i flussi audio e/o video.

È importante comprendere che ogni esempio di supporto in un flusso Web contiene una struttura [**di \_ intestazione di \_ esempio \_ webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , che ha una lunghezza variabile a seconda della lunghezza del membro **wszURL** . Il puntatore ai dati di esempio punta inizialmente a questa struttura ed è necessario far avanzare il puntatore oltre la struttura per accedere ai dati effettivi nel flusso. Il filtro del gestore del flusso Web deve essere basato sulla classe **CBaseRenderer** . Nel metodo **DoRenderSample** il filtro dovrà analizzare la struttura per ottenere informazioni sul flusso Web e quindi eseguire l'azione appropriata. In genere, questa operazione comporterà il salvataggio del file su disco e la chiamata a **CommitUrlCacheEntry** e **CreateUrlCacheEntry** per inserire i file nella cache di Internet Explorer. Il filtro deve gestire i file multipart, ovvero i file più grandi di un campione, e deve anche gestire i comandi di rendering, che sono specificati dal membro **WMT \_ webstream \_ Sample \_ header. wSampleType** . Il filtro Invia un **\_ \_ evento OLE EC** all'applicazione, insieme al testo dell' **intestazione di \_ esempio webstream WMT \_ . stringa \_ wszURL** che contiene il nome del file di cui eseguire il rendering. L'applicazione fa quindi in modo che nel browser venga visualizzata la pagina specificata. Se il flusso Web è stato creato correttamente, il file deve essere già presente nella cache.

Per ulteriori informazioni sugli **\_ \_ eventi OLE** **CBaseRenderer**, **DoRenderSample** e EC, vedere la documentazione relativa a DirectShow SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Flussi Web**](web-streams.md)
</dt> </dl>

 

 




