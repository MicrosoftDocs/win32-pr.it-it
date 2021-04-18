---
description: Modalità di selezione dell'area DVD da parte di Microsoft DVD Navigator
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Modalità di selezione dell'area DVD da parte di Microsoft DVD Navigator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8a2898725ad187946b50e567f7daa7e72a9886
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303729"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a>Modalità di selezione dell'area DVD da parte di Microsoft DVD Navigator

Microsoft DVD Navigator usa l'algoritmo seguente per determinare la corrispondenza dell'area durante la riproduzione di dischi DVD su un PC:

1.  Il navigatore DVD ottiene l'area del disco, l'area dell'unità e l'area del decodificatore.
2.  Se l'area del disco è "tutte le aree", il navigatore DVD riproduce il disco.
3.  Se il disco non è contrassegnato per tutte le aree, il navigatore DVD controlla se il decodificatore ha un'area preimpostata.
4.  Se il decodificatore ha un'area preimpostata e non corrisponde all'area del disco, il navigatore DVD restituisce un errore che indica che non è possibile riprodurre il disco nella configurazione DVD corrente. Uscita
5.  Se l'area del decodificatore non è impostata o è uguale all'area del disco, il navigatore DVD controlla se l'area dell'unità è uguale all'area del disco.
6.  Se l'area dell'unità corrisponde all'area del disco, il navigatore DVD riproduce il titolo.
7.  In caso contrario, se l'area del driver non corrisponde all'area del disco, il navigatore DVD richiama il codice per modificare l'area dell'unità. Se il numero consentito di modifiche all'area è esaurito, il tentativo di modifica dell'area ha esito negativo e il titolo non può essere riprodotto nel sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto delle modifiche all'area DVD in Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



