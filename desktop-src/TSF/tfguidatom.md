---
title: TfGuidAtom (msctf. h)
description: Il tipo di dati TfGuidAtom identifica un GUID in TSF. Un TfGuidAtom viene ottenuto chiamando ITfCategoryMgr RegisterGUID.
ms.assetid: 91696612-1829-4052-81d1-eddc23278d35
keywords:
- TfGuidAtom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c05d3c9a3bc7d725bf2df38069d7bc6112dad08b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104118934"
---
# <a name="tfguidatom"></a>TfGuidAtom

Il tipo di dati **TfGuidAtom** identifica un **GUID** in TSF. Un **TfGuidAtom** viene ottenuto chiamando [**ITfCategoryMgr:: RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).


```C++
typedef DWORD TfGuidAtom;
```



## <a name="remarks"></a>Commenti

Un valore **TfGuidAtom** è valido solo all'interno del processo da cui viene chiamato **ITfCategoryMgr:: RegisterGUID** .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Componente ridistribuibile<br/>          | TSF 1,0 su Windows 2000 Professional<br/>                                      |
| Intestazione<br/>                   | <dl> <dt>Msctf. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msctf. idl</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITfCategoryMgr:: GetGuid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[**ITfCategoryMgr::IsEqualTfGuidAtom**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-isequaltfguidatom)
</dt> <dt>

[**ITfCategoryMgr::RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> </dl>

 

 





