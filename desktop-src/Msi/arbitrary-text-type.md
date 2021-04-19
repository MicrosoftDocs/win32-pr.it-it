---
description: Il tipo di testo arbitrario di tipo semantico è uno dei tipi di formato testo.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Tipo di testo arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311054"
---
# <a name="arbitrary-text-type"></a>Tipo di testo arbitrario

Il tipo di testo arbitrario di [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md). Questo tipo è costituito da una stringa di testo arbitraria di qualsiasi lunghezza fornita dall'utente. Lo strumento di merge sostituisce questa stringa arbitraria nei modelli specificati nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).

Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della stringa di testo nella colonna nome, immettere "0" nella colonna formato e lasciare vuote le colonne Type e ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md). La stringa di testo arbitrario può essere in qualsiasi linguaggio compatibile con la tabella codici del database. Per informazioni dettagliate, vedere la pagina relativa alla [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md). Null è un valore valido per la stringa di testo a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della tabella ModuleConfiguration.

 

 



