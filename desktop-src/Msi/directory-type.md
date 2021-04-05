---
description: Il tipo di directory di tipo semantico è uno dei tipi di formato chiave, costituito da una chiave esterna nella tabella di directory fornita dall'utente.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Tipo di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e3ba336dd5de7cd45ef9215f0397ba51ce544d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882981"
---
# <a name="directory-type"></a>Tipo di directory

Il tipo di directory di [tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md), costituito da una chiave esterna nella tabella di [directory](directory-table.md) fornita dall'utente.

Lo strumento di merge deve sostituire un [identificatore](identifier.md) Windows Installer valido per gli elementi di questo tipo. Mergemod.dll non impone questa restrizione ed è attivo lo strumento di merge per assicurarsi che l'utente fornisca una chiave valida nella tabella di directory.

Un elemento configurabile del tipo di directory deve modificare solo la directory di destinazione dell'installazione e non modificare l'immagine di origine. Un elemento configurabile di questo tipo deve pertanto modificare solo le chiavi esterne nella tabella di directory senza modificare direttamente la tabella di directory.

Poiché la \_ colonna di directory della [tabella dei componenti](component-table.md) è non nullable, null è un valore non valido per un elemento configurabile di questo tipo anche se msmConfigItemNonNullable non è impostato nella colonna Attributes.

Il tipo di directory può essere usato con due tipi di ContextData.

**ContextData IsolationDirectory**

Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una directory di destinazione per i file del modulo. Lo strumento di merge sostituisce l'identificatore della directory nei modelli della colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md). Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della directory nella colonna nome, immettere "1" nella colonna formato, immettere "directory" nella colonna tipo e immettere "IsolationDirectory" nella colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md).

**ContextData ShortcutLocation**

Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una directory di destinazione per i collegamenti nel modulo. Lo strumento di merge sostituisce l'identificatore del collegamento nei modelli della colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md). Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della directory nella colonna nome, immettere "1" nella colonna formato, immettere "directory" nella colonna tipo e immettere "ShortcutLocation" nella colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md).

 

 



