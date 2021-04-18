---
title: File di configurazione dell'applicazione (ACF)
description: Potrebbero esserci aspetti dell'applicazione distribuita che interessano un componente, ma non hanno nulla a che fare con un altro componente.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- MIDL DI ACF
- Microsoft Interface Definition Language MIDL, descritto, file di configurazione dell'applicazione
- file di configurazione dell'applicazione MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9066e5641d6b71e68ba670984765661f1b9f6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298671"
---
# <a name="application-configuration-file-acf"></a>File di configurazione dell'applicazione (ACF)

Potrebbero esserci aspetti dell'applicazione distribuita che interessano un componente, ma non hanno nulla a che fare con un altro componente. Ad esempio, un oggetto può contenere una struttura di dati complessa e di grandi dimensioni e passare il contenuto di questa struttura di dati a un altro oggetto. Il layout esatto di questa struttura di dati potrebbe non essere significativo per l'applicazione ricevente. Inoltre, la struttura può contenere tipi di dati che il compilatore MIDL non riconosce e non può generare codice di marshalling e di unmarshalling.

Le applicazioni client possono condividere la stessa interfaccia ma possono essere eseguite su piattaforme diverse; ognuno può avere bisogno di un proprio set di routine di marshalling. Infine, i singoli client potrebbero non avere sempre lo stesso set di funzioni. Non è efficiente generare codice stub per le funzioni che non verranno mai implementate in un'applicazione client specifica.

Definendo questi aspetti locali dell'interfaccia in un file di configurazione dell'applicazione (ACF), è possibile separare le differenze tra le interfacce client dalla relativa rappresentazione di rete, consentendo al server di inviare e ricevere dati in un formato coerente, rendendo il codice stub più compatto ed efficiente.

La struttura e la sintassi di una definizione di interfaccia ACF sono identiche alla definizione IDL:

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

Per impostazione predefinita, il nome dell'interfaccia ACF deve corrispondere al nome nella definizione IDL. Tuttavia, quando si usa l'opzione del compilatore MIDL/ [**ACF**](-acf.md) per specificare in modo esplicito un nome di file ACF, non è necessario che i nomi di interfaccia corrispondano. Questa funzionalità consente a diverse interfacce di condividere una singola specifica ACF.

 

 




