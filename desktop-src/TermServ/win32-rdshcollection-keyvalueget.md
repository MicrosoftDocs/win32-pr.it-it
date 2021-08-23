---
title: Metodo KeyValueGet della classe Win32_RDSHCollection
description: Recupera il valore associato alla chiave specificata nella raccolta.
ms.assetid: 69d309a4-b32e-4dbc-bd28-be79d395ac26
ms.tgt_platform: multiple
keywords:
- Metodo KeyValueGet Servizi Desktop remoto
- Metodo KeyValueGet Servizi Desktop remoto , Win32_RDSHCollection classe
- Win32_RDSHCollection classe Servizi Desktop remoto , metodo KeyValueGet
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueGet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 943db8db044758e7f78e7d79b4ae5280c6ce51281b5858237a24e5f83add33a4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119422681"
---
# <a name="keyvalueget-method-of-the-win32_rdshcollection-class"></a>Metodo KeyValueGet della classe RDSHCollection Win32 \_

Recupera il valore associato alla chiave specificata nella raccolta.

## <a name="syntax"></a>Sintassi


```mof
uint32 KeyValueGet(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ Pollici\]
</dt> <dd>

Chiave che identifica il valore da recuperare.

</dd> <dt>

*Valore* \[ Cambio\]
</dt> <dd>

In caso di esito positivo, restituisce il valore associato alla chiave specificata.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2016<br/>                                                              |
| Spazio dei nomi<br/>                | Rdms \\ cimv2 \\ radice<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





