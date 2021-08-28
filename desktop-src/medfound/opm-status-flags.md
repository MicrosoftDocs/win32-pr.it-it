---
description: I flag nella tabella seguente specificano lo stato di una sessione di Output Protection Manager (OPM).
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: Flag di stato OPM (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edc044d9159ad6e6a6e957c4be0228a8e2531164
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480197"
---
# <a name="opm-status-flags"></a>Flag di stato OPM

I flag nella tabella seguente specificano lo stato di una sessione di Output Protection Manager (OPM).




| Costante/valore | Descrizione | 
|----------------|-------------|
| <span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl><dt><strong>OPM_STATUS_NORMAL</strong></dt><dt>0x00</dt></dl> | Stato normale.<br /> | 
| <span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl><dt><strong>OPM_STATUS_LINK_LOST</strong></dt><dt>0x01</dt></dl> | L'integrità della connessione è stata compromessa. Di seguito sono riportati alcuni esempi di eventi che determinano l'impostazione di questo flag da parte del driver:<br /><ul><li>Il driver non può più applicare il livello di protezione corrente.</li><li>Il driver ha rilevato un errore di integrità interno.</li><li>Il connettore tra il computer e il dispositivo di visualizzazione è stato scollegato.</li></ul> | 
| <span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl><dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt><dt>0x02</dt></dl> | La configurazione della connessione è stata modificata. Ad esempio, l'utente ha modificato la modalità di visualizzazione del desktop.<br /> | 
| <span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl><dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt><dt>0x04</dt></dl> | L'adattatore grafico o il driver è stato manomesso.<br /> Questo flag non viene usato in <em>modalità di emulazione COPP.</em> L'output video imposta invece il flag OPM_STATUS_LINK_LOST se rileva manomissioni.<br /> | 
| <span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl><dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt><dt>0x08</dt></dl> | All'output video viene High-Bandwidth un dispositivo HDCP (Digital protezione del contenuto) revocato.<br /> Questo flag di stato può essere restituito da <a href="opm-get-virtual-protection-level.md">una OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> o <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> query. <br /> Il dispositivo revocato potrebbe essere collegato direttamente all'output video o indirettamente tramite un ripetitore HDCP. È necessario un output video per rilevare questa condizione mentre HDCP è abilitato, ma non in caso contrario.<br /> Questo flag non viene usato in <em>modalità di emulazione COPP,</em>perché l'output video non rileva i dispositivi revocati in tale modalità.<br /> | 




## <a name="remarks"></a>Commenti

Alcune di queste costanti sono equivalenti ai valori **dell'enumerazione \_ COPP StatusFlags** usati in Certified Output Protection Protocol (COPP).

## <a name="requirements"></a>Requisiti



| Requisito | valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni OPM](opm-enumerations.md)
</dt> </dl>

 

 




