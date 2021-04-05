---
title: Architettura delle interfacce del servizio Active Directory
description: Molti servizi directory sono gerarchici e quindi si prestano a un modello a oggetti gerarchico. In questa sezione vengono utilizzate le rappresentazioni di oggetti COM per illustrare diverse funzionalità ADSI.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Active Directory architettura di interfacce di servizio ADSI
- ADSI ADSI, informazioni su, architettura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59d8d6281aa99bd96efa38166ef658972a5f54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707495"
---
# <a name="active-directory-service-interfaces-architecture"></a>Architettura delle interfacce del servizio Active Directory

Molti servizi directory sono gerarchici e quindi si prestano a un modello a oggetti gerarchico. In questa sezione vengono utilizzate le rappresentazioni di oggetti COM per illustrare diverse funzionalità ADSI.

Nella figura seguente del modello a oggetti, un oggetto di sistema di primo livello contiene un oggetto spazio dei nomi per ogni provider ADSI installato.

![oggetto contenitore spazi dei nomi](images/ds2top.png)

Ogni oggetto spazio dei nomi è a sua volta un contenitore che contiene i nodi radice di primo livello di ogni server, dominio o qualsiasi altro tipo di oggetti di sistema di directory definito come radice in ogni servizio directory.

ADSI fornisce un set di oggetti e interfacce predefiniti che consentono alle applicazioni client di interagire con i servizi di directory utilizzando un set uniforme di metodi. Tuttavia, ADSI potrebbe non consentire l'accesso a tutte le funzionalità di un servizio directory. Per utilizzare al meglio il set completo di funzionalità di ogni servizio directory, ADSI fornisce un modello di schema che i provider di servizi di directory e i fornitori di software di terze parti possono utilizzare per estendere le funzionalità oltre le interfacce fornite in ADSI.

Gli oggetti contenitore del nodo radice, disponibili all'interno di ogni oggetto spazio dei nomi del provider, includono un oggetto contenitore dello schema ADSI. Questo oggetto contiene la definizione di tutte le funzionalità per quel provider. Per altre informazioni, vedere [modello di schema ADSI](adsi-schema-model.md).

Questa sezione include gli argomenti seguenti:

-   [Oggetti interfacce del servizio Active Directory](active-directory-service-interfaces-objects.md)
-   [Namespaces](namespaces.md) (Spazi dei nomi)
-   [Provider di interfacce del servizio Active Directory](active-directory-service-interfaces-provider.md)
-   [Modello di schema ADSI](adsi-schema-model.md)

 

 




