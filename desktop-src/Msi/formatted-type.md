---
description: Il tipo formattato di tipo semantico è uno dei tipi di formato testo.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Tipo formattato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b97e0c0c1763352f75424bf54d01f6871604f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049702"
---
# <a name="formatted-type"></a>Tipo formattato

Il tipo formattato di [tipo semantico](semantic-types.md) è uno dei [tipi di formato testo](text-format-types.md). Questo tipo è costituito da una stringa di testo arbitraria di qualsiasi lunghezza fornita dall'utente e nel formato di testo formattato Windows Installer. Per informazioni dettagliate, vedere [formattato](formatted.md). Lo strumento di merge sostituisce questa stringa nei modelli specificati nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md).

Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome della stringa di testo nella colonna nome, immettere "0" nella colonna formato, immettere "formattato" nella colonna tipo e lasciare vuota la colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md). La stringa può essere in qualsiasi linguaggio compatibile con la tabella codici del database. Per informazioni dettagliate, vedere la pagina relativa alla [gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md). Null è un valore valido per la stringa di testo a meno che msmConfigItemNonNullable non sia stato incluso nel campo Attributes della tabella ModuleConfiguration.

 

 



