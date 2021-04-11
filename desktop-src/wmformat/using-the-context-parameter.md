---
title: Uso del parametro di contesto
description: Uso del parametro di contesto
ms.assetid: 50e37c36-0ce1-4abd-bb25-f18bb164fdeb
keywords:
- Windows Media Format SDK, parametro di contesto
- Windows Media Format SDK, parametro pvContext
- parametro pvContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 084d7ac0f58d3f3e19ae6b1d6f990a1867988bcd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104117351"
---
# <a name="using-the-context-parameter"></a>Uso del parametro di contesto

Alcuni callback usati da Windows Media Format SDK accettano un parametro denominato *pvContext*. Gli oggetti chiamante passano lungo il valore specificato nel metodo che ha avviato l'azione asincrona. Ad esempio, quando si chiama [**IWMReader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open), è possibile passare un valore per *pvContext*. Quando il metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) viene chiamato dall'oggetto Reader per notificare all'applicazione che il file è stato aperto, passerà qualsiasi valore usato nella chiamata per **aprirlo** come parametro *pvContext* di **OnStatus**. Questo parametro di contesto viene fornito per l'uso e può essere usato nel modo desiderato.

Il parametro *pvContext* viene usato più spesso quando più oggetti devono condividere lo stesso callback. Ad esempio, diversi oggetti usano il metodo [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . È possibile usare *pvContext* per consentire ai diversi oggetti di condividere un'implementazione di **OnStatus** passando un valore diverso per *pvContext* nella chiamata originale. Nell'implementazione di **OnStatus** è possibile creare un ramo della logica di gestione dei messaggi in base al valore di *pvContext*.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Utilizzo dei metodi di callback**](using-the-callback-methods.md)
</dt> </dl>

 

 




