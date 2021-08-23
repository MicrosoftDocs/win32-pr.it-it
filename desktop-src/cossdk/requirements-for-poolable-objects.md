---
description: Gli oggetti in pool devono soddisfare determinati requisiti per consentire l'uso di una singola istanza di oggetto da parte di più client.
ms.assetid: 2cd4211e-be12-4197-8b43-5cb9f2321016
title: Requisiti per gli oggetti in pool
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3e3b67f7d796c199649b64f711ec32a75374bff60ebf900b34871ed4bc310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047289"
---
# <a name="requirements-for-poolable-objects"></a>Requisiti per gli oggetti in pool

Gli oggetti in pool devono soddisfare determinati requisiti per consentire l'uso di una singola istanza di oggetto da parte di più client.

## <a name="stateless"></a>Senza stato

Per mantenere la sicurezza, la coerenza e l'isolamento, gli oggetti in pool non devono contenere uno stato specifico del client dal client al client. È possibile gestire qualsiasi stato per client usando [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), eseguendo l'inizializzazione specifica del contesto con [**IObjectControl::Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) e pulendo qualsiasi stato client con [**IObjectControl::D attiva**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate). Per altri dettagli, vedere Controllo [della durata e dello stato degli oggetti.](controlling-object-lifetime-and-state.md)

## <a name="no-thread-affinity"></a>Nessuna affinità di thread

Gli oggetti in pool non possono essere associati a un thread specifico. In caso contrario, le prestazioni potrebbero essere potenzialmente pericolose. Per questo motivo, gli oggetti in pool non possono essere contrassegnati per l'esecuzione nel modello apartment. devono essere eseguiti nell'apartment multithreading o nell'apartment neutro. Inoltre, gli oggetti in pool non devono usare l'archiviazione thread-local né aggregare il gestore di marshalling a thread libero. Per altri dettagli sul threading in COM+, vedere [Modelli di threading COM+.](com--threading-models.md)

> [!Note]  
> Microsoft Visual Basic 6.0 e gli ambienti di sviluppo precedenti possono creare solo componenti del modello apartment. Tuttavia, in Visual Basic .NET, i componenti possono essere in pool.

 

## <a name="aggregatable"></a>Aggregabile

Gli oggetti in pool devono supportare l'aggregazione, ovvero devono supportare la creazione richiamando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) con un argomento *pUnkOuter* non NULL. Quando COM+ attiva un oggetto in pool, crea un'aggregazione per gestire la durata dell'oggetto in pool e per chiamare metodi su [**IObjectControl.**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) Per informazioni dettagliate sulla scrittura di oggetti aggregabili, vedere [Aggregazione.](/windows/desktop/com/aggregation)

## <a name="transactional-components"></a>Componenti transazionali

Gli oggetti in pool che partecipano alle transazioni devono integrare manualmente le risorse gestite. Mentre è in pool, se l'oggetto contiene una risorsa gestita, ad esempio una connessione di database, non sarà possibile che gestione risorse si integra automaticamente in una transazione quando l'oggetto viene attivato nel contesto specificato. Pertanto, l'oggetto stesso deve gestire la logica di rilevamento della transazione, la disattivazione dell'integrazione automatica del gestore di risorse e l'integrazione manuale di tutte le risorse che contiene. Inoltre, un oggetto in pool transazionale deve riflettere lo stato corrente delle relative risorse nei valori dei parametri [**di IObjectControl::CanBePooled.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) Per altri dettagli, vedere [Pooling Transactional Objects](pooling-transactional-objects.md).

## <a name="implement-iobjectcontrol-to-manage-the-object-lifetime"></a>Implementare IObjectControl per gestire la durata degli oggetti

Gli oggetti in pool devono [**implementare IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol), anche se non è strettamente necessario. I componenti transazionali in pool, tuttavia, devono implementare **IObjectControl**. Questi componenti devono monitorare lo stato delle risorse che contengono e indicare quando non possono essere riutilizzati. Quando [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) restituisce false, elimina una transazione. Per altri dettagli, vedere Controllo [della durata e dello stato degli oggetti.](controlling-object-lifetime-and-state.md)

## <a name="language-restrictions"></a>Restrizioni del linguaggio

I componenti sviluppati con Microsoft Visual Basic 6.0 e versioni precedenti non possono essere in pool perché questi componenti saranno thread modello apartment. Tuttavia, in Visual Basic .NET, i componenti possono essere in pool.

## <a name="legacy-components"></a>Componenti legacy

Fino a quando non sono transazionali e sono conformi ai requisiti precedenti appropriati, i componenti possono essere in pool anche se non sono stati scritti in modo specifico in base alla funzionalità di pooling. Non è necessario implementare [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol); Un componente che non esegue questa operazione semplicemente non parteciperà alla gestione della relativa durata. Se [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) non è implementato, l'oggetto continuerà a essere riutilizzato fino a quando il pool non raggiungerà le dimensioni massime.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stringhe del costruttore di oggetti COM+](com--object-constructor-strings.md)
</dt> <dt>

[Controllo della durata e dello stato degli oggetti](controlling-object-lifetime-and-state.md)
</dt> <dt>

[Funzionamento del pool di oggetti](how-object-pooling-works.md)
</dt> <dt>

[Miglioramento delle prestazioni con il pooling di oggetti](improving-performance-with-object-pooling.md)
</dt> <dt>

[Pooling di oggetti transazionali](pooling-transactional-objects.md)
</dt> </dl>

 

 
