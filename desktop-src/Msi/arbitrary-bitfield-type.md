---
description: Il &\# 0034; Bitfield&0034; tipo senza richieste di contesto che l'utente fornisce un numero intero il cui valore viene usato per impostare uno o più \# bit in un campo di bit. Questo testo può essere in qualsiasi linguaggio compatibile con la tabella codici del database.
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Tipo di campo di bit arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521889ffb1677bed249a92f757556a2fdbe36768
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884578"
---
# <a name="arbitrary-bitfield-type"></a>Tipo di campo di bit arbitrario

Tipo "Bitfield" senza richieste di contesto che l'utente fornisce un numero intero il cui valore viene usato per impostare uno o più bit in un campo di bit. Questo testo può essere in qualsiasi linguaggio compatibile con la tabella codici del database.

Il tipo di campo di bit arbitrario di [tipo semantico](semantic-types.md) è uno dei tipi bitfield. Questo tipo è costituito da un numero intero scelto dall'utente da un set di scelte. Lo strumento di unione sostituisce l'intero selezionato nei modelli specificati nella colonna Valore della [tabella ModuleSubstitution](modulesubstitution-table.md). Per specificare un elemento configurabile di questo tipo, gli autori di moduli devono immettere il nome dell'elemento nella colonna Nome, immettere "3" nella colonna Formato, lasciare vuota la colonna Tipo e immettere l'elenco di possibili numeri interi nella colonna ContextData della [tabella ModuleConfiguration](moduleconfiguration-table.md).

La colonna Type è riservata e deve essere Null. La voce nella colonna ContextData per tutti i tipi di formato bitfield deve essere nel formato " &lt; mask &gt; ; &lt; Valore &gt; = &lt; del nome &gt; ; &lt; Name value ....", dove mask è un valore intero che indica i bit di interesse, Name è un nome visualizzato localizzabile per la scelta e value è un valore &gt; = &lt; &gt; intero &lt; &gt; &lt; &gt; &lt; &gt; decimale. La colonna di contesto è in uso [il formato speciale CMSM](cmsm-special-format.md) e per tutti i tipi di campo di bit. È possibile immettere un carattere letterale "=" o ";" nel campo Nome antendo un carattere barra &lt; &gt; rovesciata (' \\ ').

 

 



