---
description: Il servizio di attivazione JIT (just-in-Time) consente a COM+ di disattivare un oggetto mentre un client conserva ancora un riferimento attivo a tale oggetto.
ms.assetid: dbc7b257-8506-42c8-8a78-3474c6d4f4b6
title: Concetti relativi all'attivazione JIT di COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c942bfeb342ea305083e0c7d7ebdea2fe96bf24
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304642"
---
# <a name="com-just-in-time-activation-concepts"></a>Concetti relativi all'attivazione JIT di COM+

Il servizio di attivazione JIT (just-in-Time) consente a COM+ di disattivare un oggetto mentre un client conserva ancora un riferimento attivo a tale oggetto. La volta successiva che il client chiama un metodo sull'oggetto, che il client ritiene ancora attivo, il servizio di attivazione JIT COM+ riattiva l'oggetto in modo trasparente al client, solo nel tempo.

Il vantaggio principale dell'utilizzo di COM + JIT è che è possibile consentire ai client di mantenere i riferimenti agli oggetti per tutto il tempo necessario, senza necessariamente vincolare risorse server importanti, ad esempio la memoria. Altri importanti vantaggi sono i seguenti:

-   Utilizzando il servizio di attivazione JIT COM+, il modello di programmazione per il client viene notevolmente semplificato in quanto il client non deve considerare la modalità di utilizzo di oggetti server e risorse server costosi. Senza l'attivazione JIT, i client possono comportare una riduzione significativa quando spesso devono chiamare e rilasciare oggetti.
    > [!Note]  
    > È possibile affinare ulteriormente questo vantaggio in merito alle prestazioni utilizzando il servizio di [pool di oggetti com+](com--object-pooling.md) . Grazie al pool di oggetti attivati tramite JIT, è possibile velocizzare la riattivazione degli oggetti per i client mentre si riutilizzano le risorse che potrebbero contenere, garantendo un controllo più preciso sulla quantità di memoria utilizzata da un determinato oggetto nel server. Per informazioni dettagliate, vedere [pool di oggetti e attivazione JIT com+](object-pooling-and-com--jit-activation.md).

     

-   Con le applicazioni distribuite, è necessario un ciclo di andata e ritorno di rete costoso per la creazione di ogni oggetto e maggiore è il client dal server, maggiori sono i costi di attivazione e di marshalling dell'oggetto server, l'apertura del canale e la configurazione del proxy e dello stub. Utilizzando il servizio di attivazione JIT COM+, è possibile ridurre al minimo la frequenza di creazione di oggetti per migliorare significativamente le prestazioni dell'applicazione.
-   Quando si utilizza l'attivazione JIT COM+ per attivare gli oggetti ai quali i client contengono riferimenti di lunga durata ma che non vengono necessariamente utilizzati continuamente, la memoria del server non è sempre vincolata a mantenere attivi gli oggetti. Questo può aumentare significativamente la scalabilità dell'applicazione. L'unico miglioramento delle prestazioni che i client vedono è il tempo impiegato da COM+ per riattivare l'oggetto, in genere solo marginalmente più tempo del necessario per allocare memoria per l'oggetto e sostanzialmente inferiore rispetto al round trip della rete per la creazione di oggetti remoti.

## <a name="enabling-com-jit-activation"></a>Abilitazione dell'attivazione JIT COM+

È possibile abilitare il servizio di attivazione JIT COM+ per un componente utilizzando lo strumento di amministrazione Servizi componenti o le funzioni amministrative. Per informazioni dettagliate su come eseguire questa operazione, vedere [Abilitazione dell'attivazione JIT per un componente](enabling-jit-activation-for-a-component.md).

L'attivazione JIT COM+ può interagire con altri servizi COM+, come nel seguente esempio:

-   Quando il componente richiede transazioni, l'attivazione JIT viene abilitata automaticamente. Per maggiori dettagli, vedere [transazioni e attivazione JIT com+](transactions-and-com--jit-activation.md).
-   Quando il componente è abilitato per l'attivazione JIT, la sincronizzazione viene impostata automaticamente su Required. Ciò significa che se due client chiamano simultaneamente un componente attivato tramite JIT e una chiamata al metodo per uno di essi restituisce, causando la disattivazione dell'oggetto, l'altro non viene lasciato invariato.

## <a name="how-deactivation-is-triggered"></a>Modalità di attivazione della disattivazione

COM+ disattiva un oggetto in base allo stato del bit di fatto sul contesto dell'oggetto. L'oggetto può utilizzare questo bit per indicare se è stato eseguito, ovvero se è pronto per essere disattivato, durante una chiamata al metodo specificata. Per ulteriori informazioni, vedere [impostazione del bit fatto](setting-the-done-bit.md).

## <a name="using-the-auto-done-property"></a>Uso della proprietà auto-done

Utilizzando lo strumento di amministrazione Servizi componenti, è possibile configurare un metodo in modo che l'oggetto venga disattivato automaticamente al ritorno del metodo. (Vedere [Abilitazione dell'operazione automatica per un metodo](enabling-auto-done-for-a-method.md) per istruzioni su come impostare questa proprietà). Selezionando questa opzione, è possibile eliminare le chiamate al metodo ripetitive per votare le transazioni. Poiché l'impostazione predefinita per il bit di coerenza è true, se è stato modificato il bit done su true e non si esegue alcuna operazione per modificare queste impostazioni, [**IObjectContext:: Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) viene chiamato automaticamente dopo la restituzione del metodo.

Tuttavia, esiste un avvertimento a questo comportamento: COM+ analizzerà il valore HRESULT restituito dal metodo. Se HRESULT indica un errore, il bit di coerenza è impostato su false e il risultato è lo stesso di se è stato chiamato [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort).

Per riepilogare, se si seleziona operazione eseguita automaticamente per un metodo e non si esegue alcuna azione per impostare alcun bit e se viene restituito HRESULT (HR), si applica quanto segue:

-   Se ha ESITo positivo (HR), è come se fosse stato chiamato il metodo [**Tocomplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete).
-   Se ha ESITo negativo (HR), è come se fosse stato chiamato il metodo [**SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort).

## <a name="using-iobjectcontrol-to-manage-object-activation-and-deactivation"></a>Uso di IObjectControl per gestire l'attivazione e la disattivazione di oggetti

È possibile implementare l'interfaccia [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) in modo che il runtime com+ gestisca automaticamente la disattivazione e la riattivazione per gli oggetti. Quando un oggetto implementa questa interfaccia, COM+ chiama [**IObjectControl::D ttiva**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) quando disattiva l'oggetto e [**IObjectControl:: Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) quando viene riattivato. Questi metodi consentono l'inizializzazione automatica del contesto per l'attivazione di oggetti e la pulizia dello stato in caso di disattivazione.

Se si esegue il pooling di oggetti che utilizzano l'attivazione JIT COM+, è consigliabile implementare [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Per informazioni dettagliate, vedere [pool di oggetti e attivazione JIT com+](object-pooling-and-com--jit-activation.md).

## <a name="statelessness-and-jit-activation"></a>Stato di assenza e attivazione JIT

Gli oggetti transazionali sono necessariamente senza stato perché non è possibile condividere lo stato attraverso un limite di transazione. Pertanto, si utilizzerà l'attivazione JIT solo quando l'oggetto non dispone di alcuno stato che andrebbe perso in caso di disattivazione. in caso contrario, si viola l'isolamento delle transazioni. A causa dei modelli di utilizzo naturale degli oggetti transazionali, eseguono alcune unità di lavoro e rilasciano l'oggetto quando viene eseguito il commit o l'interruzione della transazione, ovvero l'attivazione JIT e le transazioni automatiche sono strettamente correlate. La configurazione di un oggetto per richiedere transazioni Abilita automaticamente l'attivazione JIT COM+.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Attività di attivazione JIT di COM+](com--just-in-time-activation-tasks.md)
</dt> <dt>

[Pool di oggetti e attivazione JIT COM+](object-pooling-and-com--jit-activation.md)
</dt> <dt>

[Transazioni e attivazione JIT COM+](transactions-and-com--jit-activation.md)
</dt> </dl>

 

 



