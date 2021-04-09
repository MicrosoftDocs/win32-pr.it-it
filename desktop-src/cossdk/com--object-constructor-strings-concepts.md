---
description: Le stringhe del costruttore di oggetti COM+ sono stringhe di inizializzazione che vengono specificate in maniera amministrativa per un componente.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Concetti relativi alle stringhe del costruttore di oggetti COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c32bffd35ad230efe1f22b52da10e1b4910d71da
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966028"
---
# <a name="com-object-constructor-strings-concepts"></a>Concetti relativi alle stringhe del costruttore di oggetti COM+

Le stringhe del costruttore di oggetti COM+ sono stringhe di inizializzazione che vengono specificate in maniera amministrativa per un componente. È possibile usare le stringhe del costruttore di oggetti per scrivere un singolo componente con un grado di generalizzazione che ne consente la personalizzazione in un secondo momento per una determinata attività. ovvero, è possibile eseguire la costruzione di oggetti con parametri.

È ad esempio possibile utilizzare questa funzionalità per scrivere un componente che include una connessione ODBC generica e successivamente specificare un DSN esatto per il componente in modo amministrativo. Se la configurazione del sistema viene modificata, è possibile modificare di conseguenza la stringa del costruttore.

> [!Note]  
> Le stringhe del costruttore di oggetti non devono essere usate per archiviare informazioni sensibili alla sicurezza.

 

È possibile utilizzare le stringhe del costruttore di oggetti insieme al [pool di oggetti](com--object-pooling.md) per ottenere un livello maggiore di granularità nella modalità di raggruppamento e riutilizzo delle risorse. È possibile, ad esempio, creare diversi componenti distinti, ad eccezione delle stringhe del costruttore e dei CLSID, per mantenere pool distinti di oggetti che contengano connessioni utilizzabili da gruppi distinti di client. Questa operazione è utile se le connessioni vengono aperte in modo da associarle a specifici ruoli di sicurezza, ad esempio quando le connessioni vengono aperte con un'autenticazione specifica nel database, rendendole non riutilizzabile nel caso generale.

A tale scopo, è possibile scrivere un singolo componente generico che si basa sulle stringhe del costruttore di oggetti, usando [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), e ricompilarlo per produrre diversi componenti personalizzabili ciascuno con un CLSID distinto. È quindi possibile personalizzare in modo amministrativo ogni componente per aprire una connessione appropriata con una stringa del costruttore, configurarli per il pool e mantenerli in pool distinti per CLSID.

È possibile specificare una stringa del costruttore quando un componente è stato scritto in modo specifico per riconoscere la stringa immessa. I componenti possono accedere a queste stringhe a livello di codice usando [**IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).

Le stringhe del costruttore vengono passate in fase di creazione dell'oggetto solo quando la costruzione di oggetti è abilitata in un punto amministrativo. COM+ chiama il metodo [**IObjectConstruct:: Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) che implementa. All'interno di questo metodo, è possibile accedere alla stringa del costruttore usando [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring). Le stringhe vuote possono essere voci valide.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pool di oggetti COM+](com--object-pooling.md)
</dt> <dt>

[Specifica di una stringa del costruttore di oggetti per un componente](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[Uso di una stringa del costruttore di oggetti per costruire un componente](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



