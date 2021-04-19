---
description: I componenti transazionali che devono essere raggruppati hanno requisiti particolari.
ms.assetid: 32e2f830-c30a-4dbc-8e69-dd2038851998
title: Raggruppamento di oggetti transazionali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 006ba32ad2ac550be4fa4418dde322ded26c64c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304945"
---
# <a name="pooling-transactional-objects"></a>Raggruppamento di oggetti transazionali

I componenti transazionali che devono essere raggruppati hanno requisiti particolari.

## <a name="manually-enlisting-resources"></a>Integrazione manuale delle risorse

Gli oggetti pool che fanno parte delle transazioni devono integrare manualmente le risorse gestite. Se un oggetto contiene risorse gestite tra client, non sarà possibile eseguire automaticamente l'integrazione di Resource Manager in una transazione quando l'oggetto viene attivato in un determinato contesto.

L'oggetto stesso deve gestire la logica di rilevamento della transazione, la disattivazione dell'integrazione automatica di Resource Manager e l'integrazione manuale di tutte le risorse che possiede. I passaggi per eseguire questa operazione sono specifici del gestore di risorse in uso. Se è necessario eseguire l'integrazione manuale, consultare la documentazione relativa a Resource Manager.

Come descritto di seguito, gli oggetti possono essere raggruppati con affinità di transazione mentre una transazione è attiva e può essere attivata con affinità di transazione se viene chiamata da un client associato a tale transazione. Prima di eseguire l'integrazione delle risorse, è innanzitutto necessario controllare l'affinità di transazione. Se l'oggetto è stato ricavato dal pool specifico di tale transazione, è già stato eseguito il lavoro in tale transazione ed è stata integrata la relativa risorsa.

## <a name="turning-off-automatic-enlistment"></a>Disattivazione dell'integrazione automatica

L'integrazione automatica deve essere disattivata dopo l'acquisizione della risorsa, in genere nel costruttore dell'oggetto. Ovvero si disabilita l'integrazione automatica e quindi si effettua la connessione.

La disabilitazione dell'integrazione automatica può talvolta essere una procedura delicata, in particolare nel caso di provider di accesso ai dati a più livelli. L'integrazione automatica viene talvolta abbinata al pool di connessioni, come con ODBC e talvolta non come con OLE DB. Potrebbe essere necessario assicurarsi che l'inserimento automatico sia disattivato a diversi livelli di provider.

## <a name="implementing-iobjectcontrol"></a>Implementazione di IObjectControl

Gli oggetti che fanno parte di un pool che partecipano alle transazioni devono monitorare lo stato corrente delle risorse che contengono. Se l'oggetto rileva che si trova in uno stato non riutilizzabile, ad esempio se una connessione non è valida, deve restituire false per [**IObjectControl:: CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled). Questo avrà l'effetto di rimuovere l'istanza dell'oggetto e di destinarla alla transazione corrente.

## <a name="transaction-specific-pools"></a>Pool di Transaction-Specific

Un pool di oggetti è in genere omogeneo e qualsiasi oggetto in pool non attualmente in uso è utile per tornare a qualsiasi client. L'unica eccezione a questa regola è nel caso degli oggetti transazionali, per cui è ottimizzato il pool di oggetti. Quando il client che richiede un oggetto ha una transazione associata, COM+ analizzerà il pool per un oggetto disponibile già associato a tale transazione. Se viene trovato un oggetto con affinità di transazione, quest'operazione viene restituita al client. in caso contrario, viene restituito un oggetto dal pool generale.

In questo modo, i pool speciali vengono mantenuti contenenti oggetti con affinità per una determinata transazione. Quando viene eseguito il commit o l'interruzione della transazione, questi oggetti vengono restituiti al pool generale senza affinità di transazione, pronti per l'utilizzo da parte di qualsiasi client.

Per questo motivo, quando il componente integra manualmente le risorse gestite in una transazione, deve prima verificare se sono già integrate. In tal caso, non è necessario eseguire l'integrazione.

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

[Requisiti per gli oggetti pool](requirements-for-poolable-objects.md)
</dt> </dl>

 

 



