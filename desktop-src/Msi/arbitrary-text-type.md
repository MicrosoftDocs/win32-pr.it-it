---
description: Il tipo di testo arbitrario di tipo semantico è uno dei tipi di formato testo.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Tipo di testo arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf22ea2a7c4be001a5c036d3e2ee2e8c441ba061f3a7ba5bda32abde3806c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066261"
---
# <a name="arbitrary-text-type"></a>Tipo di testo arbitrario

Il tipo di testo arbitrario di [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md). Questo tipo è costituito da una stringa di testo arbitraria di qualsiasi lunghezza fornita dall'utente. Lo strumento di unione sostituisce questa stringa arbitraria nei modelli specificati nella colonna Valore della [tabella ModuleSubstitution](modulesubstitution-table.md).

Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della stringa di testo nella colonna Nome, immettere "0" nella colonna Formato e lasciare vuote le colonne Type e ContextData della tabella [ModuleConfiguration](moduleconfiguration-table.md). La stringa di testo arbitraria può essere in qualsiasi linguaggio compatibile con la tabella codici del database. Per informazioni dettagliate, [vedere Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md). Null è un valore valido per la stringa di testo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributi della tabella ModuleConfiguration.

 

 



