---
description: Metodi di callback asincroni
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Metodi di callback asincroni
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e59fec2423d6bc1b02a3f5ce05855419596bc92ea54062303ebd1315d087e489
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606711"
---
# <a name="asynchronous-callback-methods"></a>Metodi di callback asincroni

Media Foundation un modo coerente per implementare metodi asincroni, usando un'interfaccia di callback.

Questa sezione descrive come implementare l'interfaccia di callback e come scrivere metodi asincroni che usano questa interfaccia. Contiene gli argomenti seguenti.



| Argomento                                                                                | Descrizione                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Chiamata di metodi asincroni](calling-asynchronous-methods.md)                     | Come chiamare metodi asincroni in Media Foundation.                                               |
| [Implementazione del callback asincrono](implementing-the-asynchronous-callback.md) | Come implementare il metodo di callback [**nell'interfaccia IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) |
| [Supporto di più callback](supporting-multiple-callbacks.md)                   | Come supportare più callback all'interno della stessa classe C++.                                        |
| [Code di lavoro](work-queues.md)                                                       | Le code di lavoro consentono di eseguire operazioni asincrone in un altro thread in modo efficiente.          |
| [Scrittura di un metodo asincrono](writing-an-asynchronous-method.md)                 | Come implementare metodi asincroni in Media Foundation.                                          |
| [Oggetti risultato asincroni personalizzati](custom-asynchronous-result-objects.md)         | Come fornire un'implementazione personalizzata [**dell'interfaccia IMFAsyncResult.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[**Interfaccia IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[Media Foundation API della piattaforma](media-foundation-platform-apis.md)
</dt> </dl>

 

 



