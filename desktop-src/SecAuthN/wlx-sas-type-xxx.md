---
description: I valori definiscono un tipo di firma di accesso condiviso specifico.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (Winwlx.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 568308d064b576f036d18aaa2d150cb1c6b7f0a2d89ee60d9410fcad123351d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785715"
---
# <a name="wlx_sas_type_xxx"></a>WLX \_ SAS \_ TYPE \_ XXX

\[La costante WLX SAS TYPE XXX non è più disponibile per l'uso a Windows \_ \_ Server \_ 2008 e Windows Vista.\]

I **valori WLX \_ SAS TYPE \_ \_ XXX** definiscono un tipo di firma di accesso condiviso specifico.

> [!Note]  
> LE DLL DELL'APPLICAZIONE vengono ignorate in Windows Vista.

 

Tutti i valori da zero a 127 sono riservati per i tipi definiti da Microsoft. I valori superiori a 127 sono disponibili per i tipi definiti dal cliente. I tipi seguenti vengono passati alle funzioni che hanno *un parametro dwSasType.*



| Costante                                                                                                                                                                                                         | Descrizione                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <dt>**WLX \_ SAS \_ DIGITARE CTRL \_ ALT \_ \_ CANC**</dt> </dl>            | Indica che un utente ha digitato la firma di accesso condiviso standard CTRL+ALT+CANC.<br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <dt>**WLX \_ SAS \_ TYPE \_ SC \_ INSERT**</dt> </dl>                      | Indica che un [*smart card*](../secgloss/s-gly.md) è stato inserito in un dispositivo compatibile.<br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <dt>**WLX \_ SAS \_ TYPE \_ SC \_ REMOVE**</dt> </dl>                      | Indica che un smart card è stato rimosso da un dispositivo compatibile.<br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <dt>**ATTIVITÀ \_ \_ SCRNSVR DI TIPO SAS \_ WLX \_**</dt> </dl> | Indica che l'attività della tastiera o del mouse si è verificata mentre era attiva screen saver sicurezza.<br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <dt>**WLX \_ SAS \_ TYPE \_ SCRNSVR \_ TIMEOUT**</dt> </dl>    | Indica che l'screen saver è stata attivata a causa dell'inattività della tastiera e del mouse.<br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <dt>**TIMEOUT DEL TIPO \_ DI FIRMA DI ACCESSO \_ CONDIVISO WLX \_**</dt> </dl>                             | Indica che non è stato ricevuto alcun input dell'utente entro il periodo di timeout specificato.<br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <dt>**WLX \_ SAS \_ TYPE \_ USER \_ LOGOFF**</dt> </dl>                | Indica che l'utente è disconnesso dal sistema.<br/>                                                                                            |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                |
| Fine del supporto client<br/>    | Windows XP<br/>                                                               |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winwlx.h</dt> </dl> |



 

 
