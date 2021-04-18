---
description: Le costanti flag globali vengono usate per abilitare o disabilitare le opzioni dei criteri di risparmio energia dell'utente.
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: Costanti flag globali (PowrProf. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fd31340e3e7daf4f9dd034c3fa2db333680a626
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312049"
---
# <a name="global-flags-constants"></a>Costanti flag globali

Le costanti flag globali vengono usate per abilitare o disabilitare le opzioni dei criteri di risparmio energia dell'utente.



| Costante/valore                                                                                                                                                                                                                                                                                         | Descrizione                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <dt></dt> <dt>0x02</dt> EnableMultiBatteryDisplay </dl> | Abilita o Disabilita lo schermo a più batterie nel contatore di alimentazione del sistema.<br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <dt></dt> <dt>0x04</dt> EnablePasswordLogon </dl>                         | Abilita o Disabilita la richiesta di accesso con password quando il sistema riprende dalla modalità standby o di ibernazione.<br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <dt></dt> <dt>0x01</dt> EnableSysTrayBatteryMeter </dl> | Abilita o Disabilita l'icona del contatore della batteria nella barra delle applicazioni. Quando questo flag è deselezionato, l'icona del contatore della batteria non viene visualizzata.<br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <dt></dt> <dt>0x10</dt> EnableVideoDimDisplay </dl>                 | Abilita o Disabilita il supporto per l'attenuazione dello schermo video quando il sistema passa dall'esecuzione a alimentazione a batteria elettrica.<br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <dt></dt> <dt>0x08</dt> EnableWakeOnRing </dl>                                     | Abilita o Disabilita il supporto per riattivazione ring.<br/>                                                                                               |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                           |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>PowrProf. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_criteri di \_ risparmio energia utente globale \_**](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




