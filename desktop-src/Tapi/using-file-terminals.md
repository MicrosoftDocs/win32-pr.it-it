---
description: I terminali di file possono essere usati in due modi.
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: Uso dei terminali di file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd72a02306efb5503d184b3f4e678df1ab2517928c8c8406d98b1d7d0efb41d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975128"
---
# <a name="using-file-terminals"></a>Uso dei terminali di file

I terminali di file possono essere usati in due modi. Il metodo più semplice è usare [**ITBasicCallControl2::SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) per selezionare un terminale di file (riproduzione o record) in un oggetto chiamata TAPI. In questo caso TAPI si occupa della connessione dei flussi audio ai terminali di traccia.

Il secondo metodo consente a un'applicazione di avere un controllo più fine sul mapping dei flussi audio alle tracce. In questo scenario, l'applicazione enumera i flussi disponibili nella chiamata, seleziona quelli che vuole registrare (o usare per la riproduzione), crea (o trova per la riproduzione) le tracce corrispondenti nel terminale di file e seleziona le tracce nei flussi di chiamata.

Per altre informazioni, vedere i seguenti argomenti:

-   [Riproduzione semplice](simple-playback.md)
-   [Riproduzione controllata dal tracciato](track-controlled-playback.md)
-   [Record semplice](simple-record.md)
-   [Record controllato dal tracciato](track-controlled-record.md)

 

 



