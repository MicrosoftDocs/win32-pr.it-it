---
title: Misurazione della qualità dei video
description: Misurazione della qualità dei video
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- Messaggio WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Messaggio WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044640"
---
# <a name="measuring-video-quality"></a>Misurazione della qualità dei video

Un modo per misurare la qualità dei video consiste nel limitare il numero di frame acquisiti eliminati durante l'operazione di acquisizione. Al termine dell'acquisizione del flusso, il valore della qualità viene confrontato con il rapporto tra i frame eliminati e il totale dei frame. Se la percentuale di frame eliminati è maggiore del valore del membro **wPercentDropForError** della struttura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) , AVICap Invia un messaggio di errore alla funzione di callback degli errori, se installata.

È possibile recuperare il limite corrente di frame eliminati (espresso come percentuale) usando il messaggio di [**\_ installazione della \_ \_ sequenza \_ WM Cap Get**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). È possibile impostare un nuovo limite specificando una percentuale come valore del membro **wPercentDropForError** della struttura **CAPTUREPARMS** e quindi inviando la struttura aggiornata alla finestra di acquisizione usando il messaggio di installazione della [**\_ sequenza del \_ set \_ \_ di estremità WM**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). Il valore predefinito di **wPercentDropForError** è 10%.

 

 




