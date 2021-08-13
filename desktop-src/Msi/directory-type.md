---
description: Tipo di directory di tipo semantico è uno dei tipi di formato chiave, costituito da una chiave esterna nella tabella Directory fornita dall'utente.
ms.assetid: b5a0ed38-1dda-4c33-9429-0cbe87e13aef
title: Tipo di directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c784ea91ceb9baaeb2c97883cace0266a146d80634ec07f5e25f0b01ac057c7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119251801"
---
# <a name="directory-type"></a>Tipo di directory

Tipo di directory di [tipo semantico](semantic-types.md) è uno dei tipi di formato chiave [,](key-format-types.md)costituito da una chiave esterna nella tabella [Directory](directory-table.md) fornita dall'utente.

Lo strumento di merge deve sostituire un identificatore Windows [installer valido](identifier.md) per gli elementi di questo tipo. Mergemod.dll non applica questa restrizione ed è lo strumento di unione a garantire che l'utente fornisce una chiave valida nella tabella Directory.

Un elemento configurabile di tipo Directory deve modificare solo la directory di destinazione dell'installazione e non l'immagine di origine. Un elemento configurabile di questo tipo deve pertanto modificare solo le chiavi esterne nella tabella Directory e non modificare direttamente la tabella Directory.

Poiché la colonna Directory della tabella Component non ammette valori Null, null è un valore non valido per un elemento configurabile di questo tipo anche se \_ msmConfigItemNonNullable non è impostato nella colonna Attributes. [](component-table.md)

Il tipo Directory può essere usato con due tipi di ContextData.

**IsolationDirectory ContextData**

Un modulo unione configurabile può usare questo tipo per consentire all'utente di fornire una directory di destinazione per i file nel modulo. Lo strumento di merge sostituisce l'identificatore della directory nei modelli nella colonna Value della [tabella ModuleSubstitution](modulesubstitution-table.md). Per specificare un elemento configurabile di questo tipo, gli autori di moduli devono immettere il nome della directory nella colonna Nome, immettere "1" nella colonna Formato, immettere "Directory" nella colonna Tipo e immettere "IsolationDirectory" nella colonna ContextData della tabella [ModuleConfiguration](moduleconfiguration-table.md).

**ShortcutLocation ContextData**

Un modulo unione configurabile può usare questo tipo per consentire all'utente di fornire una directory di destinazione per i collegamenti nel modulo. Lo strumento di unione sostituisce l'identificatore del collegamento nei modelli nella colonna Valore della [tabella ModuleSubstitution](modulesubstitution-table.md). Per specificare un elemento configurabile di questo tipo, gli autori di moduli devono immettere il nome della directory nella colonna Nome, immettere "1" nella colonna Formato, immettere "Directory" nella colonna Tipo e immettere "ShortcutLocation" nella colonna ContextData della tabella [ModuleConfiguration](moduleconfiguration-table.md).

 

 



