---
description: Il metodo GetLocalOffsetForDate restituisce l'offset in minuti (+ o &\# 8211;) tra GMT e l'ora locale per il tempo fornito nell'argomento.
audience: developer
ms.assetid: 15cc5f45-604c-4335-bcd3-92d62dc15420
ms.tgt_platform: multiple
title: 'Metodi WBEMTime:: GetLocalOffsetForDate (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e2c10cd076e18a803f0cb22b2798c09091cc70b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883505"
---
# <a name="wbemtimegetlocaloffsetfordate-methods"></a>Metodi WBEMTime:: GetLocalOffsetForDate

\[La classe [**WBEMTime**](wbemtime.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]

Il metodo **GetLocalOffsetForDate** restituisce l'offset in minuti (+ o) tra GMT e ora locale per il tempo fornito nell'argomento.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                           | Descrizione                                           |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| [**GetLocalOffsetForDate (Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(consttime_t_))         | Argument è un riferimento a un' **ora \_ t**.<br/>  |
| [**GetLocalOffsetForDate (FILETIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constfiletime))     | Argument è un puntatore a un oggetto **FILETIME**.<br/>   |
| [**GetLocalOffsetForDate (struct TM \* )**](/windows/desktop/api/wbemtime/nf-wbemtime-wbemtime-getstructtm)   | Argument è un puntatore alla struttura **TM** .<br/> |
| [**GetLocalOffsetForDate (SYSTEMTIME \* )**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-getlocaloffsetfordate(constsystemtime)) | Argument è un puntatore a un oggetto **SYSTEMTIME**.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
