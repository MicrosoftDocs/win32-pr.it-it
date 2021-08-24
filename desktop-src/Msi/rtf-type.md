---
description: Il tipo RTF di tipo semantico è uno dei tipi di formato testo.
ms.assetid: 91fc47c1-520a-4002-9dbe-4ee2b56f84b3
title: Tipo RTF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269b378644fbf41e906993097cea8bb4fb27f969cbda046aab59700896513774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039691"
---
# <a name="rtf-type"></a>Tipo RTF

Il tipo RTF di [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md). Questo tipo è costituito da una stringa di testo arbitraria nel formato RTF (Rich Text Format) di qualsiasi lunghezza fornita dall'utente. Lo strumento di unione sostituisce questa stringa nei modelli specificati nella colonna Value della [tabella ModuleSubstitution](modulesubstitution-table.md).

Per specificare un elemento configurabile di questo tipo, gli autori del modulo devono immettere il nome della stringa di testo nella colonna Nome, immettere "0" nella colonna Formato, immettere "RTF" nella colonna Tipo e lasciare vuota la colonna ContextData della tabella [ModuleConfiguration](moduleconfiguration-table.md). La stringa può essere in qualsiasi linguaggio compatibile con la tabella codici del database. Vedere [Gestione della tabella codici (Windows programma di installazione).](code-page-handling-windows-installer-.md) Null è un valore valido per la stringa di testo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributi della tabella ModuleConfiguration.

 

 



