---
description: Specifica le informazioni sul segnale video, oltre al livello di protezione.
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527876"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a>il \_ set \_ di OPM ACP \_ e la \_ \_ segnalazione CGMSA

Specifica le informazioni sul segnale video, oltre al livello di protezione.



| Requisito | Valore |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| GUID comando | il \_ set \_ di OPM ACP \_ e la \_ \_ segnalazione CGMSA                                                                                |
| Dati di input   | Struttura [**di \_ \_ parametri di \_ \_ \_ segnalazione \_ ACP e CGMSA di un set OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) |



 

## <a name="remarks"></a>Commenti

Questo comando equivale al \_ comando DXVA COPPSetSignaling usato in Certified Output Protocol (Copp).

Per CGMS-A, determinati standard di protezione richiedono che il segnale televisivo includa informazioni all'interno degli stessi pacchetti di forma d'onda VBI dei bit CGMS-A. Tra le altre cose, queste informazioni includono le proporzioni dell'immagine. I televisori potrebbero non essere visualizzati correttamente se le informazioni sulle proporzioni non sono coerenti con il flusso video. L'applicazione può utilizzare questo comando per specificare le proporzioni in modo che il driver di grafica possa generare i pacchetti VBI corretti.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[Comandi di OPM](opm-commands.md)
</dt> </dl>

 

 




