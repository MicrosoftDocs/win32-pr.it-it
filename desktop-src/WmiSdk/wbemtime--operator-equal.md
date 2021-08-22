---
description: Gli operatori di assegnazione della classe WBEMTime vengono sottoposti a overload per facilitare le conversioni tra vari formati di Windows e in fase di esecuzione ANSI C. Le diverse firme di overload sono elencate di seguito.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: Operatori WBEMTime::operator= (WbemTime.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 321ca0ba75d40389fbd6eb2ba70dc67a9b8e16afd3b5390bbc9ec61bd875c79a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502901"
---
# <a name="wbemtimeoperator-operators"></a>Operatori WBEMTime::operator=

\[La [**classe WBEMTime**](wbemtime.md) fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API MI devono essere](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) usate per tutti i nuovi sviluppi.\]

Gli [**operatori di assegnazione della classe WBEMTime**](wbemtime.md) vengono sottoposti a overload per facilitare le conversioni tra Windows e i formati di run-time ANSI C. Le diverse firme di overload sono elencate di seguito.

### <a name="overload-list"></a>Elenco di overload



| Operatore                                                                     | Descrizione                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**operator=(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))               | Converte un **BSTR** nel **formato WBEMTime.**<br/>         |
| [**operator=(time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))        | Converte **time \_ t** nel **formato WBEMTime.**<br/>        |
| [**operator=(FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))     | Converte **FILETIME** nel **formato WBEMTime.**<br/>       |
| [**operator=(struct tm&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))   | Converte una **struttura tm** nel **formato WBEMTime.**<br/> |
| [**operator=(SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_)) | Converte **SYSTEMTIME nel** **formato WBEMTime.**<br/>     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
