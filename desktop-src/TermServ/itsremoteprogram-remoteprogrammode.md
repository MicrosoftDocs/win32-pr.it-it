---
title: ItsRemoteProgram RemoteProgramMode - proprietà
description: La Windows RemoteApp di Server 2008 R2.
ms.assetid: 9ebdf966-db9c-4a14-8469-f8b153c6ea78
ms.tgt_platform: multiple
keywords:
- Proprietà RemoteProgramMode Servizi Desktop remoto
- Proprietà RemoteProgramMode Servizi Desktop remoto, interfaccia ITSRemoteProgram
- ItsRemoteProgram interface Servizi Desktop remoto proprietà RemoteProgramMode
- Proprietà RemoteProgramMode Servizi Desktop remoto, interfaccia ITSRemoteProgram2
- ItsRemoteProgram2 interface Servizi Desktop remoto , RemoteProgramMode property
- Proprietà RemoteProgramMode Servizi Desktop remoto, interfaccia ITSRemoteProgram3
- ItsRemoteProgram3 interface Servizi Desktop remoto , RemoteProgramMode property
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
ms.openlocfilehash: c36f450e6cbfec3922a56a42bc2f1f61466774eeff46c0987b6fad4ca9dc9731
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124821"
---
# <a name="itsremoteprogramremoteprogrammode-property"></a>ItsRemoteProgram::RemoteProgramMode - proprietà

La Windows RemoteApp di Server 2008 R2.

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

Modalità RemoteApp. Se impostato su **VARIANT \_ TRUE,** la modalità RemoteApp è abilitata e la sessione remota ospiterà i programmi RemoteApp. Se impostato su **VARIANT \_ FALSE** (impostazione predefinita), la modalità RemoteApp non è abilitata. La sessione remota ospiterà un desktop remoto.

## <a name="error-codes"></a>Codici di errore

Restituisce **S \_ OK in** caso di esito positivo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Libreria dei tipi<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID ITSRemoteProgram è definito \_ come FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





