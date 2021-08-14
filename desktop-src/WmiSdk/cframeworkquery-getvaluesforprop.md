---
description: Il metodo GetValuesForProp restituisce tutti i valori per una determinata proprietà generata da tale proprietà così come appare all'interno della query.
audience: developer
ms.assetid: b5ed4b48-f622-4a55-897d-d800ada0270f
ms.tgt_platform: multiple
title: Metodi CFrameworkQuery::GetValuesForProp (FrQuery.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9dc0d51a93986a5ce39326ad7c6139b5dd989ad16f486aeac1b1da03c3b86149
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109405"
---
# <a name="cframeworkquerygetvaluesforprop-methods"></a>Metodi CFrameworkQuery::GetValuesForProp

\[La [**classe CFrameworkQuery**](/windows/win32/api/frquery/nl-frquery-cframeworkquery) fa parte di WMI Provider Framework, che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi devono essere usate](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) per tutti i nuovi progetti di sviluppo.\]

Il **metodo GetValuesForProp** restituisce tutti i valori per una determinata proprietà generata da tale proprietà così come appare all'interno della query.

Ad esempio, una chiamata a **GetValuesForProp**(L"Name", sa) restituisce la matrice *sa*, che contiene tutti i valori di "Name" che richiedono l'invio di istanze per soddisfare la query. Se *sa* contiene {"a","b"}, tutte le istanze in cui "Name=a" più tutte le istanze in cui "Name=b" devono essere inviate nuovamente per soddisfare completamente la query.

Se i vincoli su "Name" non sono sufficientemente limitanti, viene restituita una matrice *sa* vuota.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                                                             | Descrizione                                                                                                                        |
|:-----------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [**GetValuesForProp(CHStringArray&, LPCWSTR)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_chstringarray_))                      | Restituisce tutti i valori per una determinata proprietà generata da tale proprietà così come appare all'interno della query.<br/> |
| [**GetValuesForProp(LPCWSTR, std::vector &lt; \_ bstr \_ t &gt;&)**](/windows/win32/api/frquery/nf-frquery-cframeworkquery-getvaluesforprop(lpcwstr_std-vector__bstr_t__)) | Restituisce tutti i valori per una determinata proprietà generata da tale proprietà così come appare all'interno della query.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>FrQuery.h (includere FwCommon.h)</dt> </dl>                                                     |
| Libreria<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



�

�
