---
description: Il tipo di finestra di dialogo di tipo semantico è uno dei tipi di formato chiave. Questo tipo è costituito da una chiave esterna nella tabella Dialog fornita dall'utente.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Tipo di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f945b499cfab5ca8b3bf85180c16d9be88f4093b258513a11b5059874cb403
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764021"
---
# <a name="dialog-type"></a>Tipo di dialogo

Il tipo di dialogo [di tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md). Questo tipo è costituito da una chiave esterna nella [tabella Dialog fornita](dialog-table.md) dall'utente.

Lo strumento di unione deve sostituire un identificatore Windows [installer valido](identifier.md) per gli elementi di questo tipo. Mergemod.dll questa restrizione non viene applicata ed è lo strumento di unione a garantire che l'utente fornisce una chiave valida nella tabella Dialog.

Null è un valore valido per questo tipo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributi della [tabella ModuleConfiguration](moduleconfiguration-table.md).

Il tipo Dialog può essere usato con i tipi seguenti di ContextData.

**DialogNext ContextData**

Un modulo unione configurabile può usare questo tipo per consentire all'utente di fornire una chiave esterna nella tabella della finestra di dialogo. Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna Nome, immettere "1" nella colonna Formato, immettere "Dialog" nella colonna Tipo e immettere "DialogNext" nella colonna ContextData della tabella [ModuleConfiguration](moduleconfiguration-table.md).

**DialogPrev ContextData**

Un modulo unione configurabile può usare questo tipo per consentire all'utente di fornire una chiave esterna nella tabella della finestra di dialogo. Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento configurabile nella colonna Nome, immettere "1" nella colonna Formato, immettere "Dialog" nella colonna Tipo e immettere "DialogPrev" nella colonna ContextData della tabella ModuleConfiguration.

 

 



