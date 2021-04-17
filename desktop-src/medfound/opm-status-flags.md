---
description: I flag nella tabella seguente specificano lo stato di una sessione di output Protection Manager (OPM).
ms.assetid: d6d85fd4-e735-4610-93e0-bb2b1782f11b
title: Flag di stato OPM (Opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cbf9d299d6d53a26a61d19372e56e42bd2cdf99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527871"
---
# <a name="opm-status-flags"></a>Flag di stato OPM

I flag nella tabella seguente specificano lo stato di una sessione di output Protection Manager (OPM).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Costante/valore</th>
<th style="text-align: left;">Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_NORMAL"></span><span id="opm_status_normal"></span><dl> <dt><strong>OPM_STATUS_NORMAL</strong></dt> <dt>0x00</dt> </dl></td>
<td style="text-align: left;">Stato normale.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_LINK_LOST"></span><span id="opm_status_link_lost"></span><dl> <dt><strong>OPM_STATUS_LINK_LOST</strong></dt> <dt>0x01</dt> </dl></td>
<td style="text-align: left;">L'integrità della connessione è stata compromessa. Di seguito sono riportati alcuni esempi di eventi che determinano l'impostazione di questo flag da parte del driver:<br/>
<ul>
<li>Il driver non può più applicare il livello di protezione corrente.</li>
<li>Il driver ha rilevato un errore di integrità interna.</li>
<li>Il connettore tra il computer e il dispositivo di visualizzazione è stato scollegato.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_RENEGOTIATION_REQUIRED"></span><span id="opm_status_renegotiation_required"></span><dl> <dt><strong>OPM_STATUS_RENEGOTIATION_REQUIRED</strong></dt> <dt>0x02</dt> </dl></td>
<td style="text-align: left;">La configurazione della connessione è cambiata. Ad esempio, l'utente ha modificato la modalità di visualizzazione del desktop.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="OPM_STATUS_TAMPERING_DETECTED"></span><span id="opm_status_tampering_detected"></span><dl> <dt><strong>OPM_STATUS_TAMPERING_DETECTED</strong></dt> <dt>0x04</dt> </dl></td>
<td style="text-align: left;">La scheda grafica o il driver è stato manomesso.<br/> Questo flag non viene usato in <em>modalità di emulazione Copp</em>. Al contrario, l'output del video imposterà il flag di OPM_STATUS_LINK_LOST se rileva manomissioni.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED"></span><span id="opm_status_revoked_hdcp_device_attached"></span><dl> <dt><strong>OPM_STATUS_REVOKED_HDCP_DEVICE_ATTACHED</strong></dt> <dt>0x08</dt> </dl></td>
<td style="text-align: left;">Un dispositivo con High-Bandwidth protezione del contenuto digitale revocato (HDCP) viene collegato all'output del video.<br/> Questo flag di stato può essere restituito da una query <a href="opm-get-virtual-protection-level.md">OPM_GET_VIRTUAL_PROTECTION_LEVEL</a> o <a href="opm-get-actual-protection-level.md">OPM_GET_ACTUAL_PROTECTION_LEVEL</a> . <br/> Il dispositivo revocato potrebbe essere collegato direttamente all'output del video o indirettamente tramite un Repeater HDCP. È necessario un output video per rilevare questa condizione mentre è abilitata la funzionalità HDCP, ma non in caso contrario.<br/> Questo flag non viene usato in <em>modalità di emulazione Copp</em>, perché l'output del video non rileva i dispositivi revocati in tale modalità.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Commenti

Alcune di queste costanti sono equivalenti ai valori dell'enumerazione **Copp \_ StatusFlags** utilizzata in Certified Output Protocol (Copp).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni di OPM](opm-enumerations.md)
</dt> </dl>

 

 




