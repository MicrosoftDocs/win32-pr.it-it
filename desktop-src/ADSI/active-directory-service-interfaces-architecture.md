---
title: Architettura delle interfacce del servizio Active Directory
description: Molti servizi directory sono gerarchici e quindi si prestano a un modello a oggetti gerarchico. In questa sezione vengono utilizzate rappresentazioni di oggetti COM per illustrare varie funzionalità di ADSI.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Architettura delle interfacce del servizio Active Directory ADSI
- ADSI ADSI , informazioni su, architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41afbc212edbea6491de4cae89f2c8b7c873019b6d5678c5bf1d5b531f519260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024085"
---
# <a name="active-directory-service-interfaces-architecture"></a>Architettura delle interfacce del servizio Active Directory

Molti servizi directory sono gerarchici e quindi si prestano a un modello a oggetti gerarchico. In questa sezione vengono utilizzate rappresentazioni di oggetti COM per illustrare varie funzionalità di ADSI.

Nella figura del modello a oggetti seguente un oggetto di sistema di primo livello contiene un oggetto Namespace per ogni provider ADSI installato.

![oggetto contenitore namespaces](images/ds2top.png)

Ogni oggetto Spazio dei nomi è a sua volta un contenitore che contiene i nodi radice di primo livello di ogni server, dominio o qualsiasi altro tipo di oggetti del sistema di directory definito come radici in ogni servizio directory.

ADSI fornisce un set di oggetti e interfacce predefiniti in modo che le applicazioni client possano interagire con i servizi directory usando un set uniforme di metodi. Ad ogni modo, ADSI potrebbe non fornire l'accesso a tutte le funzionalità di un servizio directory. Per usare al meglio il set completo di funzionalità di ogni servizio directory, ADSI fornisce un modello di schema che i provider di servizi directory e i fornitori di software di terze parti possono usare per estendere le funzionalità oltre le interfacce fornite in ADSI.

Gli oggetti contenitore del nodo radice, disponibili all'interno di ogni oggetto Namespace del provider, includono un oggetto contenitore dello schema ADSI. Questo oggetto contiene la definizione di tutte le funzionalità per tale provider. Per altre informazioni, vedere [Modello di schema ADSI.](adsi-schema-model.md)

Questa sezione include gli argomenti seguenti:

-   [Oggetti delle interfacce del servizio Active Directory](active-directory-service-interfaces-objects.md)
-   [Namespaces](namespaces.md) (Spazi dei nomi)
-   [Provider di interfacce del servizio Active Directory](active-directory-service-interfaces-provider.md)
-   [Modello di schema ADSI](adsi-schema-model.md)

 

 




