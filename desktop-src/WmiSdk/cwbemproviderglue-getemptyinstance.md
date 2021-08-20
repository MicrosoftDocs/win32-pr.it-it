---
description: Il metodo GetEmptyInstance recupera una singola istanza non popolata della classe specificata.
audience: developer
ms.assetid: 2873b466-3782-4d63-a777-5b25e3fb7615
ms.tgt_platform: multiple
title: Metodi CWbemProviderGlue::GetEmptyInstance (WbemGlue.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 293467b88136ece55bf3a6f1d8faeb583464ef542067b1b296ca061505ead8c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925450"
---
# <a name="cwbemprovidergluegetemptyinstance-methods"></a>Metodi CWbemProviderGlue::GetEmptyInstance

\[La [**classe CWbemProviderGlue**](/windows/win32/api/wbemglue/nl-wbemglue-cwbemproviderglue) fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi devono essere usate](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) per tutti i nuovi progetti di sviluppo.\]

Il **metodo GetEmptyInstance** recupera una singola istanza non popolata della classe specificata.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                                            | Descrizione                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [**GetEmptyInstance(LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr))                            | Recupera una singola istanza non popolata della classe specificata.<br/> |
| [**GetEmptyInstance(MethodContext,LPCWSTR,CInstance,LPCWSTR)**](/windows/win32/api/wbemglue/nf-wbemglue-cwbemproviderglue-getemptyinstance(methodcontext_lpcwstr_cinstance_lpcwstr)) | Recupera una singola istanza non popolata della classe specificata.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>WbemGlue.h (includere FwCommon.h)</dt> </dl>                                                    |
| Libreria<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
