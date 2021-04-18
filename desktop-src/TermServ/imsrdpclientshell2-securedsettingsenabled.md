---
title: Proprietà SecuredSettingsEnabled di IMsRdpClientShell2
description: Recupera un valore che indica se la pagina Web corrente si trova in un'area di protezione URL attendibile di Internet Explorer.
ms.assetid: 51988473-fff7-4574-bd6e-d05ca452da54
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà SecuredSettingsEnabled
- Servizi Desktop remoto proprietà SecuredSettingsEnabled, interfaccia IMsRdpClientShell2
- Interfaccia IMsRdpClientShell2 Servizi Desktop remoto, proprietà SecuredSettingsEnabled
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.SecuredSettingsEnabled
- IMsRdpClientShell2.get_SecuredSettingsEnabled
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1009759051207db7e6b8d741c1dd91e3de1ffc36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302462"
---
# <a name="imsrdpclientshell2securedsettingsenabled-property"></a>Proprietà IMsRdpClientShell2:: SecuredSettingsEnabled

Recupera un valore che indica se la pagina Web corrente si trova in un'area di protezione URL attendibile di Internet Explorer.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_SecuredSettingsEnabled(
  [out, retval] BOOL *pSecuredSettingsEnabled
);
```



## <a name="property-value"></a>Valore proprietà

Puntatore a un valore booleano che indica se la pagina Web corrente si trova in un'area di sicurezza URL di Internet Explorer attendibile.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                          |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                             |
| DLL<br/>                      | <dl> <dt>MsRdpWebAccess.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientShell2**](imsrdpclientshell2.md)
</dt> </dl>

 

 





