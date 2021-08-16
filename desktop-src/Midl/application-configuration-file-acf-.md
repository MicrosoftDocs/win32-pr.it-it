---
title: File di configurazione dell'applicazione (ACF)
description: Possono esserci aspetti dell'applicazione distribuita che interessano un componente, ma che non hanno nulla a che fare con un altro.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- ACF MIDL
- Microsoft Interface Definition Language MIDL , descritto, file di configurazione dell'applicazione
- file di configurazione dell'applicazione MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56158267a11125a825442b4db98224d292fdfc309f79cb1562818dee9c08aa23
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808343"
---
# <a name="application-configuration-file-acf"></a>File di configurazione dell'applicazione (ACF)

Possono esserci aspetti dell'applicazione distribuita che interessano un componente, ma che non hanno nulla a che fare con un altro. Ad esempio, un oggetto può contenere una struttura di dati complessa di grandi dimensioni e passare il contenuto di questa struttura di dati a un altro oggetto. Il layout esatto di questa struttura di dati potrebbe non avere significato per l'applicazione ricevente. Inoltre, la struttura può contenere tipi di dati che il compilatore MIDL non riconosce e non può generare il marshalling e l'unmarsciamento del codice.

Le applicazioni client possono condividere la stessa interfaccia ma essere eseguite su piattaforme diverse. è possibile che ognuna di esse necessiti di un proprio set di routine di marshalling. Infine, i singoli client potrebbero non avere sempre bisogno dello stesso set di funzioni. Non è efficiente generare codice stub per le funzioni che non verranno mai implementate in una particolare applicazione client.

Definendo questi aspetti locali dell'interfaccia in un file di configurazione dell'applicazione (ACF), è possibile separare le differenze tra le interfacce client dalla relativa rappresentazione di rete, consentendo al server di inviare e ricevere dati in un formato coerente e rendendo il codice stub più compatto ed efficiente.

La struttura e la sintassi di una definizione di interfaccia ACF sono identiche alla definizione IDL:

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

Per impostazione predefinita, il nome dell'interfaccia ACF deve corrispondere al nome nella definizione IDL. Tuttavia, quando si usa l'opzione del compilatore [**MIDL/acf**](-acf.md) per specificare in modo esplicito un nome di file ACF, non è necessario che i nomi di interfaccia corrispondano. Questa funzionalità consente a diverse interfacce di condividere una singola specifica ACF.

 

 




