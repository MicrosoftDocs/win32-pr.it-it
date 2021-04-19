---
description: In questo argomento vengono identificate diverse strategie di gestione degli errori da tenere presenti quando si sviluppano componenti per COM+.
ms.assetid: 1ae5875b-8085-44f2-9071-c2a5d7543ac1
title: Strategie per la gestione degli errori in COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca64546683fa45ac8df3bcb47534d8de482798
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304730"
---
# <a name="strategies-for-handling-errors-in-com"></a>Strategie per la gestione degli errori in COM+

In questo argomento vengono identificate diverse strategie di gestione degli errori da tenere presenti quando si sviluppano componenti per COM+.

-   **Restituisce un valore HRESULT per tutti i metodi in tutte le interfacce del componente.**  COM+ utilizza valori **HRESULT** per segnalare eventuali errori durante l'esecuzione di chiamate di funzione o chiamate al metodo di interfaccia. **HRESULT** indica se un metodo ha avuto esito positivo o negativo e identifica la struttura associata all'errore, ad esempio RPC, Win32 o ITF, per gli errori specifici dell'interfaccia. Inoltre, le API di sistema forniscono una ricerca da un **HRESULT** a una stringa che descrive la condizione di errore. L'utilizzo di metodi che restituiscono valori **HRESULT** è fondamentale per i componenti ben scritti e è essenziale per il processo di debug. Microsoft Visual Basic definisce automaticamente ogni metodo con un valore **HRESULT** come valore restituito. In Microsoft Visual C++, è necessario restituire in modo esplicito un valore **HRESULT**. Per ulteriori informazioni sui valori HRESULT, vedere la pagina relativa alla [struttura dei codici di errore com](/windows/desktop/com/structure-of-com-error-codes).
-   **Avviare l'oggetto raccolta ErrorInfo in base a qualsiasi metodo fornito dallo strumento di sviluppo.** Gli oggetti della raccolta [**errorInfo**](errorinfo.md) sono spesso denominati eccezioni com, perché consentono a un oggetto di passare (o generare) informazioni dettagliate sugli errori al chiamante, anche attraverso i limiti dell'Apartment. Il valore di questo oggetto errore generico è che integra un HRESULT, estendendo il tipo di informazioni sugli errori che è possibile restituire a un chiamante. Ogni oggetto della raccolta **errorInfo** restituisce una descrizione contestuale, l'origine dell'errore e l'identificatore di interfaccia del metodo che ha originato l'errore. È anche possibile includere puntatori a una voce in un file della guida. L'automazione offre tre interfacce per la gestione dell'oggetto Error. Il componente deve implementare l'interfaccia di automazione **ISupportErrorInfo** per annunciare il proprio supporto per la raccolta **errorInfo** . Quando si verifica un errore, il componente usa l'interfaccia di automazione **ICreateErrorInfo** per inizializzare un oggetto Error. Quando il chiamante controlla HRESULT e rileva che la chiamata al metodo ha avuto esito negativo, esegue una query sull'oggetto per verificare se supporta la raccolta **errorInfo** . In tal caso, il chiamante usa l'interfaccia di automazione **IErrorInfo** per recuperare le informazioni sull'errore. Visual Basic programmatori possono accedere facilmente all'oggetto raccolta **errorInfo** , esposto tramite l'oggetto Err. È possibile generare errori con la funzione di generazione Err e rilevare errori con l'istruzione **On Error** . Il Visual Basic livello di runtime si occupa automaticamente del mapping. Se si utilizza il supporto del compilatore COM di Visual C++, è possibile utilizzare \_ la \_ classe com raise \_ Error per segnalare un errore e \_ la \_ classe di errore com per recuperare le informazioni sull'errore. In COM+ le eccezioni C++ tradizionali non vengono propagate come informazioni **IErrorInfo** estese. Per ulteriori informazioni sull'oggetto raccolta **errorInfo** , vedere la sezione relativa alla gestione degli errori nella Guida all'automazione.
    > [!Note]  
    > COM richiede che tutti gli oggetti della raccolta [**errorInfo**](errorinfo.md) vengano sottoposti a marshalling per valore, implicando che i componenti che implementano l'interfaccia di automazione **IErrorInfo** debbano implementare e supportare anche l'interfaccia [**IMarshal**](/windows/desktop/api/objidl/nn-objidl-imarshal) . L'implementazione dell'interfaccia **IMarshal** deve supportare il marshalling per valore per il componente.

     

-   **Usare le transazioni per gestire gli errori delle risorse condivise.** Le transazioni automatiche possono ridurre significativamente la quantità di codice di gestione degli errori che è necessario scrivere quando si utilizzano i gestori di risorse gestiti dallo stato. Tuttavia, le transazioni non eliminano completamente la necessità di una gestione degli errori. È comunque necessario restituire i codici di errore dai metodi di interfaccia e verificare i codici di errore all'interno del chiamante per evitare di eseguire operazioni non necessarie per una transazione eliminata. Per ulteriori informazioni sulla combinazione della gestione degli errori con l'elaborazione delle transazioni, vedere [velocizzare le transazioni inviando una notifica all'oggetto radice](speeding-transactions-by-notifying-the-root-object.md).
-   **Genera errori in modo esplicito.** Evitare che le informazioni sugli errori lascino un oggetto a meno che l'oggetto non generi in modo esplicito l'errore. Rilevare tutti gli errori generati dagli strumenti e gestirli nel codice del componente. Includere almeno un gestore standard per segnalare gli errori imprevisti in modo coerente.
-   **Usare la funzionalità \_ intervallo ITF degli errori per segnalare errori specifici dell'interfaccia.** Gli errori specifici dell'interfaccia devono trovarsi nell' \_ intervallo di errori della struttura, tra 0x0200 e 0xFFFF. È possibile definire un codice di errore personalizzato in Visual Basic come offset rispetto a vbObjectError. Usare la \_ macro make HRESULT in C++ per introdurre un codice di errore specifico dell'interfaccia, come illustrato nell'esempio seguente:

    ``` syntax
    const HRESULT ERROR_NUMBER = MAKE_HRESULT (SEVERITY_ERROR, FACILITY_ITF, 10);
    ```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Criteri di isolamento degli errori e FailFast](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[Individuazione dell'origine di un errore](finding-the-source-of-an-error.md)
</dt> <dt>

[Modalità di modifica dei valori restituiti da COM+](how-com--modifies-return-values.md)
</dt> <dt>

[Interpretazione dei codici di errore](interpreting-error-codes.md)
</dt> <dt>

[Risoluzione dei problemi](troubleshooting.md)
</dt> </dl>

 

 
