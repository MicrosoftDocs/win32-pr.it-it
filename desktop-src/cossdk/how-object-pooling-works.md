---
description: Quando si configura un componente per il pool, COM+ ne manterrà le istanze in un pool, pronto per essere attivato per qualsiasi client che richiede il componente. Tutte le richieste di creazione di oggetti verranno gestite tramite il gestore di pool.
ms.assetid: 34978b50-cd20-42fd-ad46-410190478ef8
title: Funzionamento del pool di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df937dd8e3d7a2fb111c7825df101cd2b53f6f39a94326efb1eafe878d74daa6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954041"
---
# <a name="how-object-pooling-works"></a>Funzionamento del pool di oggetti

Quando si configura un componente per il pool, COM+ ne manterrà le istanze in un pool, pronto per essere attivato per qualsiasi client che richiede il componente. Tutte le richieste di creazione di oggetti verranno gestite tramite il gestore di pool.

I pool vengono configurati e gestiti in base ai componenti. Un pool è costituito da oggetti omogenei che condividono lo stesso CLSID. L'unica eccezione è per gli oggetti transazionali, per i quali vengono mantenuti i pool secondari contenenti oggetti con affinità di transazione mentre una transazione è in sospeso.

All'avvio dell'applicazione, il pool verrà popolato fino al livello minimo specificato a livello amministrativo, purché la creazione dell'oggetto abbia esito positivo. Quando le richieste client per il componente arrivano, vengono soddisfatte in base al primo servizio dal pool. Se non sono disponibili oggetti in pool e il pool non è ancora al livello massimo specificato, viene creato e attivato un nuovo oggetto per il client.

Quando il pool raggiunge il livello massimo, le richieste client vengono accodati e riceveranno il primo oggetto disponibile dal pool. Il numero di oggetti, inclusi quelli attivati e disattivati, non supererà mai il valore massimo del pool. Le richieste di creazione di oggetti si verificano dopo un periodo di tempo specificato a livello amministrativo, in modo che sia possibile controllare per quanto tempo i client attenderanno la creazione dell'oggetto. In caso di errore di timeout, il client riceverà l'errore E \_ TIMEOUT da [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Quando possibile, COM+ tenterà di riutilizzare un oggetto dopo che un client lo ha rilasciato, fino a quando il pool non raggiunge il livello massimo. L'oggetto è responsabile del monitoraggio dello stato per determinare se può essere riutilizzato e deve restituire un valore appropriato per [**IObjectControl::CanBePooled.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled)

Quando viene creato, un oggetto in pool viene aggregato in un oggetto più grande che gestirà la durata dell'oggetto. L'oggetto esterno chiama i metodi [**su IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) nei momenti appropriati nel ciclo di vita dell'oggetto, come indicato di seguito:

-   Il [**metodo Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) viene chiamato ogni volta che l'oggetto viene restituito a un client, attivato in un contesto specifico.
-   Il [**metodo Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) viene chiamato ogni volta che un oggetto viene rilasciato dal client o, nel caso di un oggetto attivato da JIT, quando viene disattivato.
-   Il [**metodo CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) viene chiamato ogni volta che un oggetto deve essere restituito al pool generale. Se l'oggetto rileva che una risorsa riutilizzabile è in uno stato non valido, deve restituire **FALSE** per questo metodo e la gestione pool scarterà l'oggetto.

Un oggetto non deve necessariamente implementare [**IObjectControl.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) In caso contrario, le istanze verranno sempre riutilizzate, fino a quando non viene raggiunto il livello massimo del pool.

Per informazioni dettagliate su come configurare i componenti da creare in pool, vedere Configurazione di un [componente per il pooling.](configuring-a-component-to-be-pooled.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stringhe del costruttore di oggetti COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controllo della durata e dello stato degli oggetti](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Miglioramento delle prestazioni con il pooling di oggetti](improving-performance-with-object-pooling.md)
</dt> <dt>

[Pooling di oggetti transazionali](pooling-transactional-objects.md)
</dt> <dt>

[Requisiti per gli oggetti in pool](requirements-for-poolable-objects.md)
</dt> </dl>

 

 
