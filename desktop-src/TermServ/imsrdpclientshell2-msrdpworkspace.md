---
title: Proprietà MsRdpWorkspace di IMsRdpClientShell2
description: Recupera un puntatore all'interfaccia IMsRdpWorkspace, che consente di gestire le credenziali e le connessioni Connessione RemoteApp e desktop.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà MsRdpWorkspace
- Servizi Desktop remoto proprietà MsRdpWorkspace, interfaccia IMsRdpClientShell2
- Interfaccia IMsRdpClientShell2 Servizi Desktop remoto, proprietà MsRdpWorkspace
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91eadd3f1b422e3da96d5bcd3a5178a2a0b0eb52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742399"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a>Proprietà IMsRdpClientShell2:: MsRdpWorkspace

Recupera un puntatore all'interfaccia [**IMsRdpWorkspace**](imsrdpworkspace.md) , che consente di gestire le credenziali e le connessioni connessione RemoteApp e desktop.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a>Valore proprietà

Indirizzo di un puntatore all'interfaccia [**IMsRdpWorkspace**](imsrdpworkspace.md) .

## <a name="remarks"></a>Commenti

L'interfaccia [**IMsRdpWorkspace**](imsrdpworkspace.md) non è esposta come interfaccia personalizzata. È accessibile solo tramite metodi [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) .

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

 

