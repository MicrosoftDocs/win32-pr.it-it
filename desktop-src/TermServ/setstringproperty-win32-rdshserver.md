---
title: Metodo SetStringProperty della classe Win32_RDSHServer (CertEnroll. h)
description: Aggiorna il valore di una proprietà di stringa di un \_ oggetto Win32 RDSHServer.
ms.assetid: 9a338872-27fc-4e37-afd6-20a42c7859e5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo SetStringProperty
- Metodo SetStringProperty Servizi Desktop remoto, classe Win32_RDSHServer
- Classe Win32_RDSHServer Servizi Desktop remoto, Metodo SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d30812c0df943175f96c8ae43a4fe094725c74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120383"
---
# <a name="setstringproperty-method-of-the-win32_rdshserver-class"></a>Metodo SetStringProperty della \_ classe RDSHServer Win32

Aggiorna il valore di una proprietà di stringa di un oggetto [**Win32 \_ RDSHServer**](win32-rdshserver.md) .

## <a name="syntax"></a>Sintassi


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
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
| Intestazione<br/>                   | <dl> <dt>CertEnroll. h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDSHServer Win32**](win32-rdshserver.md)
</dt> </dl>

 

 





