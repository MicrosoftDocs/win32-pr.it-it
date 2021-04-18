---
description: Il tipo di file di tipo semantico è uno dei tipi di formato chiave. Questo tipo è costituito da una chiave esterna nella tabella file fornita dall'utente.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b47e76f4a910b336c749a4f0d5001c8568cead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315474"
---
# <a name="file-type"></a>Tipo di file

Il tipo di file di [tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md). Questo tipo è costituito da una chiave esterna nella [tabella file](file-table.md) fornita dall'utente.

Il tipo di file può essere usato con i tipi di ContextData seguenti.

**ContextData AssemblyContext**

Questo tipo può essere utilizzato per consentire agli utenti di configurare chiavi esterne per gli assembly Win32 o Common Language Runtime. Lo strumento di merge deve sostituire un [identificatore](identifier.md) Windows Installer per gli elementi di questo tipo nel modello nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md). Mergemod.dll non impone questa operazione ed è lo strumento di merge per assicurarsi che l'utente fornisca una chiave valida nella tabella file.

Null è un valore valido per questo tipo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della [tabella ModuleConfiguration](moduleconfiguration-table.md).

 

 



