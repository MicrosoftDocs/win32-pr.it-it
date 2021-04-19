---
description: La classe WBEMTime facilita le conversioni tra diversi formati di runtime di Windows e ANSI C. Per ulteriori informazioni, vedere anche metodi della classe WBEMTimeSpan.
ms.assetid: b633bc8c-9d02-4bcf-8528-10773fb5ae7a
ms.tgt_platform: multiple
title: Classe WBEMTime (WbemTime.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WBEMTime
api_type:
- COM
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 5d2f06b06db998dc18a876e0e5534e1d86c6ae89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318849"
---
# <a name="wbemtime-class"></a>Classe WBEMTime

\[La classe **WBEMTime** fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]

La classe **WBEMTime** facilita le conversioni tra diversi formati di runtime di Windows e ANSI C. Per ulteriori informazioni, vedere anche [**metodi della classe WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan).

## <a name="members"></a>Membri

La classe **WBEMTime** dispone di questi tipi di membri:

-   [Costruttori](#constructors)
-   [Metodi](#methods)

### <a name="constructors"></a>Costruttori

La classe **WBEMTime** dispone di questi costruttori.



| Costruttore                           | Descrizione                                                                                                   |
|:--------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**WBEMTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr)) | Costruttore che semplifica le conversioni tra diversi formati di runtime di Windows e ANSI C.<br/> |



 

### <a name="methods"></a>Metodi

La classe **WBEMTime** dispone di questi metodi.



| Metodo                                                           | Descrizione                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Deselezionare**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)                                  | Imposta l'ora dell'oggetto **WBEMTime** su un'ora non valida.<br/>                                                                |
| [**GetBSTR**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)                              | Visualizza l'ora come valore **BSTR** .<br/>                                                                                      |
| [**GetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)                              | Ottiene l'ora come valore **BSTR** nel formato DateTime CIM.<br/>                                                                   |
| [**GetDMTFNonNtfs**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)                | Ottiene una data DMTF basata su un formato FAT o [data e ora](date-and-time-format.md) in cui l'ora UTC non è nota.<br/> |
| [**GetFileTime ha provocato**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)                      | Ottiene l'ora come struttura **FILETIME** MFC.<br/>                                                                             |
| [**GetLocalOffsetForDate**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85)) | Di overload. Restituisce l'offset in minuti (+ o-) tra GMT e l'ora locale per il tempo fornito nell'argomento.<br/>         |
| [**GetStructtm**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)                      | Ottiene l'ora come struttura **TM** della fase di esecuzione del linguaggio ANSI C.<br/>                                                                |
| [**GetSYSTEMTIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)                  | Ottiene l'ora come struttura **SYSTEMTIME** MFC.<br/>                                                                           |
| [**GetTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)                              | Ottiene l'ora come intero a 64 bit.<br/>                                                                                          |
| [**GetTime \_ t**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)                         | Ottiene l'ora come variabile di runtime ANSI C \_ t.<br/>                                                                       |
| [**IsOk**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)                                    | Indica se l'oggetto **WBEMTime** rappresenta un'ora valida.<br/>                                                          |
| [**SetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)                              | Imposta l'ora nell'oggetto **WBEMTime** in formato DateTime CIM.<br/>                                                            |



 

## <a name="wbemtime-overloaded-operators"></a>Operatori di overload WBEMTime

L'oggetto **WBEMTime** definisce gli operatori di overload seguenti.



| Operatori di overload WBEMTime                                                                                                                                                                                                                                                                                                                                                                                                                                        | Descrizione                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**operatore =**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | Operatore di *assegnazione* facilita le conversioni tra diversi formati di runtime di Windows e ANSI C.                           |
| [**operatore +**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-add)                                                                                                                                                                                                                                                                                                                                                                                                                         | L'operatore di *addizione* incrementa l'ora di un oggetto in base a un intervallo di tempo. Il risultato viene restituito in un nuovo oggetto **WBEMTime** .              |
| [**operatore + =**](/windows/win32/api/directxmath/nf-directxmath-operator-add-assign)                                                                                                                                                                                                                                                                                                                                                                                                                  | L'operatore *Add-and-assign* incrementa l'ora di un oggetto in base a un intervallo di tempo.                                                             |
| [**operatore**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | L'operatore di *sottrazione* decrementa l'ora di un oggetto in base all'ora di un altro oggetto. Il risultato viene restituito in un nuovo oggetto **WBEMTime** . |
| [**operatore-=**](/windows/win32/api/directxmath/nf-directxmath-operator-sub-assign)                                                                                                                                                                                                                                                                                                                                                                                                                 | L'operatore *Subtract-and-assign* decrementa l'ora di un oggetto in base a un intervallo di tempo.                                                        |
| [**operatore = =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to)[**operatore! =**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)<br/> [**operatore >**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)<br/> [**operatore >=**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)<br/> [**operatore <**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)<br/> [**operatore <=**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)<br/> | Gli operatori di confronto confrontano due oggetti **WBEMTime** .                                                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>WbemTime. h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



 

