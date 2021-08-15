---
description: Metodo di overload che rilascia la memoria che contiene il percorso.
audience: developer
ms.assetid: 9164d7b2-15b8-4b73-ab8c-68ed45692ea0
ms.tgt_platform: multiple
title: Metodi CObjectPathParser::Free (ObjPath.h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 0e7e5e366d96d4c8b5c6d82f177a480114c5d6356759c8db46389c809aea7137
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118819807"
---
# <a name="cobjectpathparserfree-methods"></a>Metodi CObjectPathParser::Free

\[La [**classe CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser) fa parte del framework del provider WMI che è ora considerato in stato finale e non saranno disponibili altri aggiornamenti, miglioramenti o sviluppo per problemi non correlati alla sicurezza che interessano queste librerie. Le [API MI devono essere usate](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) per tutti i nuovi sviluppi.\]

Metodo di overload che rilascia la memoria che contiene il percorso.

### <a name="overload-list"></a>Elenco di overload



| Metodo                                                                     | Descrizione                                                                          |
|:---------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Free(LPWSTR)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(lpwstr))                     | Rilascia la memoria che contiene il percorso non analizzato.<br/>                      |
| [**Free(ParsedObjectPath)**](/windows/win32/api/objpath/nf-objpath-cobjectpathparser-free(parsedobjectpath)) | Rilascia la memoria che contiene la struttura con il percorso analizzato.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>ObjPath.h (include ObjPath.h)</dt> </dl>                                                      |
| Libreria<br/>                  | <dl> <dt>FrameDyn.lib</dt> </dl>                                                                       |
| DLL<br/>                      | <dl> <dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CObjectPathParser**](/windows/win32/api/objpath/nl-objpath-cobjectpathparser)
</dt> </dl>

�

�
