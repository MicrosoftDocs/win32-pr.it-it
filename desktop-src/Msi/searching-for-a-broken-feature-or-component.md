---
description: Il programma di installazione può aumentare la resilienza dell'applicazione reinstallando automaticamente i componenti danneggiati.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Ricerca di una funzionalità o di un componente interrotto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa17fc66fdf0bda0a04df9a5917d4e79671b32f453ead921d4f43f89bbd47dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041241"
---
# <a name="searching-for-a-broken-feature-or-component"></a>Ricerca di una funzionalità o di un componente interrotto

Il programma di installazione può aumentare [la resilienza dell'applicazione](resiliency.md) reinstallando automaticamente i componenti danneggiati. In particolare, il programma di installazione reinstalla un componente o una funzionalità se rileva che manca il file o la chiave del Registro di sistema specificata nella colonna KeyPath della tabella [Component.](component-table.md)

Se il KeyPath del componente di una funzionalità è danneggiato nell'origine o se si verifica un errore nella modalità di creazione di KeyPath nel database, il programma di installazione può tentare di aprire un pacchetto di installazione e reinstallare la funzionalità ogni volta che viene attivato il collegamento della funzionalità.

Per determinare la causa di ripetuti tentativi di reinstallare una funzionalità o un'applicazione, controllare il registro eventi per due voci, ad esempio le seguenti.

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

Il primo messaggio indica quale componente nel pacchetto del prodotto è stato installato. Si tratta del componente a cui viene fatto riferimento nella colonna \_ Componente della tabella [Collegamento](shortcut-table.md).

Il secondo messaggio indica quale componente non riesce a rilevare. Si tratta del componente con keyPath mancante o danneggiato che attiva la reinstallazione.

 

 



