---
title: Uso del parametro di contesto
description: Uso del parametro di contesto
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows MEDIA Format SDK, parametro di contesto
- Windows Media Format SDK, parametro pvContext
- Parametro pvContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 102315470243910158fd3bf474a209fa1e0888536671e3ede3764be519c672f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585201"
---
# <a name="using-the-context-parameter"></a>Uso del parametro di contesto

Alcuni dei callback usati dall'SDK Windows Media Format accettano un parametro denominato *pvContext.* Gli oggetti chiamanti passano il valore specificato nel metodo che ha avviato l'azione asincrona. Ad esempio, quando si chiama [**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), è possibile passare un valore per *pvContext*. Quando il metodo [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) viene chiamato dall'oggetto reader per notificare all'applicazione che il file è stato aperto, passerà qualsiasi valore usato nella chiamata a **Open** come parametro *pvContext* di **OnStatus.** Questo parametro di contesto viene fornito per l'uso ed è possibile usarlo nel modo che si desidera.

Il *parametro pvContext* viene usato più spesso quando più oggetti devono condividere lo stesso callback. Ad esempio, diversi oggetti usano il [**metodo IWMStatusCallback::OnStatus.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) È possibile usare *pvContext* per consentire ai diversi oggetti di condividere un'implementazione di **OnStatus** passando un valore diverso per *pvContext* nella chiamata originale. Nell'implementazione di **OnStatus** è possibile creare un ramo della logica di gestione dei messaggi in base al valore *di pvContext.*

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso dei metodi di callback**](using-the-callback-methods.md)
</dt> </dl>

 

 




