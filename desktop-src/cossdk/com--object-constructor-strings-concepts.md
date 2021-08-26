---
description: Le stringhe del costruttore di oggetti COM+ sono stringhe di inizializzazione specificate a livello amministrativo per un componente.
ms.assetid: b4915dae-c97c-4d36-95ee-bb10dcb40845
title: Concetti relativi alle stringhe del costruttore di oggetti COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9baef62780950e93043a48c2ccf13910faf7c692dc534f984ffd028e0b342dcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029521"
---
# <a name="com-object-constructor-strings-concepts"></a>Concetti relativi alle stringhe del costruttore di oggetti COM+

Le stringhe del costruttore di oggetti COM+ sono stringhe di inizializzazione specificate a livello amministrativo per un componente. È possibile usare stringhe costruttore di oggetti per scrivere un singolo componente con un grado di generalità che ne consenta la successiva personalizzazione per una determinata attività. in altre informazioni, è possibile eseguire la costruzione di oggetti con parametri.

Ad esempio, è possibile usare questa funzionalità per scrivere un componente che contiene una connessione ODBC generica e successivamente specificare un DSN esatto per il componente a livello amministrativo. Se la configurazione del sistema cambia, è possibile modificare di conseguenza la stringa del costruttore.

> [!Note]  
> Le stringhe del costruttore di oggetti non devono essere usate per archiviare informazioni sensibili alla sicurezza.

 

È possibile usare le stringhe del costruttore di oggetti in combinazione con il [pool di](com--object-pooling.md) oggetti per ottenere un maggiore livello di granularità nel modo in cui si esercitino il pooling e si riutilizzino le risorse. Ad esempio, è possibile creare diversi componenti distinti, identici ad eccezione delle stringhe del costruttore e dei CLSID, per mantenere pool distinti di oggetti che conterranno connessioni utilizzabili da gruppi distinti di client. Ciò sarebbe utile se le connessioni vengono aperte in modo da associarle a ruoli di sicurezza specifici, ad esempio quando le connessioni vengono aperte con un'autenticazione specifica nel database, rendendole non riutilizzabili nel caso generale.

A tale scopo, è possibile scrivere un singolo componente generico che si basa su stringhe del costruttore di oggetti, [**usando IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct), e ricompilarlo per produrre diversi componenti personalizzabili ognuno con un CLSID distinto. È quindi possibile personalizzare a livello amministrativo ogni componente per aprire una connessione appropriata con una stringa del costruttore, configurarli per il pool e verranno mantenuti in pool distinti per OGNI CLSID.

È possibile specificare una stringa costruttore quando un componente è stato scritto in modo specifico per riconoscere la stringa immessa. I componenti possono accedere a queste stringhe a livello di codice [**usando IObjectConstruct**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstruct).

Le stringhe del costruttore vengono passate in fase di creazione dell'oggetto solo quando la costruzione dell'oggetto è abilitata a livello amministrativo. COM+ chiama [**il metodo IObjectConstruct::Construct**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectconstruct-construct) che implementa. All'interno di tale metodo è possibile accedere alla stringa del costruttore usando [**IObjectConstructString**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectconstructstring). Le stringhe vuote possono essere voci valide.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pool di oggetti COM+](com--object-pooling.md)
</dt> <dt>

[Specifica di una stringa del costruttore di oggetti per un componente](specifying-an-object-constructor-string-for-a-component.md)
</dt> <dt>

[Uso di una stringa del costruttore di oggetti per costruire un componente](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



