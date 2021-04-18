---
description: Quando si configura un componente da raggruppare, COM+ ne manterrà le istanze in un pool, pronto per essere attivato per qualsiasi client che richiede il componente. Tutte le richieste di creazione di oggetti verranno gestite tramite Gestione pool.
ms.assetid: 34978b50-cd20-42fd-ad46-410190478ef8
title: Funzionamento del pool di oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78784fc0e5362c14ceb598b404976c6ca494a19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304825"
---
# <a name="how-object-pooling-works"></a>Funzionamento del pool di oggetti

Quando si configura un componente da raggruppare, COM+ ne manterrà le istanze in un pool, pronto per essere attivato per qualsiasi client che richiede il componente. Tutte le richieste di creazione di oggetti verranno gestite tramite Gestione pool.

I pool sono configurati e gestiti in base ai singoli componenti. Un pool è costituito da oggetti omogenei che condividono lo stesso CLSID. L'unica eccezione riguarda gli oggetti transazionali, per i quali i pool vengono mantenuti contenenti oggetti con affinità di transazione mentre una transazione è in sospeso.

Quando l'applicazione viene avviata, il pool verrà popolato fino al livello minimo che è stato specificato in modo amministrativo, a condizione che la creazione dell'oggetto abbia esito positivo. Poiché le richieste dei client per il componente sono disponibili, vengono soddisfatte per la prima volta dal pool. Se non sono disponibili oggetti in pool e il pool non è ancora al livello massimo specificato, viene creato e attivato un nuovo oggetto per il client.

Quando il pool raggiunge il livello massimo, le richieste client vengono accodate e riceveranno il primo oggetto disponibile dal pool. Il numero di oggetti, inclusi sia attivato che disattivato, non supererà mai il valore massimo del pool. Le richieste di creazione di oggetti si timeout dopo un periodo di tempo specificato amministrativa, in modo da poter controllare il tempo di attesa dei client per la creazione dell'oggetto. Quando si verifica un errore di timeout, il client otterrà il \_ timeout di errore E da [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Quando possibile, COM+ tenterà di riutilizzare un oggetto dopo che è stato rilasciato da un client, fino a quando il pool non raggiunge il livello massimo. L'oggetto è responsabile del monitoraggio dello stato per determinare se è possibile riutilizzarlo e deve restituire un valore appropriato per [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).

Quando viene creato un oggetto in pool, questo viene aggregato in un oggetto più grande che gestirà la durata dell'oggetto. L'oggetto esterno chiama i metodi su [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) in momenti appropriati nel ciclo di vita dell'oggetto, come indicato di seguito:

-   Il metodo [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) viene chiamato ogni volta che l'oggetto viene restituito a un client, attivato in un contesto specifico.
-   Il metodo [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) viene chiamato ogni volta che un oggetto viene rilasciato dal client o, nel caso di un oggetto attivato da JIT, quando viene disattivato.
-   Il metodo [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) viene chiamato ogni volta che un oggetto deve essere restituito al pool generale. Se l'oggetto rileva che alcune risorse riutilizzabili sono in uno stato non valido, deve restituire **false** per questo metodo e la gestione pool eliminerà l'oggetto.

Un oggetto non deve necessariamente implementare [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). In caso contrario, le istanze verranno sempre riutilizzate fino a quando non viene raggiunto il livello massimo del pool.

Per informazioni dettagliate su come configurare i componenti da raggruppare, vedere [configurazione di un componente da raggruppare](configuring-a-component-to-be-pooled.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stringhe del costruttore di oggetti COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controllo della durata e dello stato degli oggetti](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Miglioramento delle prestazioni con il pool di oggetti](improving-performance-with-object-pooling.md)
</dt> <dt>

[Raggruppamento di oggetti transazionali](pooling-transactional-objects.md)
</dt> <dt>

[Requisiti per gli oggetti pool](requirements-for-poolable-objects.md)
</dt> </dl>

 

 
