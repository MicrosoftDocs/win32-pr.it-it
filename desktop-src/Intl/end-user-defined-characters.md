---
description: I caratteri definiti dall'utente finale (EUDC) nei set di caratteri a byte doppio (DBCS) e nell'area di utilizzo privato (PUA) in Unicode sono caratteri personalizzati.
ms.assetid: e76ea1ed-5962-440a-a722-b59b314babd6
title: Caratteri dell'area di utilizzo definiti dall'utente finale e privati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19152ff8564cae4ccccc154a6c9d349f0fc6cd8791fcccb1973b553bc681cc5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119898760"
---
# <a name="end-user-defined-and-private-use-area-characters"></a>Caratteri dell'area di utilizzo definiti dall'utente finale e privati

I caratteri definiti dall'utente finale (EUDC) [nei](double-byte-character-sets.md) set di caratteri a byte doppio (DBCS) e nell'area di utilizzo privato (PUA) in [Unicode](unicode.md) sono caratteri personalizzati. Possono essere definiti e implementati da un utente finale o da un'altra parte, ad esempio un produttore di apparecchiature, un gruppo di utenti, un ente governativo o una società di progettazione di tipi di carattere. Il loro uso consente agli utenti di formare nomi e altre parole usando caratteri non disponibili nei tipi di carattere standard dello schermo e della stampante.

I caratteri EUDC e PUA possono essere assegnati in modo diverso, o non assegnati affatto, in computer diversi. Alcune codepage hanno estensioni che riutilizzano l'intervallo EUDC e queste estensioni possono essere in conflitto tra loro. In altri casi, un produttore potrebbe fornire un set personalizzato di caratteri in uno di questi intervalli. Inoltre, i gruppi di utenti possono tentare di fornire caratteri aggiuntivi nel pua. Combinazioni diverse di questi casi possono causare conflitti. Quando si creano applicazioni basate su caratteri EUDC o PUA, è necessario tenere presenti le interpretazioni in conflitto di un singolo punto di codice.

Negli argomenti seguenti vengono illustrati i tipi di carattere che supportano le UDC e l'accesso e la gestione per questi caratteri:

-   [Set di caratteri e tipi di carattere](character-sets-and-fonts.md)
-   [Voci del Registro di sistema EUDC](eudc-registry-entries.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui set di caratteri e Unicode](about-unicode-and-character-sets.md)
</dt> </dl>

 

 



