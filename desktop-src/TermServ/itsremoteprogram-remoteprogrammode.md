---
title: Proprietà RemoteProgramMode di ITSRemoteProgram
description: Modalità RemoteApp di Windows Server 2008 R2.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà RemoteProgramMode
- Servizi Desktop remoto proprietà RemoteProgramMode, interfaccia ITSRemoteProgram
- Interfaccia ITSRemoteProgram Servizi Desktop remoto, proprietà RemoteProgramMode
- Servizi Desktop remoto proprietà RemoteProgramMode, interfaccia ITSRemoteProgram2
- Interfaccia ITSRemoteProgram2 Servizi Desktop remoto, proprietà RemoteProgramMode
- Servizi Desktop remoto proprietà RemoteProgramMode, interfaccia ITSRemoteProgram3
- Interfaccia ITSRemoteProgram3 Servizi Desktop remoto, proprietà RemoteProgramMode
topic_type:
- apiref
api_name:
- ITSRemoteProgram.RemoteProgramMode
- ITSRemoteProgram.get_RemoteProgramMode
- ITSRemoteProgram.put_RemoteProgramMode
- ITSRemoteProgram2.RemoteProgramMode
- ITSRemoteProgram2.get_RemoteProgramMode
- ITSRemoteProgram2.put_RemoteProgramMode
- ITSRemoteProgram3.RemoteProgramMode
- ITSRemoteProgram3.get_RemoteProgramMode
- ITSRemoteProgram3.put_RemoteProgramMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8582824e2f6349e37b125ffd974847b602ad6fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301867"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a>Proprietà ITSRemoteProgram:: RemoteProgramMode

Modalità RemoteApp di Windows Server 2008 R2.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_RemoteProgramMode(
  [in]  VARIANT_BOOL vboolRemoteProgramMode
);

HRESULT get_RemoteProgramMode(
  [out] VARIANT_BOOL *pvboolRemoteProgramMode
);
```



## <a name="property-value"></a>Valore proprietà

Modalità RemoteApp. Se impostato su **Variant \_ true**, la modalità RemoteApp è abilitata e la sessione remota ospiterà i programmi RemoteApp. Se è impostato su **Variant \_ false** (impostazione predefinita), la modalità RemoteApp non è abilitata. La sessione remota ospiterà un desktop remoto.

## <a name="error-codes"></a>Codici di errore

Restituisce **\_ OK** se ha esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ ITSRemoteProgram è definito come FDD029F9-467a-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





