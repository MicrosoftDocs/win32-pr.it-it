---
title: Metodo GetInt32Property della classe Win32_RDSHServer (Microsoft. Diagnostics. appanalysis. h)
description: Recupera un valore di proprietà Integer di un \_ oggetto Win32 RDSHServer.
ms.assetid: 4601e9cb-927b-4af8-a12b-09a8ca44c2f7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo GetInt32Property
- Metodo GetInt32Property Servizi Desktop remoto, classe Win32_RDSHServer
- Classe Win32_RDSHServer Servizi Desktop remoto, metodo GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a2427cfa19a84a8b8988cceacf3e0b836a031f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964431"
---
# <a name="getint32property-method-of-the-win32_rdshserver-class"></a>Metodo GetInt32Property della \_ classe RDSHServer Win32

Recupera un valore di proprietà Integer di un oggetto [**Win32 \_ RDSHServer**](win32-rdshserver.md) .

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

[**\_RDSHServer Win32**](win32-rdshserver.md)
</dt> </dl>

 

 





