---
description: Il &\# 0034; Campo di&0034; tipo senza richieste di contesto che l'utente fornisce un intero il cui valore viene utilizzato per impostare uno o più bit in un campo \# di bit. Questo testo può essere in qualsiasi linguaggio compatibile con la tabella codici del database.
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Tipo di campo di bit arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 842c9d1725b2bfe9ef0585cafd085ac1ceba33554899909ae3317af38fd7caac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118381385"
---
# <a name="arbitrary-bitfield-type"></a>Tipo di campo di bit arbitrario

Tipo "Bitfield" senza richieste di contesto che l'utente fornisce un integer il cui valore viene usato per impostare uno o più bit in un campo di bit. Questo testo può essere in qualsiasi linguaggio compatibile con la tabella codici del database.

Il tipo di campo di bit [arbitrario di tipo semantico](semantic-types.md) è uno dei tipi bitfield. Questo tipo è costituito da un numero intero scelto dall'utente da un set di scelte. Lo strumento di unione sostituisce l'intero selezionato nei modelli specificati nella colonna Value della [tabella ModuleSubstitution](modulesubstitution-table.md). Per specificare un elemento configurabile di questo tipo, gli autori di moduli devono immettere il nome dell'elemento nella colonna Nome, immettere "3" nella colonna Formato, lasciare vuota la colonna Tipo e immettere l'elenco di possibili numeri interi nella colonna ContextData della tabella [ModuleConfiguration](moduleconfiguration-table.md).

La colonna Type è riservata e deve essere Null. La voce nella colonna ContextData per tutti i tipi di formato bitfield deve essere nel formato " <mask> ;<Name>=<value>;<Name>=<value>....", dove è un valore intero che indica i bit di interesse, è un nome visualizzato <mask> localizzabile per la scelta <Name> e <value> è un valore intero decimale. La colonna context è in uso [cmsm special format e](cmsm-special-format.md) per tutti i tipi di campo di bit. È possibile immettere un carattere letterale "=" o ";" nel campo anteficcando una barra <Name> rovesciata (' \\ ').

 

 



