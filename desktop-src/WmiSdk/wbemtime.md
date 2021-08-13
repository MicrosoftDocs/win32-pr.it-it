---
description: La classe WBEMTime facilita le conversioni tra Windows e i formati di run-time ANSI C. Per altre informazioni, vedere anche Metodi della classe WBEMTimeSpan.
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
ms.openlocfilehash: 16b4e8933113386e877aec23313f74695b321f932c10f0e2730bcf5888675cc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553247"
---
# <a name="wbemtime-class"></a>Classe WBEMTime

\[La **classe WBEMTime** fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API MI devono essere](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) usate per tutti i nuovi sviluppi.\]

La **classe WBEMTime** facilita le conversioni tra Windows e i formati di run-time ANSI C. Per altre informazioni, vedere anche Metodi della classe [**WBEMTimeSpan**](/windows/desktop/api/WbemTime/nl-wbemtime-wbemtimespan).

## <a name="members"></a>Membri

La **classe WBEMTime** ha questi tipi di membri:

-   [Costruttori](#constructors)
-   [Metodi](#methods)

### <a name="constructors"></a>Costruttori

La **classe WBEMTime** ha questi costruttori.



| Costruttore                           | Descrizione                                                                                                   |
|:--------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**WBEMTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-wbemtime(constbstr)) | Costruttore che facilita le conversioni tra Windows e i formati di run-time ANSI C.<br/> |



 

### <a name="methods"></a>Metodi

La **classe WBEMTime** include questi metodi.



| Metodo                                                           | Descrizione                                                                                                                            |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [**Cancella**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-clear)                                  | Imposta l'ora **nell'oggetto WBEMTime** su un'ora non valida.<br/>                                                                |
| [**GetBSTR**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getbstr)                              | Presenta l'ora come **valore BSTR.**<br/>                                                                                      |
| [**GetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtf)                              | Ottiene l'ora come **valore BSTR** in formato datetime CIM.<br/>                                                                   |
| [**GetDMTFNonNtfs**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getdmtfnonntfs)                | Ottiene una data DMTF basata su un formato FAT o di data [e ora](date-and-time-format.md) in cui l'ora UTC non è nota.<br/> |
| [**GetFILETIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getfiletime)                      | Ottiene l'ora come struttura **FILETIME** MFC.<br/>                                                                             |
| [**GetLocalOffsetForDate**](/previous-versions/windows/desktop/legacy/aa394049(v=vs.85)) | Di overload. Restituisce l'offset in minuti (+ o -) tra GMT e ora locale per l'ora specificata nell'argomento .<br/>         |
| [**GetStructtm**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getstructtm)                      | Ottiene l'ora come struttura tm dello **struct** di run-time ANSI C.<br/>                                                                |
| [**GetSYSTEMTIME**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-getsystemtime)                  | Ottiene l'ora come struttura **SYSTEMTIME** MFC.<br/>                                                                           |
| [**GetTime**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime)                              | Ottiene l'ora come intero a 64 bit.<br/>                                                                                          |
| [**Gettime \_ t**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-gettime_t)                         | Ottiene l'ora come variabile t in fase di esecuzione ANSI \_ C.<br/>                                                                       |
| [**IsOk**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-isok)                                    | Indica se **l'oggetto WBEMTime** rappresenta un'ora valida.<br/>                                                          |
| [**SetDMTF**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-setdmtf)                              | Imposta l'ora **nell'oggetto WBEMTime** in formato datetime CIM.<br/>                                                            |



 

## <a name="wbemtime-overloaded-operators"></a>Operatori di overload WBEMTime

**L'oggetto WBEMTime** definisce gli operatori di overload seguenti.



| Operatori di overload WBEMTime                                                                                                                                                                                                                                                                                                                                                                                                                                        | Descrizione                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**operatore =**](/previous-versions/windows/desktop/legacy/aa394050(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | *L'operatore* di assegnazione facilita le conversioni tra Windows e i formati di run-time ANSI C.                           |
| [**operatore +**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-add)                                                                                                                                                                                                                                                                                                                                                                                                                         | *L'operatore* di addizione incrementa il tempo di un oggetto di un intervallo di tempo. Il risultato viene restituito in un nuovo **oggetto WBEMTime.**              |
| [**operatore +=**](/windows/win32/api/directxmath/nf-directxmath-operator-add-assign)                                                                                                                                                                                                                                                                                                                                                                                                                  | *L'operatore Add-and-assign* incrementa il tempo di un oggetto di un intervallo di tempo.                                                             |
| [**operatore -**](/previous-versions/windows/desktop/legacy/aa394051(v=vs.85))                                                                                                                                                                                                                                                                                                                                                                                                                       | *L'operatore* di sottrazione decrementa il tempo di un oggetto in base all'ora di un altro oggetto. Il risultato viene restituito in un nuovo **oggetto WBEMTime.** |
| [**operator -=**](/windows/win32/api/directxmath/nf-directxmath-operator-sub-assign)                                                                                                                                                                                                                                                                                                                                                                                                                 | *L'operatore subtract-and-assign* decrementa il tempo di un oggetto di un intervallo di tempo.                                                        |
| [**operatore ==**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-equal-equal-to)[**operatore !=**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-not-equal-to)<br/> [**operatore >**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than)<br/> [**operatore >=**](/windows/desktop/api/WbemTime/nf-wbemtime-wbemtime-operator-greater-than-equal-to)<br/> [**operatore <**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than)<br/> [**operatore <=**](/windows/win32/api/wbemtime/nf-wbemtime-wbemtime-operator-less-than-equal-to)<br/> | Gli operatori di confronto confrontano **due oggetti WBEMTime.**                                                                            |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>WbemTime.h</dt> </dl>                                                                         |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



 

