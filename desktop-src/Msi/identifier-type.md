---
description: Il tipo di identificatore di tipo semantico è uno dei tipi di formato testo.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Tipo di identificatore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6d4e63b473c9ba0705c093f1dec5bcdbc1e26f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131482"
---
# <a name="identifier-type"></a>Tipo di identificatore

Il tipo di identificatore di [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md). Questo tipo è costituito da una stringa di testo fornita dall'utente nel formato di un [identificatore](identifier.md)Windows Installer. Lo strumento di merge sostituisce questa stringa nei modelli specificati nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).

Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della stringa di testo nella colonna nome, immettere "0" nella colonna formato, immettere "Identifier" nella colonna tipo e lasciare vuota la colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md). La stringa può essere in qualsiasi linguaggio compatibile con la tabella codici del database. Vedere la pagina relativa alla [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md). Null è un valore valido per la stringa di testo a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della tabella ModuleConfiguration.

 

 



