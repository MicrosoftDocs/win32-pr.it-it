---
description: Supporto per il debug di Visual Basic COM+ a differenza di MTS
ms.assetid: aa012f88-1f88-4c7f-b774-82b9e29da5e9
title: Supporto per il debug di Visual Basic COM+ a differenza di MTS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038b29bbc6fbe5c8375f91f0006b85940f00b944
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305014"
---
# <a name="com-visual-basic-debugging-support-contrasted-with-mts"></a>Supporto per il debug di Visual Basic COM+ a differenza di MTS

COM+ rimuove o riduce diverse limitazioni di debug con Microsoft Visual Basic 6,0 e MTS. Nell'elenco seguente sono riepilogate le modifiche che è possibile prevedere con COM+:

-   Debug di più componenti: in COM+ è possibile eseguire il debug di scenari in cui un client in esecuzione in un'istanza dell'IDE effettua chiamate a un numero qualsiasi di dll in esecuzione in un altro come gruppo di progetto. Gli oggetti nei progetti DLL raggruppati possono chiamarsi reciprocamente in modo arbitrario, propagando il contesto in base alle esigenze. Naturalmente, questo funziona anche quando le dll e il client si trovano nello stesso gruppo di progetto nella stessa istanza dell'IDE.

-   Limitazioni del debug sugli \_ eventi di inizializzazione della classe e di \_ terminazione della classe: con com+ è possibile inserire il codice nell' \_ inizializzazione della classe e \_ gli eventi di terminazione della classe di un componente dell'applicazione com+ anche se il codice tenta di accedere all'oggetto o all'oggetto di contesto corrispondente. È possibile impostare punti di interruzione e usare gli orologi. È anche possibile impostare punti di interruzione nell' \_ evento di terminazione della classe.

    Sebbene non sia più necessario come soluzione alternativa, è comunque possibile implementare l'interfaccia [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) e usare i metodi [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) e [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) se è necessario eseguire il codice durante l'avvio e l'arresto del componente. È anche possibile inserire punti di interruzione nel codice per i metodi **Deactivate** o [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) .

-   Controllo di oggetti MTS: con COM+ è possibile aggiungere orologi per le variabili oggetto restituite da COM+, inclusi i valori restituiti dai metodi [**SafeRef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef), [**GetObjectContext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)e [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) .

-   Maggiore stabilità quando i componenti hanno esito negativo: in COM+, un errore del componente non verrà più interrotto sempre Visual Basic (che viene eseguito nello stesso processo del componente sottoposto a debug). Ad esempio, il supporto per gli errori di riattivazione JIT (just-in-Time) consente ora di esaminare il contesto dell'oggetto durante il debug.

-   Il debugger può riattivare gli oggetti rilasciati da COM+, ad esempio con MTS, Visual Basic 6,0 può riattivare gli oggetti COM+ mentre si esegue il debug in un client in un singolo passaggio. A causa del modo in cui Visual Basic 6,0 individua le informazioni sugli oggetti, si tratta di un comportamento previsto. Si consideri il codice di esempio seguente:

    ``` syntax
    Dim obj As Object
    Set obj = CreateObject("MyApp.MyClass")
    obj.Test  'Call the user-defined subroutine named Test.
    Set obj = Nothing
    ```

    Se obj. Il metodo di test chiama [**IObjectContext:: Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete), com+ libera immediatamente obj dalla memoria, ma obj non è ancora stato impostato su Nothing. Quando obj. Il test restituisce, il debugger Visual Basic chiama [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) su obj per l'interfaccia [**IProvideClassInfo**](/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo) . Il wrapper del contesto associato a obj crea una nuova istanza di MyApp. MyClass per il servizio della chiamata **QueryInterface** . Di conseguenza, l'oggetto non inizializzato verrà visualizzato nel debugger dopo obj. Il test ha restituito. Questo oggetto viene visualizzato solo nel debugger e viene rimosso dall'istruzione successiva per impostare obj su Nothing.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Debug di componenti Visual Basic compilati](debugging-compiled-visual-basic-components.md)
</dt> <dt>

[Debug nell'IDE di Visual Basic](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 
