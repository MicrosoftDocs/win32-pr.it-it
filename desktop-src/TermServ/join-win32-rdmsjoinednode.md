---
title: Metodo join della classe Win32_RDMSJoinedNode
description: Aggiunge un nodo a Desktop remoto Management Services (RDBMS).
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Metodo join Servizi Desktop remoto
- Metodo join Servizi Desktop remoto, classe Win32_RDMSJoinedNode
- Classe Win32_RDMSJoinedNode Servizi Desktop remoto, metodo Join
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
ms.openlocfilehash: 587e68758971453e8c4e307ccb37ce6cede262f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400372"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a>Metodo join della classe Win32 \_ RDMSJoinedNode

Aggiunge un nodo a Desktop remoto Management Services (RDBMS).

## <a name="syntax"></a>Sintassi


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*NodeFQDN* \[ in\]
</dt> <dd>

Nome di dominio completo del nodo.

</dd> <dt>

*Nodesid* \[ in\]
</dt> <dd>

ID di sicurezza (SID) del nodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDMSJoinedNode Win32**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





