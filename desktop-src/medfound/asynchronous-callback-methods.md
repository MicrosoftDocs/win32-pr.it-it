---
description: Metodi di callback asincroni
ms.assetid: ea778eaa-6460-4a93-bd6a-1857ea8b6230
title: Metodi di callback asincroni
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0064873a5b026b6910597ebc9911f56f00584b03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305520"
---
# <a name="asynchronous-callback-methods"></a>Metodi di callback asincroni

Media Foundation offre un modo coerente per implementare metodi asincroni, usando un'interfaccia di callback.

In questa sezione viene descritto come implementare l'interfaccia di callback e come scrivere metodi asincroni che utilizzano questa interfaccia. Contiene gli argomenti seguenti.



| Argomento                                                                                | Descrizione                                                                                         |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [Chiamata di metodi asincroni](calling-asynchronous-methods.md)                     | Come chiamare metodi asincroni in Media Foundation.                                               |
| [Implementazione del callback asincrono](implementing-the-asynchronous-callback.md) | Come implementare il metodo di callback nell'interfaccia [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . |
| [Supporto di più callback](supporting-multiple-callbacks.md)                   | Come supportare più callback all'interno della stessa classe C++.                                        |
| [Code di lavoro](work-queues.md)                                                       | Le code di lavoro rappresentano un modo efficiente per eseguire operazioni asincrone su un altro thread.          |
| [Scrittura di un metodo asincrono](writing-an-asynchronous-method.md)                 | Come implementare metodi asincroni in Media Foundation.                                          |
| [Oggetti risultato asincrono personalizzati](custom-asynchronous-result-objects.md)         | Come fornire un'implementazione personalizzata dell'interfaccia [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .   |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback)
</dt> <dt>

[**Interfaccia IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult)
</dt> <dt>

[API della piattaforma Media Foundation](media-foundation-platform-apis.md)
</dt> </dl>

 

 



