---
title: Metodo GetJoinedNodeCount della classe Win32_RDMSJoinedNode
description: Ottenere il numero di server in cui sono installati i ruoli specificati.
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetJoinedNodeCount
- Metodo GetJoinedNodeCount Servizi Desktop remoto, classe Win32_RDMSJoinedNode
- Classe Win32_RDMSJoinedNode Servizi Desktop remoto, metodo GetJoinedNodeCount
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301448"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a>Metodo GetJoinedNodeCount della \_ classe RDMSJoinedNode Win32

Ottenere il numero di server in cui sono installati i ruoli specificati.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RoleType* \[ in\]
</dt> <dd>

Oggetto bit che specifica i tipi di ruolo.

<dt>

0
</dt> <dd>

Tutti

</dd> <dt>

1
</dt> <dd>

Broker di Connessione Desktop remoto (RDCB)

</dd> <dt>

2
</dt> <dd>

Host sessione Desktop remoto (RDSH)

</dd> <dt>

4
</dt> <dd>

Host di virtualizzazione Desktop remoto (RDVH)

</dd> </dl> </dd> <dt>

*Numero* \[ di out\]
</dt> <dd>

Se l'operazione riesce, restituisce il numero di server con i ruoli specificati installati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDMSJoinedNode Win32**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





