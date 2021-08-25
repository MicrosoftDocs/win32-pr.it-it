---
title: Stato della finestra di acquisizione
description: Stato della finestra di acquisizione
ms.assetid: c3f80cac-30b2-42f0-8a9c-4053728c558b
keywords:
- WM_CAP_GET_STATUS messaggio
- Macro capGetStatus
- Struttura CAPSTATUS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 367d35c3869adb6f4e960fa472e0cd6a22483c37fa981e886b3a78f0b7410029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375287"
---
# <a name="capture-window-status"></a>Stato della finestra di acquisizione

È possibile recuperare lo stato corrente di una finestra di acquisizione usando il messaggio [**WM \_ CAP GET \_ \_ STATUS**](wm-cap-get-status.md) (o la macro [**capGetStatus).**](/windows/desktop/api/Vfw/nf-vfw-capgetstatus) Questo messaggio recupera una copia della struttura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) con i valori correnti dei relativi membri. La **struttura CAPSTATUS** contiene informazioni relative alle dimensioni dell'immagine, alla posizione di scorrimento e all'attivazione della sovrapposizione o dell'anteprima dell'immagine. Poiché le informazioni rappresentate in **CAPSTATUS** sono dinamiche, l'applicazione deve aggiornare il contenuto della struttura ogni volta che le dimensioni o il formato del flusso video acquisito potrebbero essere cambiati, ad esempio dopo la visualizzazione del formato video del driver di acquisizione.

La modifica delle dimensioni della finestra di acquisizione non ha alcun effetto sulle dimensioni del flusso video acquisito effettivo. La finestra di dialogo formato visualizzata dal driver di dispositivo di acquisizione video controlla le dimensioni del flusso video acquisito.

 

 




