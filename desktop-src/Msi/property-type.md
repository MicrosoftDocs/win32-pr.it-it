---
description: Il tipo di proprietà di tipo semantico è uno dei tipi di formato chiave. Questo tipo è costituito da una chiave esterna nella tabella Property fornita dall'utente.
ms.assetid: 819e4e90-0bc3-41ba-851d-1d4c52b6eeea
title: Tipo di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6446b5a0ef5f2cf1bc969f531a3b8c35e6990a2ca3eee3c0002e4f62fbf4cea9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145334"
---
# <a name="property-type"></a>Tipo di proprietà

Il tipo di proprietà di [tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md). Questo tipo è costituito da una chiave esterna nella [tabella Property](property-table.md) fornita dall'utente.

Lo strumento di merge deve sostituire un identificatore Windows installer [valido](identifier.md) per gli elementi di questo tipo. Mergemod.dll non applica questa restrizione ed è lo strumento di unione a garantire che l'utente fornisce una chiave valida nella tabella Property. Le chiavi primarie della tabella Property sono i nomi delle proprietà.

Null è un valore valido per questo tipo a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributi della [tabella ModuleConfiguration](moduleconfiguration-table.md).

Il tipo Property può essere usato con i tipi di ContextData seguenti.

**Null ContextData**

Un modulo unione configurabile può usare questo tipo per consentire all'utente di fornire un nome di proprietà a una tabella di database nel modulo. Lo strumento di unione sostituisce l'identificatore della proprietà nei modelli nella colonna Value della [tabella ModuleSubstitution](modulesubstitution-table.md). Per specificare un elemento configurabile di questo tipo, gli autori del modulo devono immettere il nome dell'elemento configurabile nella colonna Nome, immettere "1" nella colonna Formato, immettere "Proprietà" nella colonna Tipo e lasciare vuota la colonna ContextData della tabella [ModuleConfiguration](moduleconfiguration-table.md).

**Public ContextData**

Un modulo unione configurabile può usare questo tipo per consentire all'utente di fornire il nome di una proprietà pubblica [a](public-properties.md) una tabella di database nel modulo. Lo strumento di unione sostituisce l'identificatore della proprietà nei modelli nella colonna Value della [tabella ModuleSubstitution](modulesubstitution-table.md). Per specificare un elemento configurabile di questo tipo, gli autori del modulo devono immettere il nome dell'elemento configurabile nella colonna Nome, immettere "1" nella colonna Formato, immettere "Proprietà" nella colonna Tipo e immettere "Public" nella colonna ContextData della tabella ModuleConfiguration.

**Private ContextData**

Un modulo unione configurabile può usare questo tipo per consentire all'utente di fornire il nome di una [proprietà](private-properties.md) privata a una tabella di database nel modulo. Lo strumento di unione sostituisce l'identificatore della proprietà nei modelli nella colonna Value della [tabella ModuleSubstitution](modulesubstitution-table.md). Per specificare un elemento configurabile di questo tipo, gli autori di moduli devono immettere il nome dell'elemento configurabile nella colonna Nome, immettere "1" nella colonna Formato, immettere "Proprietà" nella colonna Tipo e immettere "Private" nella colonna ContextData della tabella ModuleConfiguration.

 

 



