---
description: Il tipo di finestra di dialogo di tipo semantico è uno dei tipi di formato chiave. Questo tipo è costituito da una chiave esterna nella tabella della finestra di dialogo fornita dall'utente.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Tipo di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ed04dece5702d232f252caa7c0ee02e7576246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314281"
---
# <a name="dialog-type"></a>Tipo di dialogo

Il tipo di finestra di dialogo di [tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md). Questo tipo è costituito da una chiave esterna nella [tabella della finestra di dialogo](dialog-table.md) fornita dall'utente.

Lo strumento di merge deve sostituire un [identificatore](identifier.md) Windows Installer valido per gli elementi di questo tipo. Mergemod.dll non impone questa restrizione ed è attivo lo strumento di merge per assicurarsi che l'utente fornisca una chiave valida nella tabella della finestra di dialogo.

Null è un valore valido per questo tipo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della [tabella ModuleConfiguration](moduleconfiguration-table.md).

Il tipo di finestra di dialogo può essere utilizzato con i tipi di ContextData seguenti.

**ContextData DialogNext**

Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una chiave esterna nella tabella della finestra di dialogo. Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna nome, immettere "1" nella colonna formato, immettere "finestra di dialogo" nella colonna tipo e immettere "DialogNext" nella colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md).

**ContextData DialogPrev**

Un modulo merge configurabile può utilizzare questo tipo per consentire all'utente di fornire una chiave esterna nella tabella della finestra di dialogo. Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna nome, immettere "1" nella colonna formato, immettere "finestra di dialogo" nella colonna tipo e immettere "DialogPrev" nella colonna ContextData della tabella ModuleConfiguration.

 

 



