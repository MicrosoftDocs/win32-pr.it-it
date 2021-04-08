---
title: Metodo KeyValueCompareAndSet della classe Win32_RDSHCollection
description: Confronta la chiave specificata nella raccolta con un comparand; Se corrispondono, la chiave viene impostata su un nuovo valore. Se la chiave non esiste, il metodo inserirà la chiave nella raccolta.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo KeyValueCompareAndSet
- Metodo KeyValueCompareAndSet Servizi Desktop remoto, classe Win32_RDSHCollection
- Classe Win32_RDSHCollection Servizi Desktop remoto, metodo KeyValueCompareAndSet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b90d703b40cf76f59cc3caf5d8f197f387cfe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873622"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a>Metodo KeyValueCompareAndSet della \_ classe RDSHCollection Win32

Confronta la chiave specificata nella raccolta con un comparand; Se corrispondono, la chiave viene impostata su un nuovo valore. Se la chiave non esiste, il metodo inserirà la chiave nella raccolta.

## <a name="syntax"></a>Sintassi


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ di in\]
</dt> <dd>

Chiave da confrontare.

</dd> <dt>

*NewValue* \[ in\]
</dt> <dd>

Nuovo valore.

</dd> <dt>

*Comparand* \[ in\]
</dt> <dd>

Stringa da confrontare con la chiave.

</dd> <dt>

*InitialValue* \[ out\]
</dt> <dd>

In caso di esito positivo o negativo, contiene il valore iniziale della chiave.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che questo metodo può recuperare il valore della chiave e, di conseguenza, incapsula la funzionalità di [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).

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

[**\_RDSHCollection Win32**](win32-rdshcollection.md)
</dt> </dl>

 

 





