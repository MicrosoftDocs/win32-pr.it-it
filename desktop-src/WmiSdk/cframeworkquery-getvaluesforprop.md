---
description: Il metodo GetValuesForProp restituisce tutti i valori per una determinata proprietà che vengono generati da tale proprietà così come vengono visualizzati all'interno della query.
audience: developer
ms.assetid: b5ed4b48-f622-4a55-897d-d800ada0270f
ms.tgt_platform: multiple
title: 'Metodi CFrameworkQuery:: GetValuesForProp (FrQuery. h)'
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b5fd9dbc22289843141c517203809045abbf05a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232639"
---
# <a name="cframeworkquerygetvaluesforprop-methods"></a>Metodi CFrameworkQuery:: GetValuesForProp

\[La classe [**CFrameworkQuery**](/windows/win32/api/frquery/nl-frquery-cframeworkquery) fa parte del Framework del provider WMI, che è ora considerato nello stato finale e non sono disponibili ulteriori sviluppi, miglioramenti o aggiornamenti per i problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) devono essere usate per tutte le nuove attività di sviluppo.\]

Il metodo **GetValuesForProp** restituisce tutti i valori per una determinata proprietà che vengono generati da tale proprietà così come vengono visualizzati all'interno della query.

Ad esempio, una chiamata a **GetValuesForProp**(L "Name", SA) restituisce la matrice *sa*, che contiene tutti i valori di "Name" che richiedono che le istanze vengano restituite per soddisfare la query. Se *sa* contiene {"a", "b"}, tutte le istanze in cui "Name = a" e tutte le istanze in cui "Name = b" devono essere restituite per soddisfare completamente la query.

Se i vincoli su "Name" non sono sufficientemente limitati, viene restituita una matrice *sa* vuota.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                             | Descrizione                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetValuesForProp (CHStringArray&, LPCWSTR)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_chstringarray_))                      | Restituisce tutti i valori per una determinata proprietà che vengono generati da tale proprietà così come vengono visualizzati all'interno della query.<br/> |
| [**GetValuesForProp (LPCWSTR, std:: Vector &lt; \_ bstr \_ t &gt;&)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_std-vector__bstr_t__)) | Restituisce tutti i valori per una determinata proprietà che vengono generati da tale proprietà così come vengono visualizzati all'interno della query.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>FrQuery. h (include FwCommon. h)</dt> </dl>                                                     |
| Libreria<br/>                  | <dl> <dt>FrameDyn. lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
