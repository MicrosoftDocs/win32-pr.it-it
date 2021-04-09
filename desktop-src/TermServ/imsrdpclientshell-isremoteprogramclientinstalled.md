---
title: Proprietà IsRemoteProgramClientInstalled di IMsRdpClientShell
description: Recupera un valore che indica se il client di Connessione Desktop remoto (RDC) supporta la funzionalità RemoteApp di Windows Server 2008 R2.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà IsRemoteProgramClientInstalled
- Servizi Desktop remoto proprietà IsRemoteProgramClientInstalled, interfaccia IMsRdpClientShell
- Interfaccia IMsRdpClientShell Servizi Desktop remoto, proprietà IsRemoteProgramClientInstalled
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
ms.openlocfilehash: 787d45f10e109a89429be5032fda245aa3609567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119375"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a>Proprietà IMsRdpClientShell:: IsRemoteProgramClientInstalled

Recupera un valore che indica se il client di Connessione Desktop remoto (RDC) supporta la funzionalità RemoteApp di Windows Server 2008 R2.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a>Valore proprietà

Recupera un valore che indica se il client di Connessione Desktop remoto (RDC) supporta la funzionalità RemoteApp.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpClientShell è definito come d012ae6d-c19a-4bfe-B367-201f8911f134<br/>   |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IMsRdpClientShell**](imsrdpclientshell.md)
</dt> </dl>

 

 





