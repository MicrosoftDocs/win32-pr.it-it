---
title: Stato della finestra di acquisizione
description: Stato della finestra di acquisizione
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- Messaggio WM_CAP_GET_STATUS
- capGetStatus (macro)
- Struttura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e6019009c8510abe3429c1043527156c55f0c4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045108"
---
# <a name="capture-window-status"></a>Stato della finestra di acquisizione

È possibile recuperare lo stato corrente di una finestra di acquisizione usando il messaggio di [**\_ \_ \_ stato WM Cap Get**](wm-cap-get-status.md) (o la macro [**capGetStatus**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) ). Questo messaggio recupera una copia della struttura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) con i valori correnti dei relativi membri. La struttura **CAPSTATUS** contiene informazioni riguardanti le dimensioni dell'immagine, la posizione di scorrimento e se è abilitata la sovrapposizione o l'anteprima dell'immagine. Poiché le informazioni rappresentate in **CAPSTATUS** sono dinamiche, l'applicazione deve aggiornare il contenuto della struttura ogni volta che è possibile che la dimensione o il formato del flusso video acquisito venga modificato (ad esempio dopo aver visualizzato il formato video del driver di acquisizione).

La modifica delle dimensioni della finestra di acquisizione non ha effetto sulle dimensioni del flusso video acquisito effettivo. La finestra di dialogo formato visualizzata dal driver del dispositivo di acquisizione video controlla le dimensioni del flusso video acquisito.

 

 




