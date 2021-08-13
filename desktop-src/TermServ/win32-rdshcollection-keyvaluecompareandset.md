---
title: Metodo KeyValueCompareAndSet della Win32_RDSHCollection classe
description: Confronta la chiave specificata nella raccolta con un confronto; Se corrispondono, la chiave viene impostata su un nuovo valore. Se la chiave non esiste, il metodo inserirà la chiave nella raccolta .
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- Metodo KeyValueCompareAndSet Servizi Desktop remoto
- Metodo KeyValueCompareAndSet Servizi Desktop remoto , Win32_RDSHCollection classe
- Win32_RDSHCollection classe Servizi Desktop remoto, metodo KeyValueCompareAndSet
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
ms.openlocfilehash: 52e1aaaf90313c8c1434a65c4ffd1045933ad503245f0dacbf78c2b7e1ca054a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422711"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a>Metodo KeyValueCompareAndSet della classe RDSHCollection Win32 \_

Confronta la chiave specificata nella raccolta con un confronto; Se corrispondono, la chiave viene impostata su un nuovo valore. Se la chiave non esiste, il metodo inserirà la chiave nella raccolta .

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

*Chiave* \[ Pollici\]
</dt> <dd>

Chiave da confrontare.

</dd> <dt>

*NewValue* \[ Pollici\]
</dt> <dd>

Nuovo valore.

</dd> <dt>

*Comparand* \[ Pollici\]
</dt> <dd>

Stringa con cui confrontare la chiave.

</dd> <dt>

*InitialValue* \[ Cambio\]
</dt> <dd>

In caso di esito positivo o negativo, contiene il valore iniziale della chiave.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che questo metodo può recuperare il valore della chiave e di conseguenza incapsula la funzionalità di [**KeyValueGet.**](win32-rdshcollection-keyvalueget.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ cimv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





