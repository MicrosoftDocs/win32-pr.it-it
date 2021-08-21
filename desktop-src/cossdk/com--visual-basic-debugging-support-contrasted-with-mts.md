---
description: Supporto del debug Visual Basic COM+ a differenza di MTS
ms.assetid: aa012f88-1f88-4c7f-b774-82b9e29da5e9
title: Supporto del debug Visual Basic COM+ a differenza di MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2c278fbe414b2e58c5dd4aa8a3b2d694ed8ba49b0523e118f69116ec7061868
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118102473"
---
# <a name="com-visual-basic-debugging-support-contrasted-with-mts"></a>Supporto del debug Visual Basic COM+ a differenza di MTS

COM+ rimuove o riduce diverse limitazioni del debug con Microsoft Visual Basic 6.0 e MTS. L'elenco seguente riepiloga le modifiche che è possibile prevedere con COM+:

-   Debug di più componenti: in COM+, è possibile eseguire il debug di scenari in cui un client in esecuzione in un'istanza dell'IDE effettua chiamate a un numero qualsiasi di DLL in esecuzione in un'altra come gruppo di progetti. Gli oggetti nei progetti DLL raggruppati possono chiamarsi arbitrariamente, scorrendo il contesto in base alle esigenze. Naturalmente, questo funziona anche quando le DLL e il client sono nello stesso gruppo di progetti nella stessa istanza dell'IDE.

-   Limitazioni di debug sugli eventi di inizializzazione della classe e di terminazione della classe: con COM+, è possibile inserire il codice negli eventi Class Initialize e Class Terminate di un componente dell'applicazione COM+, anche se il codice tenta di accedere all'oggetto o al relativo oggetto di contesto \_ \_ \_ \_ corrispondente. È possibile impostare punti di interruzione e usare espressioni di controllo. È anche possibile impostare punti di interruzione nell'evento Class \_ Terminate.

    Anche se non è più necessaria come soluzione alternativa, è comunque possibile implementare l'interfaccia [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) e usare i relativi metodi [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) e [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) se è necessario eseguire codice durante l'avvio e l'arresto del componente. È anche possibile inserire punti di interruzione nel codice per **i metodi Deactivate** o [**CanBePooled.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)

-   Osservare gli oggetti MTS: con COM+, è possibile aggiungere espressioni di controllo per le variabili oggetto restituite da COM+, inclusi i valori restituiti dai metodi [**SafeRef,**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef) [**GetObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)e [**IObjectContext::CreateInstance.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance)

-   Maggiore stabilità in caso di errore dei componenti: in COM+, un errore del componente non viene più sempre Visual Basic (che viene eseguito nello stesso processo del componente di cui è stato eseguito il debug). Ad esempio, il supporto per gli errori di riattivazione JIT consente ora di esaminare il contesto dell'oggetto durante il debug.

-   Il debugger può riattivare gli oggetti rilasciati da COM+: come con MTS, Visual Basic 6.0 potrebbe riattivare gli oggetti COM+ durante il debug a passaggio singolo in un client. A causa del modo in cui Visual Basic 6.0 individua le informazioni sugli oggetti, questo è il comportamento previsto. Si consideri il codice di esempio seguente:

    ``` syntax
    Dim obj As Object
    Set obj = CreateObject("MyApp.MyClass")
    obj.Test  'Call the user-defined subroutine named Test.
    Set obj = Nothing
    ```

    Se obj. Il metodo di test chiama [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), COM+ libera immediatamente obj dalla memoria, ma obj non è ancora stato impostato su Nothing. Quando obj. Viene restituito il test, Visual Basic debugger chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su obj per [**l'interfaccia IProvideClassInfo.**](/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo) Il wrapper di contesto associato a obj crea una nuova istanza di MyApp.MyClass per eseguire la **chiamata QueryInterface.** Di conseguenza, questo oggetto non inizializzato verrà visualizzato nel debugger dopo obj. Il test è stato restituito. Questo oggetto viene visualizzato solo nel debugger e viene rimosso dall'istruzione successiva per impostare obj su Nothing.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Debug di componenti Visual Basic compilati](debugging-compiled-visual-basic-components.md)
</dt> <dt>

[Debug nell'IDE Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 
