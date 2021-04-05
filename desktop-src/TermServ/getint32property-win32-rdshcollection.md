---
title: Metodo GetInt32Property della classe Win32_RDSHCollection (Microsoft. Diagnostics. appanalysis. h)
description: Recupera un valore di proprietà Integer di un \_ oggetto Win32 RDSHCollection.
ms.assetid: ab68f357-057d-4a36-ae39-f47198768a49
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetInt32Property
- Metodo GetInt32Property Servizi Desktop remoto, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Servizi Desktop remoto, metodo GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5cc29234fe3bb1b92e68e728423931da965391f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740407"
---
# <a name="getint32property-method-of-the-win32_rdshcollection-class"></a>Metodo GetInt32Property della \_ classe RDSHCollection Win32

Recupera un valore di proprietà Integer di un oggetto [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) .

## <a name="syntax"></a>Sintassi


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ di in\]
</dt> <dd>

Chiave che identifica la proprietà da recuperare.

</dd> <dt>

*Valore* \[ di out\]
</dt> <dd>

Riceve il valore della proprietà recuperata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                                      |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                                 |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ RDBMS<br/>                                                                                   |
| Intestazione<br/>                   | <dl> <dt>Microsoft. Diagnostics. appanalysis. h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDSHCollection Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





