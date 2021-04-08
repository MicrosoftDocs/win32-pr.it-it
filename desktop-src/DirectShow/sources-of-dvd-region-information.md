---
description: Origini delle informazioni sull'area DVD
ms.assetid: f4874aa7-c58a-49a3-9474-c621cc19156b
title: Origini delle informazioni sull'area DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac426f995323bfd30d3430dccb4044c5f71a119
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967921"
---
# <a name="sources-of-dvd-region-information"></a>Origini delle informazioni sull'area DVD

Sono disponibili tre fonti di informazioni sull'area DVD che interagiscono per determinare l'area per la riproduzione di DVD in un computer Windows.

-   Titolo del DVD. La maggior parte dei titoli DVD è contrassegnata per un'area specifica. Alcuni titoli possono essere riprodotti in una sola area, alcuni possono essere riprodotti in più aree e altri possono essere riprodotti in tutte le aree. Le aree da 1 a 6 sono state definite nella specifica DVD-Video originale. L'area 7 non è attualmente definita. L'area 8 è stata aggiunta in 1999 per sedi speciali, ad esempio le aeroplani. I dischi DVD-ROM (quelli senza area video) non devono contenere codice di area.
-   Unità DVD-ROM. Esistono due tipi di unità DVD-ROM: unità RPC fase 1 (RPC1) e unità RPC fase 2 (RPC2). Le unità RPC1 non dispongono di supporto hardware integrato per la gestione delle aree. Per queste unità, Windows mantiene le informazioni sul conteggio delle modifiche dell'area e l'area può essere modificata una sola volta. Le unità RPC2 gestiscono le informazioni sul conteggio delle modifiche nell'hardware e, in generale, l'area di tali unità può essere modificata fino a 5 volte.
-   Decoder DVD. Alcuni decodificatori DVD, hardware o software, vengono impostati per un'area specifica. In generale, l'utente non può modificare l'area del decodificatore.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto delle modifiche all'area DVD in Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



