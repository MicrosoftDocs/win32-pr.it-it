---
description: In COM+, lo stato temporaneo condiviso per gli oggetti viene gestito tramite gestione proprietà condivise . SPM è un dispenser di risorse che è possibile usare per condividere lo stato tra più oggetti all'interno di un processo server.
ms.assetid: 31b50c2a-68b5-4816-9a56-8cd9475e7beb
title: Concetti relativi all'Gestione proprietà COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9ce190cb4f4e65e6ab5208dd2adec08f807d4f6d29d4cf99a3e70a1c0a7004
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129013"
---
# <a name="com-shared-property-manager-concepts"></a>Concetti relativi all'Gestione proprietà COM+

In COM+, lo stato temporaneo condiviso per gli oggetti viene gestito tramite gestione proprietà condivise . SPM è un dispenser di risorse che è possibile usare per condividere lo stato tra più oggetti all'interno di un processo server.

Non è possibile usare variabili globali in un ambiente distribuito a causa di problemi di concorrenza e conflitti di nomi. Il gestore delle proprietà condivise elimina i conflitti di nome fornendo gruppi di proprietà condivise, che stabiliscono spazi dei nomi univoci per le proprietà condivise che contengono. SPM implementa anche blocchi e semafori per proteggere le proprietà condivise dall'accesso simultaneo, con la possibilità di perdere gli aggiornamenti e lasciare le proprietà in uno stato imprevedibile.

> [!Note]  
> Lo stato temporaneo condiviso è un'informazione sullo stato mantenuta in memoria che non è in grado di superare gli errori di sistema. Le informazioni sono progettate per essere condivise da più oggetti tra più limiti di transazione (ma non tra processi).

 

Le proprietà condivise archiviate in SPM sono disponibili solo per gli oggetti in esecuzione nello stesso processo. Ciò significa che gli oggetti che useranno SPM per archiviare i valori e che dovranno avere accesso a questi valori devono essere installati come parte della stessa applicazione COM+. Gli amministratori di sistema possono spostare classi COM+ da un pacchetto a un altro dopo la distribuzione dell'applicazione COM+. Se si basano su più oggetti che condividono proprietà tramite SPM, è necessario documentare chiaramente che devono essere installati nella stessa applicazione COM+.

È anche importante che i componenti che condividono le proprietà abbia lo stesso attributo di attivazione. Se due componenti nello stesso pacchetto hanno attributi di attivazione diversi, in genere non saranno in grado di condividere le proprietà. Ad esempio, se un componente è configurato per l'esecuzione in un processo client e l'altro è configurato per l'esecuzione in un processo server, i relativi oggetti verranno in genere eseguiti in processi diversi anche se si trovano nello stesso pacchetto.

È sempre consigliabile creare un'istanza degli oggetti [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md), [**SharedPropertyGroup**](sharedpropertygroup.md)e [**SharedProperty**](sharedproperty.md) da componenti COM+ anziché da un client di base. Se un client di base crea proprietà e gruppi di proprietà condivise, le proprietà condivise si trova all'interno del processo client di base, non in un processo server. Ciò significa che gli oggetti COM+ non possono condividere le proprietà a meno che gli oggetti non siano anche in esecuzione nel processo client (che in genere non è una buona idea).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Com+ Shared Gestione proprietà](com--shared-property-manager.md)
</dt> <dt>

[Gruppi di proprietà condivise](shared-property-groups.md)
</dt> </dl>

 

 



