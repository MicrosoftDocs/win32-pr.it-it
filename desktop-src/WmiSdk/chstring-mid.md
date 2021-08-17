---
description: Il metodo Mid estrae una sottostringa di lunghezza nCount caratteri da una stringa CHString, a partire dalla posizione nFirst (in base zero). Il metodo restituisce una copia della sottostringa estratta.
audience: developer
ms.assetid: 2036813b-f991-4ca3-95d3-8bbe858aae09
ms.tgt_platform: multiple
title: Metodi CHString::Mid (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: cbe5b7fc6e3f0d4130e106217c46c82202c230f180dd4c90d09f90073dee08ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319843"
---
# <a name="chstringmid-methods"></a>Metodi CHString::Mid

\[La [**classe CHString**](chstring.md) fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API MI devono essere](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) usate per tutti i nuovi sviluppi.\]

Il **metodo Mid** estrae una sottostringa di lunghezza *nCount* caratteri da una stringa [**CHString,**](chstring.md) a partire dalla posizione *nFirst* (in base zero). Il metodo restituisce una copia della sottostringa estratta.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                        | Descrizione                                                              |
|:----------------------------------------------|:-------------------------------------------------------------------------|
| [**Mid(int,int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int_int)) | Estrae una sottostringa di lunghezza e punto iniziale specificati.<br/> |
| [**Mid(int)**](/windows/win32/api/chstring/nf-chstring-chstring-mid(int))         | Estrae una sottostringa a partire da int.<br/>                        |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>ChString.h (includere FwCommon.h)</dt> </dl>                                                    |
| Libreria<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
