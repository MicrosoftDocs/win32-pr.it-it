---
title: Metodo TestAndSetState della classe Win32_RDSHServer
description: Confronta lo stato corrente con il comparand specificato. Se le due corrispondenze, lo stato viene impostato su un nuovo valore. Indipendentemente dalla corrispondenza, viene restituito anche lo stato corrente.
ms.assetid: f1bb0076-251b-4c0d-92f9-1c460e1b26bb
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo TestAndSetState
- Metodo TestAndSetState Servizi Desktop remoto, classe Win32_RDSHServer
- Classe Win32_RDSHServer Servizi Desktop remoto, metodo TestAndSetState
topic_type:
- apiref
api_name:
- Win32_RDSHServer.TestAndSetState
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4c9b616c2a288f5f39b240d71b2611e25d45f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119974"
---
# <a name="testandsetstate-method-of-the-win32_rdshserver-class"></a>Metodo TestAndSetState della \_ classe RDSHServer Win32

Confronta lo stato corrente con il comparand specificato. Se le due corrispondenze, lo stato viene impostato su un nuovo valore. Indipendentemente dalla corrispondenza, viene restituito anche lo stato corrente.

## <a name="syntax"></a>Sintassi


```mof
uint32 TestAndSetState(
  [in]  uint32 Comparand,
  [in]  uint32 NewState,
  [out] uint32 InitState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Comparand* \[ in\]
</dt> <dd>

Valore da confrontare con lo stato corrente. Se i due valori corrispondono, lo stato viene impostato su *NewState*.

</dd> <dt>

*NewState* \[ in\]
</dt> <dd>

Nuovo valore dello stato.

</dd> <dt>

*InitState* \[ out\]
</dt> <dd>

In caso di esito positivo o negativo, restituisce lo stato corrente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDSHServer Win32**](win32-rdshserver.md)
</dt> </dl>

 

 





