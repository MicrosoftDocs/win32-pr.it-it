---
title: Uso del callback di OnStatus
description: Uso del callback di OnStatus
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- Windows Media Format SDK, metodo OnStatus callback
- Windows Media Format SDK, interfaccia IWMStatusCallback
- Metodo di callback OnStatus, informazioni
- IWMStatusCallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e96b8d7fd75fd8a1d97a56c8b09304c51d0238
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956168"
---
# <a name="using-the-onstatus-callback"></a>Uso del callback di OnStatus

Il metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback viene chiamato da diversi oggetti in Windows Media Format SDK. **OnStatus** riceve messaggi che rappresentano le modifiche dello stato delle operazioni SDK.

Per usare il metodo di callback **OnStatus** , è necessario implementare una classe nell'applicazione che eredita dall'interfaccia [**IWMStatusCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) . Includere il codice per la versione di **OnStatus** nella classe. Alcuni esempi di implementazioni di **OnStatus** sono disponibili negli esempi inclusi in questo SDK. Per ulteriori informazioni sugli esempi, vedere [applicazioni di esempio](sample-applications.md).

È necessario associare l'implementazione del callback di stato a vari oggetti di Windows Media Format SDK. Ogni oggetto ha un modo diverso per effettuare questa associazione. Per un elenco dei metodi che associano oggetti specifici, vedere la pagina di riferimento di **IWMStatusCallback** .

I messaggi di stato che possono essere ricevuti da **OnStatus** sono definiti nel tipo di enumerazione [**\_ dello stato WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) .

È possibile scegliere i messaggi da intercettare e quali ignorare. Tuttavia, per determinate funzionalità è necessaria la risposta ad alcuni messaggi di stato. Ad esempio, quando si usa il Reader asincrono, il metodo [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) apre un file in modo asincrono. L'unico modo per stabilire quando il file è stato aperto consiste nel intercettare il \_ messaggio aperto MWT. In genere, i messaggi a cui si risponde sono notifiche del completamento delle attività asincrone.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Utilizzo dei metodi di callback**](using-the-callback-methods.md)
</dt> </dl>

 

 




