---
title: Estensioni dello schema
description: L'architettura dello schema ADSI consente di aggiungere nuove classi dello schema al contenitore di classi dello schema e nuove proprietà a un oggetto classe dello schema esistente in fase di esecuzione.
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c7fdc4b363fea83029fc5526464bd5825fa851dbe82e874911a0ab45d869843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118178820"
---
# <a name="schema-extensions"></a>Estensioni dello schema

L'architettura dello schema ADSI consente di aggiungere nuove classi dello schema al contenitore di classi dello schema e nuove proprietà a un oggetto classe dello schema esistente in fase di esecuzione. Quest'ultima capacità non richiede nuovo codice. Si tratta di una funzionalità importante per gli spazi dei nomi che consentono servizi directory estendibili. Il componente provider deve consentire questa estendibilità e sapere dove accedere e archiviare l'istanza della classe e i valori delle relative proprietà. In un tipico servizio directory estendibile queste informazioni vengono archiviate nel database del servizio directory allo stesso modo di qualsiasi altra definizione di classe e proprietà dello schema.

> [!Note]  
> Nella terminologia dell'interfaccia COM è possibile aggiungere solo proprietà a una classe di schema esistente, non ai metodi. L'aggiunta di un nuovo metodo richiederebbe l'aggiunta di una nuova implementazione di tale metodo e quindi richiederebbe codice aggiuntivo.

 

Per un esempio di uno schema del provider specifico, vedere [Gestione dello schema.](schema-management.md)

 

 




