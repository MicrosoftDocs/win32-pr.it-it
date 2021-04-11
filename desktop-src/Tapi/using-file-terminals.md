---
description: I terminali dei file possono essere utilizzati in due modi.
ms.assetid: 5a7d6aa7-0eb8-4652-af0b-74fbdb5a2c2f
title: Uso di terminali file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7637e83e56fddb2589bbd0858b5e994ca02855
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131926"
---
# <a name="using-file-terminals"></a>Uso di terminali file

I terminali dei file possono essere utilizzati in due modi. Il metodo più semplice consiste nell'usare [**ITBasicCallControl2:: SelectTerminalOnCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-selectterminaloncall) per selezionare un file Terminal (riproduzione o record) su un oggetto chiamata TAPI. In questo caso TAPI si occupa della connessione dei flussi audio ai terminali di tracking.

Il secondo metodo consente a un'applicazione di avere un controllo più preciso sul mapping dei flussi audio alle tracce. In questo scenario, l'applicazione enumera i flussi disponibili nella chiamata, seleziona quelli che vuole registrare (o usare per la riproduzione), crea (o trova per la riproduzione) le tracce corrispondenti nel terminale file e seleziona le tracce nei flussi di chiamata.

Per altre informazioni, vedere i seguenti argomenti:

-   [Riproduzione semplice](simple-playback.md)
-   [Riproduzione controllata dal rilevamento](track-controlled-playback.md)
-   [Record semplice](simple-record.md)
-   [Record controllato dal rilevamento](track-controlled-record.md)

 

 



