---
title: Flussi Web
description: Flussi Web
ms.assetid: 78a2c703-a3f8-4afc-85d3-1c0a8f5a52b5
keywords:
- Windows Media Format SDK, flussi Web
- Formati di sistemi avanzati (ASF), flussi Web
- ASF (formato avanzato dei sistemi), flussi Web
- Windows Media Format SDK, flussi
- Formato di sistemi avanzati (ASF), flussi
- ASF (formato avanzato dei sistemi), flussi
- Flussi Web, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710eb9903662d9707d575a09b55ec8e99a224c38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044643"
---
# <a name="web-streams"></a>Flussi Web

Un flusso Web è simile a un flusso di file in quanto contiene file di dati. In un flusso Web, questi file sono in genere pagine HTML e grafica associata in formato GIF o JPEG.

I flussi Web possono essere particolarmente utili per i file ASF usati come presentazioni. Prima del supporto dei flussi Web, le presentazioni avrebbero URL nei flussi di script all'interno di un file, in modo da consentire il caricamento di una pagina Web in un momento predeterminato. La difficoltà era che la congestione della rete poteva causare ritardi e creare un'esperienza di visualizzazione scadente.

Con i flussi Web, le parti costitutive di pagine Web possono essere incluse nel file ASF come flusso. Man mano che vengono ricevuti, i file possono essere memorizzati nella cache in modo che, quando il comando per visualizzare o eseguire il rendering di un URL venga recapitato, è possibile accedervi immediatamente da un browser. Ciò consente una riproduzione uniforme e uniforme. Il comando Render viene recapitato nel flusso Web, non come comando script in un flusso separato.

È consigliabile che i flussi Web creati usando Windows Media Format 9 Series SDK o versione successiva abbiano il numero di versione 1. Questo valore viene specificato nella struttura [**del \_ \_ formato webstream WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_webstream_format) nel membro **wVersion** . L'SDK non esegue alcuna operazione per applicare questa versione.

> [!Note]  
> Quando ci si connette a flussi broadcast live con flussi Web, è possibile che l'utente riceva un comando Render prima che il file specificato sia effettivamente nella cache locale. A meno che l'applicazione non gestisca questa condizione, nel browser verrà visualizzato l'errore "pagina non trovata".

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Flussi arbitrari**](arbitrary-streams.md)
</dt> <dt>

[**Configurazione di flussi Web**](configuring-web-streams.md)
</dt> </dl>

 

 




