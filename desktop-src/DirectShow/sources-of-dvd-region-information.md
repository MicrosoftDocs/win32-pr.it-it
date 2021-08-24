---
description: Origini delle informazioni sull'area DVD
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: Origini delle informazioni sull'area DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729dc02d07b927dd2bb7938ba87c6435df04459ad3ebd1976ede808bd292552e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904097"
---
# <a name="sources-of-dvd-region-information"></a>Origini delle informazioni sull'area DVD

Esistono tre fonti di informazioni sull'area DVD che funzionano insieme per determinare l'area per la riproduzione di DVD in un PC Windows.

-   Titolo DVD. La maggior parte dei titoli dei DVD è contrassegnata per un'area specifica. Alcuni titoli possono essere riprodotti in una sola area, altri in più aree e altri in tutte le aree. Le aree da 1 a 6 sono state definite nella specifica DVD-Video originale. L'area 7 non è attualmente definita. L'area 8 è stata aggiunta nel 1999 per sedi speciali, ad esempio gli aerei. I dischi DVD-ROM (quelli senza zona video) non devono contenere codice di area.
-   Unità DVD-ROM. Esistono due tipi di unità DVD-ROM: RPC Fase 1 (RPC1) e RPC Fase 2 (RPC2). Le unità RPC1 non dispongono del supporto hardware incorporato per la gestione delle aree. Per queste unità, Windows le informazioni sul conteggio delle modifiche dell'area e l'area può essere modificata una sola volta. Le unità RPC2 mantengono le informazioni sul conteggio delle modifiche dell'area nell'hardware e, in generale, l'area di tali unità può essere modificata fino a 5 volte.
-   Decodificatore DVD. Alcuni decodificatori DVD, hardware o software, sono impostati per un'area specifica. In generale, l'utente non può modificare l'area del decodificatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto della modifica dell'area DVD in Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



