---
description: Il tipo di icona del tipo semantico è uno dei tipi di formato chiave. Questo tipo è costituito da una chiave nella tabella delle icone fornita dall'utente.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Tipo di icona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a7c90de925ff34977e7ff192dffe0b8614e5734
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308188"
---
# <a name="icon-type"></a>Tipo di icona

Il tipo di icona del [tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md). Questo tipo è costituito da una chiave nella [tabella delle icone](icon-table.md) fornita dall'utente.

Lo strumento di merge deve sostituire un [identificatore](identifier.md) Windows Installer valido per gli elementi di questo tipo. Mergemod.dll non impone questa restrizione ed è attivo lo strumento di merge per assicurarsi che l'utente fornisca una chiave valida nella tabella delle icone.

Null è un valore valido per questo tipo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della [tabella ModuleConfiguration](moduleconfiguration-table.md).

Il tipo binario può essere utilizzato con i tipi di ContextData seguenti.

**ContextData ShortcutIcon**

Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una chiave esterna a una riga nella [tabella delle icone](icon-table.md) che contiene un'immagine adatta per l'utilizzo come icona di collegamento. Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna nome, immettere "1" nella colonna formato, immettere "Icon" nella colonna tipo e immettere "ShorcutIcon" nella colonna ContextData della tabella ModuleConfiguration. Questo tipo non è appropriato per l'utilizzo in una tabella dell'interfaccia utente. Per modificare una chiave nella tabella delle icone in queste tabelle, vedere icona ContextData in [tipo binario](binary-type.md).

 

 



