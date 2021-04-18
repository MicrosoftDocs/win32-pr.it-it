---
title: Metodo Unjoin della classe Win32_RDMSJoinedNode
description: Rimuove un nodo da Desktop remoto Management Services (RDBMS).
ms.assetid: 37c462f4-a19d-4b85-8fac-2735deb7c04f
ms.tgt_platform: multiple
keywords:
- Metodo Unjoin Servizi Desktop remoto
- Unjoin Method Servizi Desktop remoto, classe Win32_RDMSJoinedNode
- Classe Win32_RDMSJoinedNode Servizi Desktop remoto, metodo Unjoin
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
ms.openlocfilehash: 234f7cc3ad8a797fff51661528f4545ed9fea3a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301745"
---
# <a name="unjoin-method-of-the-win32_rdmsjoinednode-class"></a>Metodo Unjoin della classe Win32 \_ RDMSJoinedNode

Rimuove un nodo da Desktop remoto Management Services (RDBMS).

## <a name="syntax"></a>Sintassi


```mof
uint32 Unjoin();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

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

 

 





