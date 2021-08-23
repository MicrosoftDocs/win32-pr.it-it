---
description: I componenti transazionali che devono essere in pool hanno requisiti speciali.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Pooling di oggetti transazionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c60180011305d0a03fee10fe1a4838f847306393709dc1bfef39f0ea8f69e18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047309"
---
# <a name="pooling-transactional-objects"></a>Pooling di oggetti transazionali

I componenti transazionali che devono essere in pool hanno requisiti speciali.

## <a name="manually-enlisting-resources"></a>Integrazione manuale delle risorse

Gli oggetti in pool che partecipano alle transazioni devono integrare manualmente le risorse gestite. Se un oggetto contiene risorse gestite tra i client, il gestore delle risorse non sarà in grado di integrarsi automaticamente in una transazione quando l'oggetto viene attivato in un determinato contesto.

L'oggetto stesso deve gestire la logica di rilevamento della transazione, la disattivazione dell'integrazione automatica del gestore risorse e l'integrazione manuale di tutte le risorse che contiene. I passaggi per questa operazione sono specifici del gestore delle risorse in uso. Se è necessario eseguire l'integrazione manuale, consultare la documentazione per resource manager.

Come descritto di seguito, gli oggetti possono essere in pool con affinità di transazione mentre una transazione è attiva e può essere attivata con affinità di transazione se viene chiamata da un client associato a tale transazione. Prima di integrare le risorse, è necessario verificare l'affinità delle transazioni. Se l'oggetto è stato prelevato dal pool specifico di tale transazione, ha già eseguito operazioni nella transazione e ne ha integrata le risorse.

## <a name="turning-off-automatic-enlistment"></a>Disattivazione dell'integrazione automatica

L'integrazione automatica deve essere disattivata dopo l'acquisizione della risorsa, in genere nel costruttore dell'oggetto. Ciò significa che si disabilita l'integrazione automatica e quindi si esegue la connessione.

La disabilitazione dell'integrazione automatica può talvolta essere una procedura sottile, in particolare nel caso di provider di accesso ai dati a più livelli. L'integrazione automatica viene talvolta abbinata al pool di connessioni, come con ODBC e talvolta no, come con OLE DB. Potrebbe essere necessario assicurarsi che l'integrazione automatica sia disattivata a diversi livelli di provider.

## <a name="implementing-iobjectcontrol"></a>Implementazione di IObjectControl

Gli oggetti in pool che partecipano alle transazioni devono monitorare lo stato corrente delle risorse che sono in possesso. Se l'oggetto rileva che si trova in uno stato non riutilizzabile, ad esempio se una connessione non è consentita, deve restituire False per [**IObjectControl::CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled). Ciò avrà l'effetto di eliminare l'istanza dell'oggetto e di eliminare la transazione corrente.

## <a name="transaction-specific-pools"></a>Transaction-Specific pool

Un pool di oggetti è in genere omogeneo e qualsiasi oggetto in pool non attualmente in uso è valido per tornare a qualsiasi client. L'unica eccezione a questa regola è nel caso di oggetti transazionali, per i quali è ottimizzato il pool di oggetti. Quando al client che richiede un oggetto è associata una transazione, COM+ analizza il pool per cercare un oggetto disponibile già associato a tale transazione. Se viene trovato un oggetto con affinità di transazione, viene restituito al client. In caso contrario, viene restituito un oggetto del pool generale.

In questo modo, vengono mantenuti pool secondari speciali contenenti oggetti con affinità per una determinata transazione. Quando la transazione esegue il commit o l'interruzione, questi oggetti vengono restituiti al pool generale senza affinità di transazione, pronti per essere usati da qualsiasi client.

Per questo motivo, quando il componente integra manualmente le risorse gestite in una transazione, deve prima verificare se sono già state integrate. In tal caso, non è necessario eseguire l'integrazione.

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

[Requisiti per gli oggetti in pool](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



