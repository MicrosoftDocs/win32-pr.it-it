---
title: Estensioni dello schema
description: L'architettura dello schema ADSI fornisce che le nuove classi dello schema possono essere aggiunte al contenitore della classe dello schema e nuove proprietà a un oggetto della classe di schema esistente in fase di esecuzione.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b86491966e2bfddbef72d68d7a96869448c38188
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104116673"
---
# <a name="schema-extensions"></a>Estensioni dello schema

L'architettura dello schema ADSI fornisce che le nuove classi dello schema possono essere aggiunte al contenitore della classe dello schema e nuove proprietà a un oggetto della classe di schema esistente in fase di esecuzione. La seconda possibilità non richiede alcun nuovo codice. Si tratta di una funzionalità importante per gli spazi dei nomi che consentono Extensible Directory Services. Il componente provider deve consentire questa estendibilità e stabilire dove accedere e archiviare l'istanza della classe e i valori delle relative proprietà. In un tipico servizio directory estendibile, queste informazioni vengono archiviate nel database del servizio directory in modo analogo a qualsiasi altra definizione di classe e proprietà dello schema.

> [!Note]  
> Nella terminologia dell'interfaccia COM, solo le proprietà possono essere aggiunte a una classe di schema esistente, non a metodi. L'aggiunta di un nuovo metodo richiederebbe l'aggiunta di una nuova implementazione del metodo e richiederebbe quindi altro codice.

 

Per un esempio di uno schema del provider specifico, vedere [gestione degli schemi](schema-management.md).

 

 




