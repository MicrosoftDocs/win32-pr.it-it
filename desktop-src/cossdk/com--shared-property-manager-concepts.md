---
description: In COM+ lo stato temporaneo condiviso per gli oggetti viene gestito tramite Gestione proprietà condivise (SPM). SPM è un dispenser di risorse che è possibile usare per condividere lo stato tra più oggetti all'interno di un processo server.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Concetti di Gestione proprietà condivisi COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be55c4a83aa363c911564aefabbe1d85f3804fb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305146"
---
# <a name="com-shared-property-manager-concepts"></a>Concetti di Gestione proprietà condivisi COM+

In COM+ lo stato temporaneo condiviso per gli oggetti viene gestito tramite Gestione proprietà condivise (SPM). SPM è un dispenser di risorse che è possibile usare per condividere lo stato tra più oggetti all'interno di un processo server.

Non è possibile usare le variabili globali in un ambiente distribuito a causa di problemi di concorrenza e conflitti di nomi. Il gestore delle proprietà condivise Elimina i conflitti di nomi fornendo gruppi di proprietà condivisi, che definiscono spazi dei nomi univoci per le proprietà condivise che contengono. Il SPM implementa anche i blocchi e i semafori per proteggere le proprietà condivise dall'accesso simultaneo, che può comportare la perdita di aggiornamenti e lasciare le proprietà in uno stato imprevedibile.

> [!Note]  
> Lo stato temporaneo condiviso è quello di informazioni sullo stato mantenute in memoria che non sopravvivono a errori di sistema. Le informazioni sono progettate per essere condivise da più oggetti oltre i limiti delle transazioni, ma non tra più processi.

 

Le proprietà condivise archiviate in SPM sono disponibili solo per gli oggetti in esecuzione nello stesso processo. Ciò significa che gli oggetti che utilizzeranno la funzione SPM per archiviare i valori e che dovranno avere accesso a questi valori devono essere installati come parte della stessa applicazione COM+. È possibile che gli amministratori di sistema sposti le classi COM+ da un pacchetto a un altro dopo che l'applicazione COM+ è stata distribuita. Se si fa affidamento su diversi oggetti che condividono le proprietà tramite il SPM, è necessario documentare chiaramente che devono essere installati nella stessa applicazione COM+.

È anche importante per i componenti che condividono le proprietà con lo stesso attributo di attivazione. Se due componenti nello stesso pacchetto hanno attributi di attivazione diversi, in genere non saranno in grado di condividere le proprietà. Se, ad esempio, un componente è configurato per l'esecuzione in un processo client e l'altro è configurato per essere eseguito in un processo server, i relativi oggetti vengono in genere eseguiti in processi diversi anche se si trovano nello stesso pacchetto.

È sempre necessario creare istanze degli oggetti [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md)e [**SharedProperty**](sharedproperty.md) dai componenti com+ anziché da un client di base. Se un client di base crea proprietà e gruppi di proprietà condivisi, le proprietà condivise si trovano all'interno del processo client di base, non in un processo server. Ciò significa che gli oggetti COM+ non possono condividere le proprietà, a meno che gli oggetti non siano in esecuzione anche nel processo client (che in genere non è un'idea consigliata).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione proprietà condivise COM+](com--shared-property-manager.md)
</dt> <dt>

[Gruppi di proprietà condivise](shared-property-groups.md)
</dt> </dl>

 

 



