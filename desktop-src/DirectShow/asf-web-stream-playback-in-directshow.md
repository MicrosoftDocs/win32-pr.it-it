---
description: Riproduzione del flusso Web ASF in DirectShow
ms.assetid: c7818c62-24af-4eac-84b8-f76be4ca6c09
title: Riproduzione del flusso Web ASF in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28d9d3b7ea4fba5537383a846e6eff64f3815eefa21613c6056a15a5e497f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824626"
---
# <a name="asf-web-stream-playback-in-directshow"></a>Riproduzione del flusso Web ASF in DirectShow

Microsoft DirectShow supporta i flussi Web negli scenari di riproduzione di file tramite il filtro [lettore ASF WM,](wm-asf-reader-filter.md) ma è necessario scrivere un filtro DirectShow personalizzato per acquisire e rendere persistente il flusso.

> [!Note]  
> Per riprodurre flussi Web nel contenuto trasmesso da un server che esegue Servizi Windows Media, usare il controllo Windows Media Player Serie 9 ActiveX® incorporato in una pagina Web.

 

Quando viene specificato un file contenente flussi di tipo WMMEDIATYPE FileTransfer, il lettore \_ ASF WM creerà un pin di output. Il blocco di formato sarà una [**struttura WMT \_ WEBSTREAM \_ FORMAT.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format) Questa struttura è documentata nella documentazione di Windows Media Format SDK. Se non è disponibile alcun filtro downstream in grado di gestire il tipo di supporto, il pin rimarrà scollegato, ma il file continuerà a riprodurre i flussi audio e/o video.

Ogni esempio di supporto in un flusso Web contiene una struttura [**WMT \_ WEBSTREAM \_ SAMPLE \_ HEADER,**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_sample_header) documentata nella documentazione di Windows Media Format SDK. La struttura ha una lunghezza variabile a seconda della lunghezza del relativo **membro wszURL.** Il puntatore ai dati di esempio punta inizialmente a questa struttura ed è necessario far avanzare il puntatore oltre la struttura per accedere ai dati effettivi nel flusso.

Il filtro del gestore del flusso Web deve essere basato sulla [**classe CBaseRenderer.**](cbaserenderer.md) Nel metodo [**CBaseRenderer::D oRenderSample**](cbaserenderer-dorendersample.md) il filtro dovrà analizzare la struttura per ottenere informazioni sul flusso Web e quindi eseguire l'azione appropriata. In genere, ciò comporta il salvataggio del file su disco e quindi la chiamata delle funzioni [**CreateUrlCacheEntry**](/windows/desktop/api/wininet/nf-wininet-createurlcacheentrya) e [**CommitUrlCacheEntryW**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentryw) o [**CommitUrlCacheEntryA**](/windows/desktop/api/wininet/nf-wininet-commiturlcacheentrya) per inserire i file nella cache Internet Explorer cache. Il filtro deve gestire file multipart, ovvero file di dimensioni maggiori di un campione, e deve anche gestire i comandi di rendering, specificati dal membro **\_ WMT WEBSTREAM \_ SAMPLE \_ HEADER.wSampleType.** Il filtro invia un evento [**\_ EC OLE \_ EVENT**](ec-ole-event.md) all'applicazione, insieme al testo della stringa **\_ WMT WEBSTREAM \_ SAMPLE \_ HEADER.wszURL** che contiene il nome del file di cui eseguire il rendering. L'applicazione fa quindi in modo che il browser visualizza la pagina specificata. Se il flusso Web è stato creato correttamente, il file deve essere già presente nella cache.

Per altre informazioni su WMT WEBSTREAM FORMAT e \_ \_ WMT WEBSTREAM SAMPLE HEADER, vedere la documentazione di \_ \_ Windows Media Format \_ SDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Lettura di file ASF in DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 
