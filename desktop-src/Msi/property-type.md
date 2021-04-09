---
description: Il tipo di proprietà di tipo semantico è uno dei tipi di formato chiave. Questo tipo è costituito da una chiave esterna nella tabella delle proprietà fornita dall'utente.
ms.assetid: 819e4e90-0bc3-41ba-851d-1d4c52b6eeea
title: Tipo di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36236c78160abbfe3ad64c6b801a3cdbdbb98b48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049992"
---
# <a name="property-type"></a>Tipo di proprietà

Il tipo di proprietà di [tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md). Questo tipo è costituito da una chiave esterna nella [tabella delle proprietà](property-table.md) fornita dall'utente.

Lo strumento di merge deve sostituire un [identificatore](identifier.md) Windows Installer valido per gli elementi di questo tipo. Mergemod.dll non impone questa restrizione ed è attivo lo strumento di merge per assicurarsi che l'utente fornisca una chiave valida nella tabella delle proprietà. Le chiavi primarie della tabella delle proprietà sono i nomi delle proprietà.

Null è un valore valido per questo tipo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della [tabella ModuleConfiguration](moduleconfiguration-table.md).

Il tipo di proprietà può essere utilizzato con i tipi di ContextData seguenti.

**ContextData null**

Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire un nome di proprietà a una tabella di database nel modulo. Lo strumento di merge sostituisce l'identificatore della proprietà nei modelli della colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md). Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna nome, immettere "1" nella colonna formato, immettere "Property" nella colonna tipo e lasciare vuota la colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md).

**ContextData pubblico**

Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire il nome di una [proprietà pubblica](public-properties.md) a una tabella di database del modulo. Lo strumento di merge sostituisce l'identificatore della proprietà nei modelli della colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md). Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna nome, immettere "1" nella colonna formato, immettere "Property" nella colonna tipo e immettere "public" nella colonna ContextData della tabella ModuleConfiguration.

**ContextData privato**

Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire il nome di una [proprietà privata](private-properties.md) a una tabella di database del modulo. Lo strumento di merge sostituisce l'identificatore della proprietà nei modelli della colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md). Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna nome, immettere "1" nella colonna formato, immettere "Property" nella colonna tipo e immettere "private" nella colonna ContextData della tabella ModuleConfiguration.

 

 



