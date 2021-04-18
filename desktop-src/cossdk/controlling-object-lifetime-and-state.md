---
description: Controllo della durata e dello stato degli oggetti
ms.assetid: 172e07a2-1711-4353-9099-ff9d31a564c6
title: Controllo della durata e dello stato degli oggetti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525cc1d582d85bc84ef2b1749a427711d1fe26fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305013"
---
# <a name="controlling-object-lifetime-and-state"></a>Controllo della durata e dello stato degli oggetti

Un oggetto in pool può partecipare al modo in cui COM+ gestisce l'attività nel pool implementando [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol). Quando viene creato un oggetto in pool, questo viene aggregato in un oggetto più grande che gestirà l'oggetto chiamando i metodi seguenti su **IObjectControl** nei punti regolari del ciclo di vita dell'oggetto:

-   [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate): viene chiamato ogni volta che l'oggetto viene restituito a un client, attivato in un contesto specifico.
-   [**Deactivate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate): viene chiamato ogni volta che un oggetto viene rilasciato dal client o, nel caso di un oggetto attivato da JIT, quando viene disattivato.
-   [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled): viene chiamato ogni volta che un oggetto deve essere restituito al pool generale.

L'implementazione di [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) è facoltativa, ad eccezione degli oggetti transazionali, che devono sempre implementare [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) per monitorare lo stato delle risorse che contengono. Tuttavia, è consigliabile implementare **IObjectControl** nella maggior parte dei casi perché fornisce un modo efficiente per gestire il comportamento di un oggetto in pool, come descritto di seguito.

## <a name="performing-context-specific-initialization"></a>Esecuzione dell'inizializzazione Context-Specific

Utilizzando [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate), è possibile inizializzare l'oggetto nel contesto in cui viene attivato per un determinato client. Per determinare, ad esempio, se l'oggetto ha affinità di transazione (le relative risorse potrebbero essere già integrate), è possibile ottenere l'ID di transazione associato al contesto.

In genere si usa [**Activate**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate)per eseguire l'inizializzazione coerente in tutti i metodi esposti dall'oggetto, considerandola come parte specifica del contesto del costruttore dell'oggetto.

## <a name="cleaning-up-any-client-state"></a>Pulizia di qualsiasi stato del client

Utilizzando [**Disattiva**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate), è possibile eliminare qualsiasi stato specifico del client che potrebbe esistere in modo che l'oggetto torni al pool in uno stato completamente generico e possa quindi essere utilizzato da qualsiasi client senza compromettere la sicurezza o l'isolamento.

## <a name="controlling-reuse-of-the-object"></a>Controllo del riutilizzo dell'oggetto

Utilizzando [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), è possibile monitorare lo stato interno dell'oggetto e segnalare se è adatto per il riutilizzo. Se **CanBePooled** restituisce true e non è stato raggiunto il numero massimo di pool, l'oggetto viene inserito nuovamente nel pool generale. Se **CanBePooled** restituisce false, l'oggetto viene rimosso. Nel caso di componenti transazionali, la restituzione di false causerà la distruzione della transazione corrente.

In genere, si conservano alcuni membri dati globali per l'oggetto e se si rileva una connessione non valida o una risorsa di qualche tipo è in uno stato non valido, impostare questo valore in modo che corrisponda alla situazione corrente e restituirlo tramite [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled).

Se un oggetto non implementa [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled), le istanze continueranno a essere riutilizzate fino a quando non viene raggiunto il livello massimo del pool.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Stringhe del costruttore di oggetti COM+](com--object-constructor-strings.md)
</dt> <dt>

[Funzionamento del pool di oggetti](how-object-pooling-works.md)
</dt> <dt>

[Miglioramento delle prestazioni con il pool di oggetti](improving-performance-with-object-pooling.md)
</dt> <dt>

[Raggruppamento di oggetti transazionali](pooling-transactional-objects.md)
</dt> <dt>

[Requisiti per gli oggetti pool](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



