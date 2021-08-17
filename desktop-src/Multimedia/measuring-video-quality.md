---
title: Misurazione della qualità video
description: Misurazione della qualità video
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- WM_CAP_GET_SEQUENCE_SETUP messaggio
- Macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP messaggio
- Macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d3a4d28c12905722447189eabc494b220d737fc0c87f7a9ebc12948390920d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118373535"
---
# <a name="measuring-video-quality"></a>Misurazione della qualità video

Un modo per misurare la qualità del video è limitare il numero di fotogrammi acquisiti eliminati durante l'operazione di acquisizione. Al termine dell'acquisizione di streaming, il valore di qualità viene confrontato con il rapporto tra fotogrammi rilasciati e frame totali. Se la percentuale di frame eliminati è maggiore del valore del membro **wPercentDropForError** della struttura [**CAPTUREPARMS,**](/windows/win32/api/vfw/ns-vfw-captureparms) AVICap invia un messaggio di errore alla funzione di callback degli errori, se installata.

È possibile recuperare il limite corrente di frame eliminati (espressi come percentuale) usando il messaggio [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) È possibile impostare un nuovo limite specificando una percentuale come valore del membro **wPercentDropForError** della struttura **CAPTUREPARMS** e quindi inviando la struttura aggiornata alla finestra di acquisizione usando il messaggio [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) Il valore predefinito **di wPercentDropForError** è 10%.

 

 




