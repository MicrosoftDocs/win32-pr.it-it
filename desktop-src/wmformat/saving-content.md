---
title: Salvataggio del contenuto
description: Salvataggio del contenuto
ms.assetid: 22f4e580-43a4-48b5-8eb3-90e1346a1093
keywords:
- Windows Media Format SDK, salvataggio contenuto
- Windows Media Format SDK, fast cache streaming
- Formato Advanced Systems (ASF), salvataggio contenuto
- ASF (formato avanzato dei sistemi), salvataggio del contenuto
- Advanced Systems Format (ASF), streaming fast cache
- ASF (formato avanzato dei sistemi), streaming fast cache
- flussi, salvataggio di contenuto
- Streaming fast cache, salvataggio contenuto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c215a81accef29f8943ed52ca24264f785d94
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724084"
---
# <a name="saving-content"></a>Salvataggio del contenuto

Usando questo SDK, un'applicazione può salvare il contenuto scaricato o trasmesso nel computer locale dell'utente, chiamando il metodo [**IWMReaderAdvanced2:: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) sull'oggetto Reader. Per il contenuto trasmesso, il server deve usare il flusso fast cache, come descritto nella sezione [Abilitazione del flusso fast cache dal client](enabling-fast-cache-streaming-from-the-client.md). Per il contenuto trasmesso, il metodo **SaveFileAs** crea un file ASX che punta a un file ASF che contiene il contenuto salvato. Se l'oggetto Reader esegue lo streaming di una playlist sul lato server, ogni voce viene salvata come file ASF separato e il file ASX punta a ognuno dei file ASF. Per il contenuto scaricato, il metodo **SaveFileAs** crea semplicemente un file ASF.

Per salvare il contenuto in un file locale, eseguire le operazioni seguenti:

1.  Chiamare [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) con l'URL. **Open** è una chiamata asincrona e restituisce immediatamente un valore. Attendere il completamento dell'operazione, come descritto in [per creare un reader e aprire un file](to-create-a-reader-and-open-a-file.md).
2.  Eseguire una query sull'oggetto Reader per l'interfaccia [**IWMReaderAdvanced4**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4) .
3.  Controllare se il contenuto può essere salvato chiamando il metodo [**IWMReaderAdvanced4:: CanSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cansavefileas) . Se il metodo restituisce false, il contenuto non può essere salvato localmente. In caso contrario, procedere al passaggio 4.
4.  Chiamare il metodo [**IWMReaderAdvanced4:: IsUsingFastCache**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-isusingfastcache) per determinare se il server sta usando lo streaming fast cache.
5.  Chiamare [**IWMReaderAdvanced2:: SaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-savefileas) con un nome file per il file locale. Se il metodo **IsUsingFastCache** ha restituito true, assegnare al file il nome di un'estensione asx. In caso contrario, assegnare al file il nome di un'estensione. ASF,. WMA o. wmv.

L'applicazione può annullare l'operazione di salvataggio mentre è in corso, chiamando il metodo [**IWMReaderAdvanced4:: CancelSaveFileAs**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-cancelsavefileas) .

Il contenuto salvato potrebbe essere protetto con DRM, quindi potrebbe non essere possibile riprodurre il file in un altro computer. Per ulteriori informazioni sulla protezione del contenuto, vedere [Digital Rights Management Features](digital-rights-management-features.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IWMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[**Interfaccia IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> </dl>

 

 




