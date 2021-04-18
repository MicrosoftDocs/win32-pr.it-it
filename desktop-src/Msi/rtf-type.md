---
description: Il tipo RTF di tipo semantico è uno dei tipi di formato testo.
ms.assetid: 91fc47c1-520a-4002-9dbe-4ee2b56f84b3
title: Tipo RTF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81c708183596d794f20e38bf89c073472e3affb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313334"
---
# <a name="rtf-type"></a>Tipo RTF

Il tipo RTF di [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md). Questo tipo è costituito da una stringa di testo arbitraria nel formato RTF (Rich Text Format) di qualsiasi lunghezza fornita dall'utente. Lo strumento di merge sostituisce questa stringa nei modelli specificati nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).

Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della stringa di testo nella colonna nome, immettere "0" nella colonna formato, immettere "RTF" nella colonna tipo e lasciare vuota la colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md). La stringa può essere in qualsiasi linguaggio compatibile con la tabella codici del database. Vedere la pagina relativa alla [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md). Null è un valore valido per la stringa di testo a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della tabella ModuleConfiguration.

 

 



