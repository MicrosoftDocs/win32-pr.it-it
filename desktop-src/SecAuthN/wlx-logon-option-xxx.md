---
description: I valori vengono usati dal parametro dwOptions di WlxLoggedOutSAS.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (Winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347136"
---
# <a name="wlx_logon_option_xxx"></a>\_opzione di accesso wlx \_ \_ xxx

\[L' \_ \_ opzione di accesso wlx \_ xxx Constant non è più disponibile per l'uso a partire da Windows Server 2008 e Windows Vista.\]

I **valori \_ \_ \_ xxx dell'opzione di accesso wlx** vengono usati dal parametro *dwOptions* di [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 

Una volta eseguito correttamente l'accesso, la DLL GINA può usare questo valore per specificare l'opzione seguente.



| Costante                                                                                                                                                                                          | Descrizione                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <dt>**\_ \_ \_ nessun profilo di accesso \_ a wlx**</dt> </dl> | Specifica che Winlogon non deve caricare un profilo per l'utente connesso. In questo caso, la DLL GINA caricherà il profilo o l'utente non necessita di un profilo.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                         |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                |
| Fine del supporto client<br/>    | Windows XP<br/>                                                               |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                      |
| Intestazione<br/>                   | <dl> <dt>Winwlx. h</dt> </dl> |



 

 




