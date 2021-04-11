---
description: Riproduzione del flusso Web ASF in DirectShow
ms.assetid: c7818c62-24af-4eac-84b8-f76be4ca6c09
title: Riproduzione del flusso Web ASF in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d14a83d2baf9c11aa824f5d6358f62790c16b30
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341936"
---
# <a name="asf-web-stream-playback-in-directshow"></a>Riproduzione del flusso Web ASF in DirectShow

Microsoft DirectShow supporta i flussi Web negli scenari di riproduzione dei file tramite il filtro [WM ASF Reader](wm-asf-reader-filter.md) , ma è necessario scrivere un filtro DirectShow personalizzato per acquisire e salvare in modo permanente il flusso.

> [!Note]  
> Per riprodurre i flussi Web nel contenuto trasmesso da un server che esegue Servizi Windows Media, utilizzare il controllo ActiveX® della serie Windows Media Player 9 incorporato in una pagina Web.

 

Quando si specifica un file contenente flussi di tipo \_ filetransfer WMMEDIATYPE, il lettore WM ASF creerà un pin di output per tale file. Il blocco di formato sarà una struttura del [**\_ \_ formato webstream WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format) . Questa struttura è documentata nella documentazione di Windows Media Format SDK. Se non è disponibile alcun filtro downstream in grado di gestire tale tipo di supporto, il pin rimarrà non connesso, ma il file continuerà a riprodurre i flussi audio e/o video.

Ogni esempio di supporto in un flusso Web contiene una struttura di [**\_ \_ \_ intestazione di esempio webstream WMT**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) , documentata nella documentazione di Windows Media Format SDK. La struttura ha una lunghezza variabile a seconda della lunghezza del membro **wszURL** . Il puntatore ai dati di esempio punta inizialmente a questa struttura ed è necessario far avanzare il puntatore oltre la struttura per accedere ai dati effettivi nel flusso.

Il filtro del gestore del flusso Web deve essere basato sulla classe [**CBaseRenderer**](cbaserenderer.md) . Nel metodo [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md) , il filtro dovrà analizzare la struttura per ottenere informazioni sul flusso Web e quindi eseguire l'azione appropriata. In genere, questa operazione comporterà il salvataggio del file su disco e quindi la chiamata delle funzioni [**CreateUrlCacheEntry**](/windows/desktop/api/wininet/nf-wininet-createurlcacheentrya) e [**CommitUrlCacheEntryW**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw) o [**CommitUrlCacheEntryA**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya) per inserire i file nella cache di Internet Explorer. Il filtro deve gestire i file multipart, ovvero i file più grandi di un campione, e deve anche gestire i comandi di rendering, che sono specificati dal membro **WMT \_ webstream \_ Sample \_ header. wSampleType** . Il filtro Invia un [**evento \_ \_ evento OLE EC**](ec-ole-event.md) all'applicazione, insieme al testo dell' **intestazione di \_ esempio webstream WMT \_ . stringa \_ wszURL** che contiene il nome del file di cui eseguire il rendering. L'applicazione fa quindi in modo che nel browser venga visualizzata la pagina specificata. Se il flusso Web è stato creato correttamente, il file deve essere già presente nella cache.

Per altre informazioni sul \_ formato WEBSTREAM WMT \_ e sull' \_ intestazione di esempio webstream WMT \_ \_ , vedere la documentazione di Windows Media Format SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
