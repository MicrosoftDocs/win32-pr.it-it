---
description: Il tipo di icona di tipo semantico è uno dei tipi di formato chiave. Questo tipo è costituito da una chiave nella tabella Icon fornita dall'utente.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Tipo di icona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28510eff674d1f25e632b1181943af70da73d9fc97a6a64ec5abd0807fe15cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634954"
---
# <a name="icon-type"></a>Tipo di icona

Il tipo di icona di [tipo semantico](semantic-types.md) è uno dei [tipi di formato chiave](key-format-types.md). Questo tipo è costituito da una chiave nella [tabella Icon](icon-table.md) fornita dall'utente.

Lo strumento di merge deve sostituire un identificatore Windows [installer valido](identifier.md) per gli elementi di questo tipo. Mergemod.dll non applica questa restrizione ed è lo strumento di unione a garantire che l'utente fornisce una chiave valida nella tabella Icon.

Null è un valore valido per questo tipo a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributi della [tabella ModuleConfiguration](moduleconfiguration-table.md).

Il tipo Binary può essere usato con i tipi di ContextData seguenti.

**ShortcutIcon ContextData**

Un modulo unione configurabile può usare questo tipo per consentire all'utente di fornire una chiave esterna a una riga nella tabella delle icone che contiene un'immagine adatta per l'uso come icona di collegamento. [](icon-table.md) Per specificare un elemento configurabile di questo tipo, gli autori di moduli devono immettere il nome dell'elemento configurabile nella colonna Nome, immettere "1" nella colonna Formato, immettere "Icon" nella colonna Tipo e immettere "ShorcutIcon" nella colonna ContextData della tabella ModuleConfiguration. Questo tipo non è appropriato per l'uso in una tabella dell'interfaccia utente. Per modificare una chiave per la tabella Icon in queste tabelle, vedere Icon ContextData in Binary Type ( [Tipo binario).](binary-type.md)

 

 



