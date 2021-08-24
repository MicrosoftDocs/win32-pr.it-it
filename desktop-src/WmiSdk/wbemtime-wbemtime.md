---
description: Il costruttore della classe WBEMTime facilita le conversioni tra Windows e i formati di run-time C ANSI.
audience: developer
ms.assetid: 8b0ce221-2186-4aed-a474-00f88cef6350
ms.tgt_platform: multiple
title: Costruttori WBEMTime::WBEMTime (WbemTime.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ac02e3ee2a7a77ed1cc2cc9157b0d6c191563f234bf594cb53029a76e76f0137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757621"
---
# <a name="wbemtimewbemtime-constructors"></a>Costruttori WBEMTime::WBEMTime

\[La [**classe WBEMTime**](wbemtime.md) fa parte di WMI Provider Framework, che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi devono essere usate](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) per tutti i nuovi progetti di sviluppo.\]

Il **costruttore della classe WBEMTime** facilita le conversioni tra Windows e i formati di run-time C ANSI.

### <a name="overload-list"></a>Elenco di overload



| Costruttore                                                                 | Descrizione                                                               |
|:----------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**WBEMTime()**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                                   | Crea un oggetto ora non inizializzato.<br/>                          |
| [**WBEMTime(BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constbstr))                           | Inizializza il nuovo oggetto time sul valore nel parametro .<br/> |
| [**WBEMTime(const time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttime_t_))        | Inizializza il nuovo oggetto time sul valore nel parametro .<br/> |
| [**WBEMTime(const struct tm)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(consttm_))    | Inizializza il nuovo oggetto time sul valore nel parametro .<br/> |
| [**WBEMTime(const FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constfiletime_))     | Inizializza il nuovo oggetto time sul valore nel parametro .<br/> |
| [**WBEMTime(const SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-wbemtime(constsystemtime_)) | Inizializza il nuovo oggetto time sul valore nel parametro .<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
