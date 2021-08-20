---
description: Modalità di selezione dell'area DVD da parte di Microsoft DVD Navigator
ms.assetid: 407619c6-2d4b-4f7f-a861-42ee0f462ecd
title: Modalità di selezione dell'area DVD da parte di Microsoft DVD Navigator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822a546276c57296bb4514e3ab2c8917abfe7218fe3afeadd528ac6bd80066d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999770"
---
# <a name="how-microsoft-dvd-navigator-selects-the-dvd-region"></a>Modalità di selezione dell'area DVD da parte di Microsoft DVD Navigator

Microsoft DVD Navigator usa l'algoritmo seguente per determinare la corrispondenza dell'area durante la riproduzione di dischi DVD in un PC:

1.  Lo strumento di navigazione DVD ottiene l'area del disco, l'area dell'unità e l'area del decodificatore.
2.  Se l'area del disco è "tutte le aree", lo strumento di spostamento DVD riproduce il disco.
3.  Se il disco non è contrassegnato per tutte le aree, lo strumento di navigazione DVD controlla se il decodificatore ha un'area preimpostato.
4.  Se il decodificatore ha un'area preimpostato e non corrisponde all'area del disco, lo strumento di navigazione DVD restituisce un errore che indica che non è in grado di riprodurre il disco nella configurazione DVD corrente. (Esci)
5.  Se l'area del decodificatore non è impostata o è uguale all'area disco, lo strumento di spostamento DVD verifica se l'area unità è uguale all'area disco.
6.  Se l'area dell'unità corrisponde all'area del disco, lo strumento di navigazione DVD riproduce il titolo.
7.  In caso contrario, se l'area del driver non corrisponde all'area del disco, lo strumento di spostamento DVD richiama il codice per modificare l'area dell'unità. Se il numero consentito di modifiche all'area è esaurito, il tentativo di modifica dell'area ha esito negativo e il titolo non può essere riprodotto in tale sistema.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto delle modifiche all'area DVD in Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



