---
title: Acquisizione di User-Initiated
description: Acquisizione di User-Initiated
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db44049ff64f6e0187ed38ca78ca0d3e1f36d6ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856625"
---
# <a name="user-initiated-capture"></a>Acquisizione di User-Initiated

È possibile recuperare il valore corrente del flag di acquisizione avviato dall'utente usando il messaggio di [**\_ installazione della \_ sequenza di recupero della \_ sequenza \_ di WM Cap**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Il valore del flag viene archiviato nel membro **fMakeUserHitOKToCapture** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . È possibile fornire all'utente un controllo preciso su quando avviare una sessione di acquisizione impostando questo membro su **true**. AVICap Visualizza una finestra di dialogo dopo l'allocazione di tutti i buffer video e audio per una sessione di acquisizione. Ciò consente all'utente di eliminare i ritardi di acquisizione a causa dell'inizializzazione del software. Se l'applicazione usa un numero ridotto di buffer video, questa finestra di dialogo è probabilmente non necessaria. Il valore predefinito è **false**.

 

 




