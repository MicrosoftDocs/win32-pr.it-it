---
description: Uso delle estensioni della Shell per implementare un gestore di hook di copia.
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: Come creare gestori di hook di copia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1468839eacc10272f8f97a120b98ada6d580bacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227439"
---
# <a name="how-to-create-copy-hook-handlers"></a>Come creare gestori di hook di copia

Le procedure generali per l'implementazione e la registrazione di un gestore di estensione della shell sono descritte in [creazione di gestori di estensioni della shell](handlers.md). Questo documento è incentrato sugli aspetti dell'implementazione specifici dei gestori di hook di copia.

-   [Implementazione di gestori di hook di copia](#step-1-implementing-copy-hook-handlers)
-   [Registrazione di gestori di hook di copia](#step-2-registering-copy-hook-handlers)
-   [Argomenti correlati](#related-topics)

## <a name="instructions"></a>Istruzioni

### <a name="step-1-implementing-copy-hook-handlers"></a>Passaggio 1: implementazione di gestori di hook di copia

Come tutti i gestori di estensioni della shell, i gestori di hook di copia sono oggetti COM (Component Object Model in-process) implementati come dll. Esportano un'interfaccia oltre a [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)). La shell Inizializza direttamente il gestore, pertanto non è necessaria un'interfaccia di inizializzazione, ad esempio [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).

L'interfaccia [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) ha un singolo metodo, [**ICopyHook:: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)). Quando una cartella sta per essere spostata, la shell chiama questo metodo. Viene passata una serie di informazioni, tra cui:

-   Nome della cartella.
-   Destinazione o nuovo nome della cartella.
-   Operazione tentata.
-   Attributi delle cartelle di origine e di destinazione.
-   Handle di finestra che può essere utilizzato per visualizzare un'interfaccia utente.

Quando viene chiamato il metodo [**ICopyHook:: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) del gestore, viene restituito uno dei tre valori seguenti per indicare alla shell come procedere.



| Valore    | Descrizione                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| IDYES    | Consente l'operazione.                                                                                                                            |
| IDNO     | Impedisce l'operazione in questa cartella. La shell può continuare con qualsiasi altra operazione approvata, ad esempio un'operazione di copia batch. |
| IDCANCEL | Impedisce l'operazione corrente e Annulla tutte le operazioni in sospeso.                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a>Passaggio 2: registrazione di gestori di hook di copia

I gestori di hook di copia per le cartelle sono registrati nella **\_ \_** \\  \\  \\ sottochiave shellex **CopyHookHandlers** della directory radice delle classi HKEY. Creare una sottochiave di **CopyHookHandlers** denominata per il gestore, quindi impostare il valore predefinito della sottochiave sul formato stringa del GUID dell'identificatore di classe del gestore (CLSID).

Nell'esempio seguente la sottochiave **MyCopyHandler** viene aggiunta all'elenco di gestori di hook di copia della shell.

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

I gestori di hook di copia per gli oggetti stampante sono registrati in modo sostanzialmente analogo. L'unica differenza è che è necessario registrarli nella sottochiave delle stampanti **\_ \_ radice delle classi HKEY** \\  .

## <a name="remarks"></a>Commenti

In genere, gli utenti e le applicazioni possono copiare, spostare, eliminare o rinominare cartelle con poche restrizioni. Implementando un gestore di hook di copia, è possibile controllare se queste operazioni vengono eseguite. Ad esempio, l'implementazione di un gestore di questo tipo consente di impedire la ridenominazione o l'eliminazione di cartelle critiche. I gestori di hook di copia possono essere implementati anche per gli oggetti Printer.

I gestori di hook di copia sono globali. La shell chiama tutti i gestori registrati ogni volta che un'applicazione o un utente tenta di copiare, spostare, eliminare o rinominare una cartella o un oggetto Printer. Il gestore non esegue l'operazione stessa. Viene approvata o bloccata. Se tutti i gestori approvano, la shell esegue l'operazione. Se un gestore oppone l'operazione, viene annullato e i gestori rimanenti non vengono chiamati. I gestori di hook di copia non sono informati dell'esito positivo o negativo dell'operazione, quindi non possono essere usati per monitorare le operazioni sui file.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di gestori di estensione della shell](handlers.md)
</dt> <dt>

[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))
</dt> </dl>

 

 
