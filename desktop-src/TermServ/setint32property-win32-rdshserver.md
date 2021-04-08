---
title: Metodo SetInt32Property della classe Win32_RDSHServer
description: Aggiorna un valore della proprietà Integer di un \_ oggetto Win32 RDSHServer.
ms.assetid: fa8df023-120d-4174-adc1-868f08fdce56
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetInt32Property
- Metodo SetInt32Property Servizi Desktop remoto, classe Win32_RDSHServer
- Classe Win32_RDSHServer Servizi Desktop remoto, metodo SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c22c8da9c046e0a42a6ec41f6ad5b3073c8d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741298"
---
# <a name="setint32property-method-of-the-win32_rdshserver-class"></a>Metodo SetInt32Property della \_ classe RDSHServer Win32

Aggiorna un valore della proprietà Integer di un oggetto [**Win32 \_ RDSHServer**](win32-rdshserver.md) .

## <a name="syntax"></a>Sintassi


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ di in\]
</dt> <dd>

Chiave che identifica la proprietà da aggiornare.

</dd> <dt>

*Valore* \[ di in\]
</dt> <dd>

Nuovo valore della proprietà.

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

[**\_RDSHServer Win32**](win32-rdshserver.md)
</dt> </dl>

 

 





