---
title: Proprietà IsRemoteProgramClientInstalled di IMsRdpClientShell
description: Recupera un valore che indica se Connessione Desktop remoto (RDC) supporta la Windows RemoteApp di Server 2008 R2.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- Proprietà IsRemoteProgramClientInstalled Servizi Desktop remoto
- Proprietà IsRemoteProgramClientInstalled Servizi Desktop remoto, interfaccia IMsRdpClientShell
- Interfaccia IMsRdpClientShell Servizi Desktop remoto proprietà , IsRemoteProgramClientInstalled
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3073bb9a9e5890ff7a6a46bb9ea0c03964bf54f1c91550dbb2746385a11fa809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118129764"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a>Proprietà IMsRdpClientShell::IsRemoteProgramClientInstalled

Recupera un valore che indica se Connessione Desktop remoto (RDC) supporta la Windows RemoteApp di Server 2008 R2.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a>Valore proprietà

Recupera un valore che indica se Connessione Desktop remoto client (RDC) supporta la funzionalità RemoteApp.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell è definito come d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





