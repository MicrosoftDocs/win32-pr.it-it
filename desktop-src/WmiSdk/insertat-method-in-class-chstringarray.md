---
description: Il metodo InsertAt inserisce un elemento (o più copie di un elemento) o tutti gli elementi di un'altra matrice in corrispondenza di un indice specificato.
audience: developer
ms.assetid: 1d6355bc-7df2-4aa3-8e47-0239d726ed7d
ms.tgt_platform: multiple
title: Metodi CHStringArray::InsertAt (ChStrArr.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 75332e300987233c0a6f3d6755d27fd7c305a7d86fb6cd9a6143c417222c0dcf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097251"
---
# <a name="chstringarrayinsertat-methods"></a>Metodi CHStringArray::InsertAt

\[La [**classe CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi devono essere usate](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) per tutti i nuovi progetti di sviluppo.\]

Il **metodo InsertAt** inserisce un elemento (o più copie di un elemento) o tutti gli elementi di un'altra matrice in corrispondenza di un indice specificato.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                               | Descrizione                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**InsertAt(int,LPCWSTR,int)**](/previous-versions/windows/desktop/legacy/aa385383(v=vs.85))       | Inserisce uno o più elementi in corrispondenza di un indice specificato in una matrice.<br/>                                               |
| [**InsertAt(int,CHStringArray \* )**](/windows/win32/api/chstrarr/nf-chstrarr-chstringarray-insertat(int_chstringarray)) | Inserisce tutti gli elementi di un altro [**oggetto CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray) in corrispondenza di un indice specificato in una matrice.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>ChStrArr.h (includere FwCommon.h)</dt> </dl>                                                    |
| Libreria<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CHStringArray**](/windows/win32/api/chstrarr/nl-chstrarr-chstringarray)
</dt> </dl>

�

�
