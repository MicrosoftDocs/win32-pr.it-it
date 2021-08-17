---
description: Il metodo CInstance::SetCHString imposta una proprietà stringa.
ms.assetid: a75b574d-9ee7-4930-a003-5d71c5f1d687
ms.tgt_platform: multiple
title: Metodi CInstance::SetCHString (Instance.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- DllExport
api_location:
- FrameDynOS.dll
- FrameDyn.dll
ms.openlocfilehash: 3f53081c284ea60f77039b12c6bb43928ea45c306a0ddfbb1cc6e8c804661c3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925777"
---
# <a name="cinstancesetchstring-methods"></a>Metodi CInstance::SetCHString

\[La [**classe CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance) fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API mi devono essere usate](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) per tutti i nuovi progetti di sviluppo.\]

Il **metodo CInstance::SetCHString** imposta una proprietà stringa.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                                           | Descrizione                        |
|:-------------------------------------------------------------------------------------------------|:-----------------------------------|
| [**SetCHString(LPCWSTR, LPCSTR)**](/windows/desktop/api/Instance/nf-instance-cinstance-setchstring(lpcwstr_lpcstr))                   | Imposta una proprietà stringa.<br/> |
| [**SetCHString(LPCWSTR, const CHString&)**](/windows/win32/api/instance/nf-instance-cinstance-setchstring(lpcwstr_constchstring_)) | Imposta una proprietà stringa.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>Instance.h (includere FwCommon.h)</dt> </dl>                                                    |
| Libreria<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CInstance**](/windows/desktop/api/Instance/nl-instance-cinstance)
</dt> </dl>

 

