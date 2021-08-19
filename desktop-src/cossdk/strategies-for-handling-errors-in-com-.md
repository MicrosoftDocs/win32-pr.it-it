---
description: In questo argomento vengono identificate diverse strategie di gestione degli errori da tenere presenti durante lo sviluppo di componenti per COM+.
ms.assetid: 1ae5875b-8085-44f2-9071-c2a5d7543ac1
title: Strategie per la gestione degli errori in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f89736f8a81e51150e9d2480c98c6e5859d9b280fc5f7cd96662f3b1b9f3e8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895701"
---
# <a name="strategies-for-handling-errors-in-com"></a>Strategie per la gestione degli errori in COM+

In questo argomento vengono identificate diverse strategie di gestione degli errori da tenere presenti durante lo sviluppo di componenti per COM+.

-   **Restituisce un valore HRESULT per tutti i metodi in tutte le interfacce dei componenti.**  COM+ usa i **valori HRESULT** per segnalare eventuali errori durante l'esecuzione di chiamate di funzione o chiamate a metodi di interfaccia. HRESULT **indica** se un metodo ha avuto esito positivo o negativo e identifica la funzionalità associata all'errore, ad esempio RPC, WIN32 o ITF per gli errori specifici dell'interfaccia. Inoltre, le API di sistema forniscono una ricerca da **un HRESULT** a una stringa che descrive la condizione di errore. L'uso di metodi **che restituiscono valori HRESULT** è fondamentale per i componenti ben scritti e sono essenziali per il processo di debug. Microsoft Visual Basic definisce automaticamente ogni metodo con **HRESULT** come valore restituito. In Microsoft Visual C++, è necessario restituire in modo esplicito **un HRESULT**. Per altre informazioni sugli HRESULT, vedere [Struttura dei codici di errore COM.](/windows/desktop/com/structure-of-com-error-codes)
-   **Avviare l'oggetto raccolta ErrorInfo in qualsiasi modo fornito dallo strumento di sviluppo.** [**Gli oggetti raccolta ErrorInfo**](errorinfo.md) vengono spesso chiamati eccezioni COM perché consentono a un oggetto di passare (o generare) informazioni dettagliate sugli errori al chiamante, anche attraverso i limiti dell'apartment. Il valore di questo oggetto errore generico è che integra un HRESULT, estendendo il tipo di informazioni sull'errore che è possibile restituire a un chiamante. Ogni **oggetto raccolta ErrorInfo** restituisce una descrizione contestuale, l'origine dell'errore e l'identificatore di interfaccia del metodo che ha generato l'errore. È anche possibile includere puntatori a una voce in un file della Guida. Automazione fornisce tre interfacce per gestire l'oggetto errore. Il componente deve implementare l'interfaccia di automazione **ISupportErrorInfo** per annunciarne il supporto per **la raccolta ErrorInfo.** Quando si verifica un errore, il componente usa **l'interfaccia di automazione ICreateErrorInfo** per inizializzare un oggetto errore. Dopo che il chiamante controlla HRESULT e rileva che la chiamata al metodo non è riuscita, esegue una query sull'oggetto per verificare se supporta la **raccolta ErrorInfo.** In caso contrario, il chiamante usa **l'interfaccia di automazione IErrorInfo** per recuperare le informazioni sull'errore. Visual Basic programmatori possono accedere facilmente all'oggetto raccolta **ErrorInfo,** esposto tramite l'oggetto Err. È possibile generare errori con la funzione Err Raise e rilevare gli errori con **l'istruzione On Error.** Il Visual Basic di esecuzione esegue il mapping per conto dell'utente. Se si usa il supporto del compilatore COM Visual C++, è possibile usare la classe com raise error per segnalare un errore e la classe di errore com per recuperare le \_ \_ informazioni \_ \_ \_ sull'errore. COM+ non propaga le eccezioni C++ tradizionali come informazioni **IErrorInfo** estese. Per altre informazioni **sull'oggetto raccolta ErrorInfo,** vedere "Gestione degli errori" nella Guida di Automazione.
    > [!Note]  
    > COM richiede che il marshalling di tutti gli oggetti raccolta [**ErrorInfo**](errorinfo.md) sia effettuato in base al valore, implicando che anche i componenti che implementano l'interfaccia di automazione **IErrorInfo** devono implementare e supportare [**l'interfaccia IMarshal.**](/windows/desktop/api/objidl/nn-objidl-imarshal) **L'implementazione dell'interfaccia IMarshal** deve supportare il marshalling per valore per il componente.

     

-   **Usare le transazioni per gestire gli errori delle risorse condivise.** Le transazioni automatiche possono ridurre significativamente la quantità di codice di gestione degli errori che è necessario scrivere quando si usano gestori di risorse gestite dallo stato. Tuttavia, le transazioni non eliminano completamente la necessità di gestire gli errori. È comunque necessario restituire i codici di errore dai metodi di interfaccia e controllare i codici di errore all'interno del chiamante per evitare di eseguire operazioni non necessarie per una transazione non necessaria. Per altre informazioni sulla combinazione della gestione degli errori con l'elaborazione delle transazioni, vedere [Speeding Transactions by Notifying the Root Object](speeding-transactions-by-notifying-the-root-object.md).
-   **Generare errori in modo esplicito.** Evitare di lasciare un oggetto a meno che l'oggetto non genera l'errore in modo esplicito. Rilevare tutti gli errori generati dagli strumenti e gestirli nel codice del componente. Includere almeno un gestore standard per segnalare errori imprevisti in modo coerente.
-   **Usare l'intervallo \_ di errori FACILITY ITF per segnalare errori specifici dell'interfaccia.** Gli errori specifici dell'interfaccia devono essere compresi nell'intervallo ITF di FACILITY, tra 0x0200 \_ e 0xFFFF. È possibile definire un codice di errore personalizzato in Visual Basic come offset da vbObjectError. Usare la macro MAKE HRESULT in C++ per introdurre un codice di errore specifico \_ dell'interfaccia, come illustrato nell'esempio seguente:

    ``` syntax
    const HRESULT ERROR_NUMBER = MAKE_HRESULT (SEVERITY_ERROR, FACILITY_ITF, 10);
    ```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Isolamento degli errori e criteri failfast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Ricerca dell'origine di un errore](finding-the-source-of-an-error.md)
</dt> <dt>

[Modalità di modifica dei valori restituiti da COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretazione dei codici di errore](interpreting-error-codes.md)
</dt> <dt>

[Risoluzione dei problemi](troubleshooting.md)
</dt> </dl>

 

 
