---
description: I valori vengono usati dal parametro dwOptions di WlxLoggedOutSAS.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (Winwlx.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae482fa7af757a18fc3a38f809befbee94e4d59753cde8e35e01d172bcc065d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914760"
---
# <a name="wlx_logon_option_xxx"></a>OPZIONE DI ACCESSO WLX \_ \_ \_ XXX

\[La costante WLX LOGON OPTION XXX non è più disponibile per l'uso a Windows \_ \_ Server \_ 2008 e Windows Vista.\]

I **valori WLX \_ LOGON OPTION \_ \_ XXX** vengono usati dal *parametro dwOptions* [**di WlxLoggedOutSAS.**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 

Al completamento dell'accesso, la DLL GINA può usare questo valore per specificare l'opzione seguente.



| Costante                                                                                                                                                                                          | Descrizione                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <dt>**WLX \_ LOGON \_ OPT \_ NO \_ PROFILE**</dt> </dl> | Specifica che Winlogon non deve caricare un profilo per l'utente connesso. In questo caso, la DLL GINA carica il profilo o l'utente non ha bisogno di un profilo.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                |
| Fine del supporto client<br/>    | Windows XP<br/>                                                               |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winwlx.h</dt> </dl> |



 

 




