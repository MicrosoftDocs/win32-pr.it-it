---
title: User-Initiated capture
description: User-Initiated capture
ms.assetid: e0d245f3-ac79-42c4-9969-8c9ec66eac62
keywords:
- WM_CAP_GET_SEQUENCE_SETUP messaggio
- Macro capCaptureGetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ca015726aabe7c171f37590a98e60774c34a09c219ef445af3e30f199d5030b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892451"
---
# <a name="user-initiated-capture"></a>User-Initiated capture

È possibile recuperare il valore corrente del flag di acquisizione avviato dall'utente usando il messaggio [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) Il valore del flag viene archiviato nel **membro fMakeUserHitOKToCapture** della [**struttura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) È possibile fornire all'utente un controllo preciso su quando avviare una sessione di acquisizione impostando questo membro su **TRUE.** AVICap visualizza una finestra di dialogo dopo l'allocazione di tutti i buffer audio e video per una sessione di acquisizione. Ciò consente all'utente di eliminare i ritardi di acquisizione a causa dell'inizializzazione del software. Se l'applicazione usa un numero ridotto di buffer video, questa finestra di dialogo probabilmente non è necessaria. Il valore predefinito è **FALSE.**

 

 




