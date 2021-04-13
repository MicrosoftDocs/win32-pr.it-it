---
description: I caratteri definiti dall'utente finale (EUDC) nei set di caratteri a doppio byte (DBCS) e nei caratteri PUA (private use area) in Unicode sono caratteri personalizzati.
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: Caratteri dell'area uso privato e definiti dall'utente finale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4307880a361bb847bb0dc24392006614336772
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348141"
---
# <a name="end-user-defined-and-private-use-area-characters"></a>Caratteri dell'area uso privato e definiti dall'utente finale

I caratteri definiti dall'utente finale (EUDC) nei [set di caratteri a doppio byte](double-byte-character-sets.md) (DBCS) e nei caratteri PUA (private use area) in [Unicode](unicode.md) sono caratteri personalizzati. Possono essere definiti e implementati da un utente finale o da un'altra parte, ad esempio un produttore di apparecchiature, un gruppo di utenti, un corpo del governo o una società di progettazione dei tipi di carattere. Il loro utilizzo consente agli utenti di creare nomi e altre parole utilizzando caratteri non disponibili nei tipi di carattere standard e della stampante.

I caratteri EUDC e PUA possono essere assegnati in modo diverso o non assegnati in computer diversi. Alcune tabelle codici includono estensioni che riutilizzano l'intervallo di EUDC e queste estensioni possono essere in conflitto tra loro. In altri casi, un produttore potrebbe fornire un set di caratteri personalizzato in uno di questi intervalli. Inoltre, i gruppi di utenti possono tentare di fornire caratteri aggiuntivi in PUA. Diverse combinazioni di questi casi possono causare conflitti. Quando si creano applicazioni che si basano su caratteri EUDC o PUA, è necessario tenere presenti le interpretazioni in conflitto di un singolo punto di codice.

Negli argomenti seguenti vengono illustrati i tipi di carattere che supportano EUDCs, nonché l'accesso e la gestione di questi caratteri:

-   [Set di caratteri e tipi di carattere](character-sets-and-fonts.md)
-   [Voci del registro di sistema EUDC](eudc-registry-entries.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui set di caratteri e Unicode](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



