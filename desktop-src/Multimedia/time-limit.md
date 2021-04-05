---
title: Limite di tempo
description: Limite di tempo
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- Struttura CAPTUREPARMS
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Struttura CAPTUREPARMS
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878c76ab1e380fe878cd8c9493163bcb71e574cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714440"
---
# <a name="time-limit"></a>Limite di tempo

È possibile limitare la durata di un'operazione di acquisizione usando i membri **fLimitEnabled** e **WTimeLimit** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . Il membro **fLimitEnabled** indica se l'operazione di acquisizione deve essere temporizzata, mentre **wTimeLimit** specifica la durata massima dell'operazione di acquisizione.

È possibile recuperare i valori per **fLimitEnabled** e **wTimeLimit** usando il messaggio di [**installazione della sequenza di WM \_ Cap \_ \_ \_ Get**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). È possibile abilitare un timer per l'operazione di acquisizione specificando **true** come valore di **fLimitEnabled** oppure è possibile impostare la durata dell'operazione di acquisizione specificando un valore, in secondi, per **wTimeLimit**. Dopo aver impostato questi membri, inviare la struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) aggiornata alla finestra di acquisizione usando il messaggio [**di \_ \_ installazione della \_ sequenza \_ del set**](wm-cap-set-sequence-setup.md) di test WM (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). Il valore predefinito di **fLimitEnabled** è **false**.

 

 




