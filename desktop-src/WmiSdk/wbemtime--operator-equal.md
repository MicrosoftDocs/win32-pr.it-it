---
description: Gli operatori di assegnazione della classe WBEMTime sono in overload per semplificare le conversioni tra diversi formati di runtime di Windows e ANSI C. Di seguito sono elencate le diverse firme di overload.
audience: developer
ms.assetid: 47978056-d46f-4f8f-99cb-8463b44da7cf
ms.tgt_platform: multiple
title: 'Operatori WBEMTime:: operator = (WbemTime. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 637cc76e776060a4c36a12a9b26bd09a6c231a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349611"
---
# <a name="wbemtimeoperator-operators"></a>Operatori WBEMTime:: operator =

\[La classe [**WBEMTime**](wbemtime.md) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]

Gli operatori di assegnazione della classe [**WBEMTime**](wbemtime.md) sono in overload per semplificare le conversioni tra diversi formati di runtime di Windows e ANSI C. Di seguito sono elencate le diverse firme di overload.

### <a name="overload-list"></a>Elenco di overload



| Operatore                                                                     | Descrizione                                                    |
|:-----------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**operatore = (BSTR)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constbstr))               | Converte un valore **BSTR** nel formato **WBEMTime** .<br/>         |
| [**operator = (Time \_ t&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttime_t_))        | Converte l' **ora \_ t** nel formato **WBEMTime** .<br/>        |
| [**operator = (FILETIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constfiletime_))     | Converte **FILETIME** nel formato **WBEMTime** .<br/>       |
| [**operator = (struct TM&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(consttm_))   | Converte una struttura **TM** nel formato **WBEMTime** .<br/> |
| [**operatore = (SYSTEMTIME&)**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-assign(constsystemtime_)) | Converte **SYSTEMTIME** nel formato **WBEMTime** .<br/>     |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
