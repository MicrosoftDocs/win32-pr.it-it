---
title: Metodo GetStringProperty della classe Win32_RDSHCollection
description: Recupera un valore della proprietà di stringa di un \_ oggetto Win32 RDSHCollection.
ms.assetid: 8e97cd91-0e45-4d87-acfb-ee7d70376ce0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del Metodo GetStringProperty
- Metodo GetStringProperty Servizi Desktop remoto, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Servizi Desktop remoto, Metodo GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1895f05317850374a4f4b24d407a4c4ace9c5db7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963909"
---
# <a name="getstringproperty-method-of-the-win32_rdshcollection-class"></a>Metodo GetStringProperty della \_ classe RDSHCollection Win32

Recupera un valore della proprietà di stringa di un oggetto [**Win32 \_ RDSHCollection**](win32-rdshcollection.md) .

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

[**\_RDSHCollection Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





