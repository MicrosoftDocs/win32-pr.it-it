---
description: Le costanti flag globali vengono usate per abilitare o disabilitare le opzioni dei criteri di risparmio energia dell'utente.
ms.assetid: d98190ef-f70e-4796-960e-ff32d2cf6f4f
title: Costanti flag globali (PowrProf.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2dfd23559959bee72e8572cc700a948df1e92dcdb37a03c41b52cdca4d578c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143535"
---
# <a name="global-flags-constants"></a>Costanti dei flag globali

Le costanti flag globali vengono usate per abilitare o disabilitare le opzioni dei criteri di risparmio energia dell'utente.



| Costante/valore                                                                                                                                                                                                                                                                                         | Descrizione                                                                                                                                        |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="EnableMultiBatteryDisplay"></span><span id="enablemultibatterydisplay"></span><span id="ENABLEMULTIBATTERYDISPLAY"></span><dl> <dt>**EnableMultiBatteryDisplay**</dt> <dt>0x02</dt> </dl> | Abilita o disabilita la visualizzazione di più batteria nel misuratore di alimentazione del sistema.<br/>                                                                 |
| <span id="EnablePasswordLogon"></span><span id="enablepasswordlogon"></span><span id="ENABLEPASSWORDLOGON"></span><dl> <dt>**EnablePasswordLogon**</dt> <dt>0x04</dt> </dl>                         | Abilita o disabilita la richiesta dell'accesso con password quando il sistema viene riattivato dalla modalità standby o ibernazione.<br/>                                         |
| <span id="EnableSysTrayBatteryMeter"></span><span id="enablesystraybatterymeter"></span><span id="ENABLESYSTRAYBATTERYMETER"></span><dl> <dt>**EnableSysTrayBatteryMeter**</dt> <dt>0x01</dt> </dl> | Abilita o disabilita l'icona del contatore della batteria nell'area di notifica. Quando questo flag è deselezionato, l'icona del contatore della batteria non viene visualizzata.<br/>      |
| <span id="EnableVideoDimDisplay"></span><span id="enablevideodimdisplay"></span><span id="ENABLEVIDEODIMDISPLAY"></span><dl> <dt>**EnableVideoDimDisplay**</dt> <dt>0x10</dt> </dl>                 | Abilita o disabilita il supporto per l'attenuazione della visualizzazione video quando il sistema cambia dall'esecuzione dell'alimentazione CA all'alimentazione a batteria.<br/> |
| <span id="EnableWakeOnRing"></span><span id="enablewakeonring"></span><span id="ENABLEWAKEONRING"></span><dl> <dt>**EnableWakeOnRing**</dt> <dt>0x08</dt> </dl>                                     | Abilita o disabilita il supporto della riattivazione dell'anello.<br/>                                                                                               |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                           |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>PowrProf.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CRITERI \_ DI RISPARMIO ENERGIA PER GLI UTENTI \_ \_ GLOBALI**](/windows/desktop/api/PowrProf/ns-powrprof-global_user_power_policy)
</dt> </dl>

 

 




