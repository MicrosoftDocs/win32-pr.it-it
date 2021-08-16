---
description: Ognuno dei costruttori seguenti inizializza un nuovo oggetto CHString con i dati specificati.
audience: developer
ms.assetid: d49e1600-d5d4-4c44-81c5-1b8c53b768de
ms.tgt_platform: multiple
title: Costruttori CHString::CHString (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 80ce10988fc335c5a16eff8507346dbcdffd6fa70f75d74fb48d3f84b0e2332b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118320049"
---
# <a name="chstringchstring-constructors"></a>Costruttori CHString::CHString

\[La [**classe CHString**](chstring.md) fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi devono essere usate](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) per tutti i nuovi progetti di sviluppo.\]

Ognuno dei costruttori seguenti inizializza un nuovo [**oggetto CHString**](chstring.md) con i dati specificati.

### <a name="overload-list"></a>Elenco di overload



| Costruttore                                                                        | Descrizione                                                  |
|:-----------------------------------------------------------------------------------|:-------------------------------------------------------------|
| [**CHString()**](/windows/win32/api/rrascfg/nn-rrascfg-ieapproviderconfig)                                          | Crea un oggetto CHString vuoto.<br/>                 |
| [**CHString(LPCSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcstr))                              | Inizializza con il valore LPCSTR.<br/>                |
| [**CHString(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr))                            | Inizializza con il valore LPCWSTR.<br/>               |
| [**CHString(WCHAR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(wchar_int))                        | Inizializza con copie int del valore WCHAR.<br/>   |
| [**CHString(LPCWSTR,int)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(lpcwstr_int))                    | Inizializza con copie int del valore LPCWSTR.<br/> |
| [**CHString(const CHString&)**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constchstring_))            | Replica il parametro CHString.<br/>                |
| [**CHString(const unsigned char \* )**](/windows/win32/api/chstring/nf-chstring-chstring-chstring(constunsignedchar)) | Inizializza con il valore a cui punta char \* .<br/>  |



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
