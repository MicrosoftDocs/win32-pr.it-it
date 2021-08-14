---
title: Limite di tempo
description: Limite di tempo
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- Struttura CAPTUREPARMS
- WM_CAP_GET_SEQUENCE_SETUP messaggio
- Macro capCaptureGetSetup
- Struttura CAPTUREPARMS
- WM_CAP_SET_SEQUENCE_SETUP messaggio
- Macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b6211edf3ce3fb86b4c0430c685ff05ff7f95c718c0a89e7ba782ae342feb18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117801265"
---
# <a name="time-limit"></a>Limite di tempo

È possibile limitare la durata di un'operazione di acquisizione usando i membri **fLimitEnabled** e **wTimeLimit** della [**struttura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) Il **membro fLimitEnabled** indica se l'operazione di acquisizione deve essere programmata, mentre **wTimeLimit** specifica la durata massima dell'operazione di acquisizione.

È possibile recuperare i valori per **fLimitEnabled** e **wTimeLimit** usando il messaggio [**WM CAP GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) È possibile abilitare un timer per l'operazione di acquisizione specificando **TRUE** come valore di **fLimitEnabled** oppure è possibile impostare la durata dell'operazione di acquisizione specificando un valore, in secondi, per **wTimeLimit**. Dopo aver impostato questi membri, inviare la struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) aggiornata alla finestra di acquisizione usando il messaggio [**WM CAP SET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) Il valore predefinito di **fLimitEnabled** è **FALSE.**

 

 




