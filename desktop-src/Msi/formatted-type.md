---
description: Il tipo formattato di tipo semantico è uno dei tipi di formato testo.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Tipo formattato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09fc535a48f6d2e89cc46fb0d64ee998b8c062d6c2a406b9d5b8801ef1b62293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044331"
---
# <a name="formatted-type"></a>Tipo formattato

Il tipo formattato di [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md). Questo tipo è costituito da una stringa di testo arbitraria di qualsiasi lunghezza fornita dall'utente e nel formato di testo formattato Windows Installer. Per informazioni dettagliate, vedere [Formatted](formatted.md). Lo strumento di unione sostituisce questa stringa nei modelli specificati nella colonna Valore della [tabella ModuleSubstitution](modulesubstitution-table.md).

Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della stringa di testo nella colonna Nome, immettere "0" nella colonna Formato, immettere "Formattato" nella colonna Tipo e lasciare vuota la colonna ContextData della tabella [ModuleConfiguration](moduleconfiguration-table.md). La stringa può essere in qualsiasi linguaggio compatibile con la tabella codici del database. Per informazioni dettagliate, [vedere Code Page Handling (Windows Installer)](code-page-handling-windows-installer-.md). Null è un valore valido per la stringa di testo, a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributi della tabella ModuleConfiguration.

 

 



