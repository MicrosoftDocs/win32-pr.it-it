---
title: Metodo GetStringProperty della classe Win32_RDSHServer
description: Recupera un valore della proprietà di stringa di un \_ oggetto Win32 RDSHServer.
ms.assetid: 136cd213-86a6-472a-8853-8d05f992309a
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo GetStringProperty
- Metodo GetStringProperty Servizi Desktop remoto, classe Win32_RDSHServer
- Classe Win32_RDSHServer Servizi Desktop remoto, Metodo GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 619a034e0a2f89270d21bf0c4fc297b4248cef59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479115"
---
# <a name="getstringproperty-method-of-the-win32_rdshserver-class"></a>Metodo GetStringProperty della \_ classe RDSHServer Win32

Recupera un valore della proprietà di stringa di un oggetto [**Win32 \_ RDSHServer**](win32-rdshserver.md) .

## <a name="syntax"></a>Sintassi


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
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

 

 





