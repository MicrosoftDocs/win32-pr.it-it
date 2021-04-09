---
description: Gli oggetti configurabili devono soddisfare determinati requisiti per consentire l'uso di una singola istanza di oggetto da parte di più client.
ms.assetid: 2cd4211e-be12-4197-8b43-5cb9f2321016
title: Requisiti per gli oggetti pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78d6834210f180ad8b514b51b6926b5cd30714fd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966106"
---
# <a name="requirements-for-poolable-objects"></a>Requisiti per gli oggetti pool

Gli oggetti configurabili devono soddisfare determinati requisiti per consentire l'uso di una singola istanza di oggetto da parte di più client.

## <a name="stateless"></a>Senza stato

Per mantenere la sicurezza, la coerenza e l'isolamento, gli oggetti raggruppabili non devono mantenere lo stato specifico del client da client a client. È possibile gestire qualsiasi stato per ogni client usando [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), eseguendo l'inizializzazione specifica del contesto con [**IObjectControl:: Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) e pulendo qualsiasi stato del client con [**IObjectControl::D ttiva**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate). Per informazioni dettagliate, vedere [controllo della durata e dello stato degli oggetti](controlling-object-lifetime-and-state.md).

## <a name="no-thread-affinity"></a>Nessuna affinità di thread

Impossibile associare oggetti pool a un thread specifico. in caso contrario, le prestazioni potrebbero essere potenzialmente disastrose. Per questo motivo, non è possibile contrassegnare gli oggetti pool per l'esecuzione nel modello di Apartment; devono essere eseguiti nell'Apartment a thread multipli o in quello neutro. Inoltre, gli oggetti del pool non devono usare l'archiviazione locale di thread né devono aggregare il gestore di marshalling a thread libero. Per informazioni più dettagliate sul threading in COM+, vedere [modelli di threading com+](com--threading-models.md).

> [!Note]  
> Gli ambienti di sviluppo Microsoft Visual Basic 6,0 e versioni precedenti possono creare solo componenti del modello di Apartment. Tuttavia, in Visual Basic .NET è possibile raggruppare i componenti.

 

## <a name="aggregatable"></a>Aggregabile

Gli oggetti pool devono supportare l'aggregazione, ovvero devono supportare la creazione richiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con un argomento *pUnkOuter* non null. Quando COM+ attiva un oggetto in pool, crea un'aggregazione per gestire la durata dell'oggetto in pool e per chiamare i metodi su [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Per informazioni dettagliate sulla scrittura di oggetti aggregabili, vedere [aggregazione](/windows/desktop/com/aggregation).

## <a name="transactional-components"></a>Componenti transazionali

Gli oggetti pool che fanno parte delle transazioni devono integrare manualmente le risorse gestite. Quando viene inserito in un pool, se l'oggetto contiene una risorsa gestita, ad esempio una connessione di database, non sarà possibile eseguire automaticamente l'integrazione di Resource Manager in una transazione quando l'oggetto viene attivato nel contesto specificato. Pertanto, è necessario che l'oggetto stesso gestisca la logica di rilevamento della transazione, disattivando l'integrazione automatica di Resource Manager e integrando manualmente tutte le risorse che possiede. Inoltre, un oggetto in pool transazionale deve riflettere lo stato corrente delle risorse nei valori dei parametri di [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled). Per informazioni dettagliate, vedere [pooling di oggetti transazionali](pooling-transactional-objects.md).

## <a name="implement-iobjectcontrol-to-manage-the-object-lifetime"></a>Implementare IObjectControl per gestire la durata degli oggetti

Gli oggetti in pool devono implementare [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), anche se non è strettamente necessario. I componenti transazionali in pool devono tuttavia implementare **IObjectControl**. Questi componenti dovrebbero monitorare lo stato delle risorse che contengono e indicano quando non possono essere riutilizzati. Quando [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) restituisce false, verrà eliminata una transazione. Per informazioni dettagliate, vedere [controllo della durata e dello stato degli oggetti](controlling-object-lifetime-and-state.md).

## <a name="language-restrictions"></a>Limitazioni della lingua

I componenti sviluppati con Microsoft Visual Basic 6,0 e versioni precedenti non possono essere raggruppati in quanto questi componenti saranno con threading di tipo Apartment. Tuttavia, in Visual Basic .NET è possibile raggruppare i componenti.

## <a name="legacy-components"></a>Componenti legacy

Fino a quando non sono transazionali e sono conformi ai requisiti precedenti appropriati, i componenti possono essere inseriti in un pool anche se non sono stati scritti specificamente con la capacità del pool. Non è necessario implementare [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). un componente che non esegue questa operazione non farà semplicemente parte della gestione del suo ciclo di vita. Se [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) non è implementato, l'oggetto continuerà a essere usato fino a quando il pool non raggiunge la dimensione massima.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stringhe del costruttore di oggetti COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controllo della durata e dello stato degli oggetti](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Funzionamento del pool di oggetti](how-object-pooling-works.md)
</dt> <dt>

[Miglioramento delle prestazioni con il pool di oggetti](improving-performance-with-object-pooling.md)
</dt> <dt>

[Raggruppamento di oggetti transazionali](pooling-transactional-objects.md)
</dt> </dl>

 

 
