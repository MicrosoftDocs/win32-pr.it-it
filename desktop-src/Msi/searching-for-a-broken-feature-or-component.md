---
description: Il programma di installazione può aumentare la resilienza dell'applicazione reinstallando automaticamente i componenti danneggiati.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Ricerca di una funzionalità o di un componente danneggiato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398d084a543ee4c9491242faa287c60d83a5f7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232065"
---
# <a name="searching-for-a-broken-feature-or-component"></a>Ricerca di una funzionalità o di un componente danneggiato

Il programma di installazione può aumentare la [resilienza](resiliency.md) dell'applicazione reinstallando automaticamente i componenti danneggiati. In particolare, il programma di installazione Reinstalla un componente o una funzionalità se rileva che il file o la chiave del registro di sistema specificata nella colonna percorso chiave della [tabella dei componenti](component-table.md) è mancante.

Se il percorso di tasto del componente di una funzionalità è danneggiato nell'origine o se si verifica un errore nel modo in cui viene creato il tasto di scelta rapida nel database, il programma di installazione può tentare di aprire un pacchetto di installazione e reinstallare la funzionalità ogni volta che viene attivato il collegamento della funzionalità.

Per determinare la provocazione di tentativi ripetuti di reinstallare una funzionalità o un'applicazione, controllare nel registro eventi la presenza di due voci come la seguente.

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

Il primo messaggio indica quale componente del pacchetto del prodotto è stato installato. Si tratta del componente a cui si fa riferimento nella \_ colonna componente della [tabella dei collegamenti](shortcut-table.md).

Il secondo messaggio indica quale componente non riesce a rilevare. Si tratta del componente con il percorso della finestra di avvio della reinstallazione mancante o danneggiato.

 

 



