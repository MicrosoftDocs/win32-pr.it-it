---
title: Metodo Unjoin della classe Win32_RDMSJoinedNode
description: Rimuove un nodo da Desktop remoto Management Services (RDMS).
ms.assetid: 37c462f4-a19d-4b85-8fac-2735deb7c04f
ms.tgt_platform: multiple
keywords:
- Metodo unjoin Servizi Desktop remoto
- Il metodo unjoin Servizi Desktop remoto , Win32_RDMSJoinedNode classe
- Win32_RDMSJoinedNode classe Servizi Desktop remoto , metodo Unjoin
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Unjoin
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d2fae16ecb31326ae16bc08efd1fbc56ae2585140d63ce360783226101d4a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424101"
---
# <a name="unjoin-method-of-the-win32_rdmsjoinednode-class"></a>Metodo Unjoin della classe \_ RDMSJoinedNode Win32

Rimuove un nodo da Desktop remoto Management Services (RDMS).

## <a name="syntax"></a>Sintassi


```mof
uint32 Unjoin();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Root \\ CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSJoinedNode**](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





