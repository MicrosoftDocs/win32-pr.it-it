---
description: Il tipo di identificatore di tipo semantico è uno dei tipi di formato testo.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Tipo di identificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab1061f6d813b0803dbe1aa0d8e49e7f93cffba6e100f778901441f4bc4ed710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634782"
---
# <a name="identifier-type"></a>Tipo di identificatore

Il tipo di identificatore di [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md). Questo tipo è costituito da una stringa di testo fornita dall'utente nel formato di un Windows identificatore del programma [di installazione](identifier.md). Lo strumento di unione sostituisce questa stringa nei modelli specificati nella colonna Value della [tabella ModuleSubstitution](modulesubstitution-table.md).

Per specificare un elemento configurabile di questo tipo, gli autori del modulo devono immettere il nome della stringa di testo nella colonna Nome, immettere "0" nella colonna Formato, immettere "Identificatore" nella colonna Tipo e lasciare vuota la colonna ContextData della tabella [ModuleConfiguration](moduleconfiguration-table.md). La stringa può essere in qualsiasi linguaggio compatibile con la tabella codici del database. Vedere [Gestione della tabella codici (Windows programma di installazione).](code-page-handling-windows-installer-.md) Null è un valore valido per la stringa di testo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributi della tabella ModuleConfiguration.

 

 



