---
title: Frequenza di acquisizione
description: Frequenza di acquisizione
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- WM_CAP_GET_SEQUENCE_SETUP messaggio
- Macro capCaptureGetSetup
- Struttura CAPTUREPARMS
- WM_CAP_SET_SEQUENCE_SETUP messaggio
- Macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 855cff56e36d9a246e1f18ae5fc4e3c09a200a2114104424f053a8780881de93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691661"
---
# <a name="capture-rate"></a>Frequenza di acquisizione

La frequenza di acquisizione è il numero di fotogrammi acquisiti ogni secondo di una sessione di acquisizione. È possibile recuperare la frequenza di acquisizione corrente usando il messaggio [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) La frequenza di acquisizione corrente viene archiviata nel **membro dwRequestMicroSecPerFrame** della [**struttura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) È possibile impostare la frequenza di acquisizione specificando il numero di microsecondi tra fotogrammi successivi come valore di questo membro, quindi inviando la struttura **CAPTUREPARMS** aggiornata alla finestra di acquisizione usando il messaggio [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) Il valore predefinito **di dwRequestMicroSecPerFrame** è 66667, che corrisponde a 15 fotogrammi al secondo.

 

 




