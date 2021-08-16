---
description: Il metodo Find cerca in una stringa la prima corrispondenza di una sottostringa.
audience: developer
ms.assetid: 98a7c5ad-5bc7-4918-b978-45d2b439f250
ms.tgt_platform: multiple
title: Metodi CHString::Find (ChString.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a7f326b202d107dc192683517508446b3c785266c675e5cf27d92577311d453a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319995"
---
# <a name="chstringfind-methods"></a>Metodi CHString::Find

\[La [**classe CHString**](chstring.md) fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API MI devono essere](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) usate per tutti i nuovi sviluppi.\]

Il **metodo Find** cerca in una stringa la prima corrispondenza di una sottostringa.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                          | Descrizione                                             |
|:------------------------------------------------|:--------------------------------------------------------|
| [**Find(WCHAR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr))     | Cerca **WSTR** in questa stringa.<br/>    |
| [**Find(LPCWSTR)**](/windows/win32/api/chstring/nf-chstring-chstring-find(lpcwstr)) | Cerca **LPCWSTR** in questa stringa.<br/> |



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
