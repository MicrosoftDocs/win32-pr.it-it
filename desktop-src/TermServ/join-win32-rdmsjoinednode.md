---
title: Metodo Join della classe Win32_RDMSJoinedNode join
description: Aggiunge un nodo a Desktop remoto Management Services (RDMS).
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Metodo join Servizi Desktop remoto
- Metodo Join Servizi Desktop remoto , Win32_RDMSJoinedNode classe
- Win32_RDMSJoinedNode classe Servizi Desktop remoto , metodo Join
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 204d83988f9a57d9fe0edf8daa6dc580676fc7395f98edcbece49674c0041aef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118605424"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a>Metodo Join della classe \_ RDMSJoinedNode Win32

Aggiunge un nodo a Desktop remoto Management Services (RDMS).

## <a name="syntax"></a>Sintassi


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NodeFQDN* \[ Pollici\]
</dt> <dd>

Nome di dominio completo del nodo.

</dd> <dt>

*NodeSID* \[ Pollici\]
</dt> <dd>

Identificatore di sicurezza (SID) del nodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Rdms \\ CIMv2 \\ radice<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSJoinedNode**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





