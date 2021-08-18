---
title: Uso del callback OnStatus
description: Uso del callback OnStatus
ms.assetid: 598e2d13-709b-42a3-ae06-b8c7d208ca9e
keywords:
- Windows Media Format SDK, metodo di callback OnStatus
- Windows Media Format SDK, interfaccia IWMStatusCallback
- Metodo di callback OnStatus,about
- IWMStatusCallback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb1f2ae8ef64204435d7837b75258b77ec12f516103caeb936e82f979049ab4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027119"
---
# <a name="using-the-onstatus-callback"></a>Uso del callback OnStatus

Il metodo di callback [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) viene chiamato da diversi oggetti in Windows Media Format SDK. **OnStatus** riceve messaggi che rappresentano le modifiche nello stato delle operazioni DELL'SDK.

Per usare il metodo di callback **OnStatus,** è necessario implementare una classe nell'applicazione che eredita [**dall'interfaccia IWMStatusCallback.**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) Includere il codice per la **versione di OnStatus** nella classe . Negli esempi inclusi in questo SDK sono disponibili diversi esempi di implementazioni di **OnStatus.** Per altre informazioni sugli esempi, vedere [Applicazioni di esempio.](sample-applications.md)

È necessario associare l'implementazione del callback di stato a vari oggetti di Windows Media Format SDK. Ogni oggetto ha un modo diverso di creare questa associazione. Per un elenco dei metodi che associano oggetti specifici, vedere la pagina di riferimento **IWMStatusCallback.**

I messaggi di stato che possono essere ricevuti da **OnStatus** sono definiti nel [**tipo di enumerazione WMT \_ STATUS.**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status)

È possibile scegliere quali messaggi intercettare e quali ignorare. Tuttavia, la risposta ad alcuni messaggi di stato è necessaria per determinate funzionalità. Ad esempio, quando si usa il lettore asincrono, il [**metodo IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open) apre un file in modo asincrono. L'unico modo per sapere quando il file è stato aperto è intercettare il messaggio MWT \_ OPENED. In genere, i messaggi a cui si risponde sono notifiche del completamento delle attività asincrone.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei metodi di callback**](using-the-callback-methods.md)
</dt> </dl>

 

 




