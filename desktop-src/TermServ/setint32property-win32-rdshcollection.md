---
title: Metodo SetInt32Property della classe Win32_RDSHCollection
description: Aggiorna un valore della proprietà Integer di un \_ oggetto Win32 RDSHCollection.
ms.assetid: 2a9a5d83-d147-43b3-b57c-6c744da0923d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetInt32Property
- Metodo SetInt32Property Servizi Desktop remoto, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Servizi Desktop remoto, metodo SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 136bb8ccf34004f747829fb43ee8080ccd1d3132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302447"
---
# <a name="setint32property-method-of-the-win32_rdshcollection-class"></a>Metodo SetInt32Property della \_ classe RDSHCollection Win32

Aggiorna un valore della proprietà Integer di un oggetto [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) .

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

[**\_RDSHCollection Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





