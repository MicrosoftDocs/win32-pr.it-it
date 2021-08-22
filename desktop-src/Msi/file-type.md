---
description: Il tipo di file di tipo semantico è uno dei tipi di formato chiave. Questo tipo è costituito da una chiave esterna nella tabella File fornita dall'utente.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Tipo di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca7611cce64bfe036575ac611ebbf63406721085f75162b04e9163eb38840cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581751"
---
# <a name="file-type"></a>Tipo di file

Il tipo di [file di tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md). Questo tipo è costituito da una chiave esterna nella [tabella File](file-table.md) fornita dall'utente.

Il tipo file può essere usato con i tipi di ContextData seguenti.

**AssemblyContext ContextData**

Questo tipo può essere usato per consentire agli utenti di configurare chiavi esterne in assembly Win32 o Common Language Runtime. Lo strumento di unione deve sostituire Windows [identificatore](identifier.md) del programma di installazione per gli elementi di questo tipo nel modello nella colonna Valore della [tabella ModuleSubstitution](modulesubstitution-table.md). Mergemod.dll questa operazione non viene applicata ed è lo strumento di unione a garantire che l'utente fornisce una chiave valida nella tabella File.

Null è un valore valido per questo tipo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributi della [tabella ModuleConfiguration](moduleconfiguration-table.md).

 

 



