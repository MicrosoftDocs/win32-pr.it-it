---
description: I valori definiscono un tipo di firma di accesso condiviso specifico.
ms.assetid: c0a1269b-f9d4-49e1-89ca-526fef148134
title: WLX_SAS_TYPE_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a75c7d7a71855700c4c8c233db3cfc18e06b9d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315846"
---
# <a name="wlx_sas_type_xxx"></a>WLX \_ SAS \_ tipo \_ xxx

\[La \_ \_ \_ costante di tipo xxx della firma di accesso condiviso non è più disponibile per l'uso a partire da Windows Server 2008 e Windows Vista.\]

I valori di **\_ \_ tipo \_ xxx** di firma di accesso condiviso definiscono un tipo di firma di accesso condiviso specifico

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 

Tutti i valori da zero a 127 sono riservati ai tipi definiti da Microsoft. I valori superiori a 127 sono disponibili per i tipi definiti dal cliente. I tipi seguenti vengono passati alle funzioni che hanno un parametro *dwSasType* .



| Costante                                                                                                                                                                                                         | Descrizione                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_SAS_TYPE_CTRL_ALT_DEL"></span><span id="wlx_sas_type_ctrl_alt_del"></span><dl> <dt>**tipo di firma di accesso condiviso di WLX \_ \_ \_ CTRL \_ ALT \_ Canc**</dt> </dl>            | Indica che un utente ha digitato la firma di accesso condiviso standard CTRL + ALT + CANC.<br/>                                                                                     |
| <span id="WLX_SAS_TYPE_SC_INSERT"></span><span id="wlx_sas_type_sc_insert"></span><dl> <dt>**tipo di firma di accesso condiviso di WLX \_ SAS \_ \_ \_**</dt> </dl>                      | Indica che una [*Smart Card*](../secgloss/s-gly.md) è stata inserita in un dispositivo compatibile.<br/> |
| <span id="WLX_SAS_TYPE_SC_REMOVE"></span><span id="wlx_sas_type_sc_remove"></span><dl> <dt>**tipo di firma di accesso condiviso di WLX \_ \_ \_ SC \_ Remove**</dt> </dl>                      | Indica che una smart card è stata rimossa da un dispositivo compatibile.<br/>                                                                        |
| <span id="WLX_SAS_TYPE_SCRNSVR_ACTIVITY"></span><span id="wlx_sas_type_scrnsvr_activity"></span><dl> <dt>**\_ \_ attività SCRNSVR di tipo SAS \_ di \_ wlx**</dt> </dl> | Indica che si è verificata un'attività della tastiera o del mouse mentre era attiva una screen saver sicura.<br/>                                                    |
| <span id="WLX_SAS_TYPE_SCRNSVR_TIMEOUT"></span><span id="wlx_sas_type_scrnsvr_timeout"></span><dl> <dt>**\_ \_ \_ timeout SCRNSVR tipo SAS \_ di wlx**</dt> </dl>    | Indica che screen saver si è verificata l'attivazione a causa di inattività della tastiera e del mouse.<br/>                                                     |
| <span id="WLX_SAS_TYPE_TIMEOUT"></span><span id="wlx_sas_type_timeout"></span><dl> <dt>**\_ \_ timeout tipo di SAS di WLX \_**</dt> </dl>                             | Indica che non è stato ricevuto alcun input da parte dell'utente entro il periodo di timeout specificato.<br/>                                                               |
| <span id="WLX_SAS_TYPE_USER_LOGOFF"></span><span id="wlx_sas_type_user_logoff"></span><dl> <dt>**\_disconnessione \_ utente tipo di SAS \_ wlx \_**</dt> </dl>                | Indica che l'utente è stato disconnesso dal sistema.<br/>                                                                                            |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Fine del supporto client<br/>    | Windows XP<br/>                                                               |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winwlx. h</dt> </dl> |



 

 
