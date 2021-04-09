---
title: Per usare un video interlacciato
description: Per usare un video interlacciato
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- Windows Media Format SDK, video interlacciato
- Windows Media Format SDK, codifica video interlacciata
- Windows Media Format SDK, codifica video interlacciato
- Windows Media Format SDK, decodifica video interlacciato
- Windows Media Format SDK, ordine dei campi
- ASF (Advanced Systems Format), video interlacciato
- ASF (Advanced Systems Format), video interlacciato
- ASF (Advanced Systems Format), codifica video interlacciata
- ASF (Advanced Systems Format), codifica video interlacciata
- ASF (Advanced Systems Format), codifica di video interlacciati
- ASF (Advanced Systems Format), codifica video interlacciato
- ASF (Advanced Systems Format), decodifica video interlacciato
- ASF (Advanced Systems Format), decodifica video interlacciato
- ASF (Advanced Systems Format), ordine dei campi
- ASF (formato avanzato dei sistemi), ordine dei campi
- video interlacciato, informazioni
- video interlacciato, codifica
- video interlacciato, decodifica
- video interlacciato, ordine dei campi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858014"
---
# <a name="to-use-interlaced-video"></a>Per usare un video interlacciato

Sono disponibili due tipi di codifica video di base: progressivo e interlacciato. Nella codifica progressiva ogni frame è una rappresentazione codificata di un frame di video. Nella codifica interlacciata ogni frame è una rappresentazione codificata di tutte le righe pari di pixel nel video o di tutte le righe dispari. Ogni frame interlacciato è denominato *campo*, quindi sono presenti campi dispari e persino campi. Una visualizzazione interlacciata (ad esempio un televisore) esegue il rendering dei campi uno alla volta, alternando i campi. Una visualizzazione progressiva esegue il rendering di tutti i frame contemporaneamente.

Il codec del profilo avanzato Windows Media Video 9 fornisce supporto per la gestione dell'interlacciamento nei flussi compressi.

## <a name="when-to-use-interlaced-video"></a>Quando usare un video interlacciato

Codifica video interlacciato è utile solo quando il contenuto viene visualizzato in un dispositivo interlacciato. Il contenuto che deve essere visualizzato in un televisore (tramite un set-top box o un altro dispositivo) potrebbe dover essere interlacciato. Il contenuto che deve essere visualizzato esclusivamente in uno schermo del computer non deve essere codificato come interlacciato.

Per codificare video interlacciato come video progressivo, è necessario configurare le impostazioni di input. Per ulteriori informazioni, vedere [to deinterlacciare video](to-deinterlace-video.md).

## <a name="field-order"></a>Ordine campi

La maggior parte delle origini di video interlacciati, ad esempio schede di acquisizione video, fornisce esempi video che includono entrambi i campi con interfoliazione. Il risultato è simile a un frame completo di video, ad eccezione del fatto che le linee dispari e pari vengono spostate leggermente nel tempo. Non è disponibile alcun standard universale per il campo nell'esempio video interleaved che si verifica prima nel tempo.

È necessario consentire agli utenti di specificare l'ordine dei campi quando si passano esempi interlacciati all'applicazione.

## <a name="encoding-interlaced-video"></a>Codifica video interlacciato

Per usare la codifica interlacciata, seguire questa procedura:

1.  Configurare il flusso video nel profilo in modo che usi l'estensione dell'unità dati del tipo di contenuto chiamando il metodo [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) . Il GUID dell'estensione di esempio per l'estensione del tipo di contenuto è WM \_ SampleExtensionsGUID \_ ContentType.
2.  Impostare il flusso nel profilo e configurare il writer con il profilo come normale.
3.  Prima di passare gli esempi interlacciati al writer, chiamare il metodo [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) per impostare l' \_ impostazione di input g wszInterlacedCoding su **true**.
4.  Per ogni campione interlacciato passato al writer, chiamare il metodo [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) per impostare il tipo di contenuto. I valori del tipo di contenuto sono combinazioni dei flag nella tabella seguente.



| Flag                         | Descrizione                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_INTERlacciato WM CT \_           | Impostare sempre questo flag quando si codifica il contenuto interlacciato. Se si usa questo flag senza impostare un flag per l'ordine dei campi (primo campo di WM \_ CT in \_ basso \_ o primo \_ \_ campo WM CT \_ Top \_ \_ ), il codec presuppone che il campo superiore sia primo. Se il codec usa l'ordine dei campi errato, non dovrebbe avere alcun impatto sulla qualità dell'immagine, ma l'efficienza della codifica sarà interessata. |
| \_primo campo WM CT in \_ basso \_ \_ | In combinazione con il \_ \_ flag interlacciato WM CT, questo flag indica che il campo inferiore (il campo che inizia con la seconda riga nell'esempio) si verifica prima nel tempo.                                                                                                                                                                                          |
| \_ \_ \_ primo campo WM CT \_ Top    | In combinazione con il \_ \_ flag interlacciato WM CT, questo flag indica che il campo superiore (il campo che inizia con la prima riga dell'esempio) si verifica prima nel tempo.                                                                                                                                                                                              |
| \_ \_ \_ primo \_ campo per la ripetizione del CT WM | Indica che il primo campo dell'esempio deve essere ripetuto durante la riproduzione. Questo flag viene usato per i video creati da film dal processo di telecine. Se non viene impostato alcun flag di ordine dei campi insieme a questo flag, si presuppone che il campo superiore si verifichi prima nel tempo.<br/>                                                                             |



 

> [!Note]  
> Se il \_ \_ flag di WM CT interlacciato non è impostato, si presuppone che l'esempio contenga un frame video progressivo.

 

## <a name="decoding-interlaced-video"></a>Decodifica video interlacciato

Quando si decodifica il video interlacciato, è necessario impostare l' \_ impostazione g wszAllowInterlacedOutput su **true** usando il metodo [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) . In caso contrario, il codec fornirà frame progressivi.

L'estensione dell'unità dati del tipo di contenuto viene mantenuta negli esempi di output. È necessario passare l'orientamento del campo al dispositivo di rendering per garantire la riproduzione corretta.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Argomenti avanzati**](advanced-topics.md)
</dt> </dl>

 

 





