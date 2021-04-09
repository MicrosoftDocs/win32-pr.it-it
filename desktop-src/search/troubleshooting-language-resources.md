---
description: Questo argomento fornisce procedure consigliate e suggerimenti per la convalida e la risoluzione dei problemi relativi alle implementazioni di IWordBreaker e IStemmer.
ms.assetid: b0e199b9-8d81-4445-92f7-de9b8a00a9cb
title: Risoluzione dei problemi relativi a risorse di linguaggio e procedure consigliate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f63a0a8acda3fff1627b37f41c2d81a67b37d66a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750319"
---
# <a name="troubleshooting-language-resources-and-best-practices"></a>Risoluzione dei problemi relativi a risorse di linguaggio e procedure consigliate

Questo argomento fornisce procedure consigliate e suggerimenti per la convalida e la risoluzione dei problemi relativi alle implementazioni di [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) e [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) .

Questo argomento è organizzato nel modo seguente:

-   [Procedure consigliate](#best-practices)
-   [Verifica della coerenza dello stemmer](#testing-stemmer-consistency)
-   [Test dell'input non valido nello stemmer](#testing-for-invalid-input-in-the-stemmer)
-   [Verifica della coerenza del Word breaker](#testing-word-breaker-consistency)
-   [Test dell'input non valido nel Word breaker](#testing-for-invalid-input-in-the-word-breaker)

### <a name="best-practices"></a>Procedure consigliate

-   Verificare che il modello di threading per le risorse della lingua sia impostato su "both" nel registro di sistema.
-   Laddove possibile, inserire i dati della lingua in una risorsa nella DLL anziché in un file separato. In questo modo la DLL risulta più semplice da installare e più sicura. Inoltre, l'inserimento di dati di lingua in una risorsa comporta un miglioramento delle prestazioni per quel componente della risorsa di linguaggio.
-   Ridurre al minimo le risorse di sistema usate dai componenti delle risorse della lingua. Se, ad esempio, ogni istanza di un oggetto risorsa della lingua necessita dell'accesso in sola lettura a un lessico, provare a condividere il lessico tra tutte le istanze.
-   Si consiglia di utilizzare il Word breaker neutro per gestire il testo non presente nella lingua o nelle impostazioni locali dell'implementazione del Word breaker. Ciò consentirà di garantire che il testo venga elaborato in modo coerente in tutte le lingue.
-   Controllare tutti i codici restituiti e restituirli da funzioni quali [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) e [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext). Se l'indicizzazione ha esito negativo, è importante passare l'errore in modo che l'utente riceva una notifica dei documenti indicizzati.

### <a name="testing-stemmer-consistency"></a>Verifica della coerenza dello stemmer

Si consiglia di monitorare le prestazioni di un'implementazione di [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) per coerenza nei casi seguenti:

-   Lo stemmer viene eseguito in modo coerente tra più chiamate a [**IStemmer:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init). Lo stemmer reinizializza con gli stessi parametri dell'inizializzazione precedente, senza rilasciare i parametri.
-   Dato lo stesso corpus di test e le ripetizioni della stessa query, [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) produce l'output identico ed effettua chiamate identiche ai metodi dell'oggetto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .

### <a name="testing-for-invalid-input-in-the-stemmer"></a>Test dell'input non valido nello stemmer

Si consiglia di monitorare il modo in cui i metodi [**IStemmer**](/windows/desktop/api/Indexsrv/nn-indexsrv-istemmer) gestiscono tutti gli errori correlati a parametri non validi. Inoltre, è consigliabile assicurarsi che i metodi dello stemmer non generino eccezioni non gestite. Lo stemmer deve gestire gli errori seguenti:

-   La chiamata a [**IStemmer:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-init) con *pfLicense* è impostata su **null**. Init ha esito negativo e non comporta una violazione di accesso.
-   Chiamata a [**IStemmer:: GetLicenseToUse**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) con il parametro *PpwcsLicense* impostato su **null**. **IStemmer:: GetLicenseToUse** non comporta una violazione di accesso.
-   Chiamata a [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) con il parametro *PwcInBuf* impostato su **null**. **IStemmer:: GenerateWordForms** ha esito negativo (restituisce e non \_ riesce) e non comporta una violazione di accesso.
-   Chiamata a [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) con il parametro *CWC* uguale a 0. **IStemmer:: GenerateWordForms** restituisce correttamente (restituisce S \_ OK) e non genera una violazione di accesso.
-   Chiamata a [**IStemmer:: GenerateWordForms**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-generatewordforms) con il parametro *PwcInBuf* impostato su **null** e il parametro *CWC* uguale a 0. **IStemmer:: GenerateWordForms** ha esito negativo (restituisce e non \_ riesce) e non comporta una violazione di accesso.

### <a name="testing-word-breaker-consistency"></a>Verifica della coerenza del Word breaker

Si consiglia di assicurarsi che l'implementazione di [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) venga eseguita in modo coerente nelle condizioni seguenti:

-   Il Word breaker viene eseguito in modo coerente tra più chiamate al metodo [**IWordBreaker:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) . Il Word breaker viene reinizializzato con gli stessi parametri dell'inizializzazione precedente, senza rilasciare i parametri.
-   Dato lo stesso corpus di test e le ripetizioni della stessa query, il metodo [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) produce l'output identico ed effettua chiamate identiche ai metodi degli oggetti [**IWordSink**](iwordsink.md) e [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) .

### <a name="testing-for-invalid-input-in-the-word-breaker"></a>Test dell'input non valido nel Word breaker

Si consiglia di assicurarsi che i metodi [**IWordBreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker) gestiscano tutti gli errori correlati a parametri non validi. Inoltre, è consigliabile assicurarsi che i metodi del Word breaker non generino eccezioni non gestite. Il Word breaker deve eseguire le funzioni seguenti e gestire gli errori seguenti:

-   La chiamata a [**IWordBreaker:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) deve restituire la lingua \_ e il \_ database \_ non \_ trovati o S \_ OK.
-   La chiamata a [**IWordBreaker:: init**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-init) inizializza correttamente il parametro *pfLicense* su **false** e chiama [**IStemmer:: GetLicenseToUse**](/windows/desktop/api/Indexsrv/nf-indexsrv-istemmer-getlicensetouse) e non genera una violazione di accesso.
-   Il Word breaker non legge oltre la fine del parametro *awcBuffer* nel metodo [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) .
-   Chiamata a [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) con *PwcInBuf* impostato su **null**. **IWordBreaker:: BreakText** ha esito negativo (restituisce e non \_ riesce) e non comporta una violazione di accesso.
-   Chiamata a [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) con il parametro *CWC* uguale a 0. **IWordBreaker:: BreakText** restituisce correttamente (restituisce S \_ OK) e non genera una violazione di accesso.
-   Chiamare il metodo [**IWordBreaker:: BreakText**](/windows/desktop/api/Indexsrv/nf-indexsrv-iwordbreaker-breaktext) con il parametro *PwcInBuf* impostato su **null** e il parametro *CWC* uguale a 0. **IWordBreaker:: BreakText** ha esito negativo (restituisce e non \_ riesce) e non comporta una violazione di accesso.
-   Le frasi generate durante la creazione dell'indice contengono lo stesso numero di parole.
-   Le frasi vengono generate durante la creazione dell'indice tramite chiamate successive ai metodi [**IWordFormSink::P utword**](iwordsink-putword.md) e [**IWordFormSink::P utaltword**](iwordsink-putaltword.md) . Il Word breaker utilizza solo l'oggetto [**IPhraseSink**](/windows/win32/api/indexsrv/nn-indexsrv-iphrasesink) durante la fase di query.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Estensione delle risorse della lingua](extending-language-resources-in-windows-search.md)
</dt> <dt>

[Informazioni sui componenti delle risorse della lingua](understanding-language-resource-components.md)
</dt> <dt>

[Implementazione di un Word breaker e uno stemmer](implementing-a-word-breaker-and-stemmer.md)
</dt> <dt>

[Considerazioni linguistiche e Unicode](linguistic-and-unicode-considerations.md)
</dt> </dl>

 

 
