---
description: Il &\# 0034; Bit&\# 0034; tipo senza richieste di contesto che l'utente fornisca un Integer il cui valore viene usato per impostare uno o più bit in un bit. Questo testo può essere in qualsiasi linguaggio compatibile con la tabella codici del database.
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Tipo bit arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6571b8585c94577927df8cfedaded802a67d125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131495"
---
# <a name="arbitrary-bitfield-type"></a>Tipo bit arbitrario

Il tipo "bit" senza richieste di contesto fornisce un Integer il cui valore viene usato per impostare uno o più bit in un bit. Questo testo può essere in qualsiasi linguaggio compatibile con la tabella codici del database.

Il tipo di bit arbitrario di [tipo semantico](semantic-types.md) è uno dei tipi bit. Questo tipo è costituito da un numero intero scelto dall'utente da un set di opzioni. Lo strumento di merge sostituisce l'intero selezionato con i modelli specificati nella colonna valore della [tabella ModuleSubstitution](modulesubstitution-table.md). Per specificare un elemento configurabile di questo tipo, gli autori dei moduli devono immettere il nome dell'elemento nella colonna nome, immettere "3" nella colonna formato, lasciare vuota la colonna tipo e immettere l'elenco dei possibili numeri interi nella colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md).

La colonna del tipo è riservata e deve essere null. La voce nella colonna ContextData per tutti i tipi di formato bit deve avere il formato " <mask> ;<Name>=<value>;<Name>=<value>.... ", dove <mask> è un valore intero che indica i bit di interesse, <Name> è un nome visualizzato localizzabile per la scelta e <value> è un valore integer decimale. La colonna context è in uso [CMSM special format](cmsm-special-format.md) e per tutti i tipi bit. Un carattere letterale "=" o ";" può essere inserito nel <Name> campo anteponendo il carattere barra rovesciata (' \\ ').

 

 



