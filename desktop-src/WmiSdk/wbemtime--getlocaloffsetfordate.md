---
description: Il metodo GetLocalOffsetForDate restituisce l'offset in minuti (+ o &\# 8211;) tra GMT e ora locale per l'ora specificata nell'argomento .
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: Metodi WBEMTime::GetLocalOffsetForDate (WbemTime.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 873ccd1bdfbac4e52b9a162da2c5ea639cd1496ea49f921504827d8c684d5cec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118107309"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a>Metodi WBEMTime::GetLocalOffsetForDate

\[La [**classe WBEMTime**](wbemtime.md) fa parte di WMI Provider Framework, che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi devono essere usate](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) per tutti i nuovi progetti di sviluppo.\]

Il **metodo GetLocalOffsetForDate** restituisce l'offset in minuti (+ o ) tra GMT e ora locale per l'ora specificata nell'argomento .

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                           | Descrizione                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| [**GetLocalOffsetForDate(time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))         | L'argomento è un riferimento a **un'ora \_ t**.<br/>  |
| [**GetLocalOffsetForDate(FILETIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))     | L'argomento è un puntatore a **un oggetto FILETIME.**<br/>   |
| [**GetLocalOffsetForDate(struct tm \* )**](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | L'argomento è un puntatore **alla struttura tm.**<br/> |
| [**GetLocalOffsetForDate(SYSTEMTIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime)) | L'argomento è un puntatore a **un oggetto SYSTEMTIME.**<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
