---
title: Proprietà MsRdpWorkspace IMsRdpClientShell2
description: Recupera un puntatore all'interfaccia IMsRdpWorkspace, usata per gestire Connessione RemoteApp e desktop credenziali e connessioni.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Proprietà MsRdpWorkspace Servizi Desktop remoto
- Proprietà MsRdpWorkspace Servizi Desktop remoto, interfaccia IMsRdpClientShell2
- Interfaccia IMsRdpClientShell2 Servizi Desktop remoto , proprietà MsRdpWorkspace
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
ms.openlocfilehash: 6470f51ccae2efb6dc3d44a7b0a2a0310ad4230861d7d86262f34fd312fcfc5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118854435"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a>Proprietà IMsRdpClientShell2::MsRdpWorkspace

Recupera un puntatore [**all'interfaccia IMsRdpWorkspace,**](imsrdpworkspace.md) usata per gestire Connessione RemoteApp e desktop credenziali e connessioni.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a>Valore proprietà

Indirizzo di un puntatore [**all'interfaccia IMsRdpWorkspace.**](imsrdpworkspace.md)

## <a name="remarks"></a>Commenti

[**L'interfaccia IMsRdpWorkspace**](imsrdpworkspace.md) non viene esposta come interfaccia personalizzata. È accessibile solo tramite [i metodi IDispatch.](/windows/desktop/com/exposing-methods-through-idispatch)

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

 

