---
title: Metodo SetInt32Property della Win32_RDSHCollection classe
description: Aggiorna un valore della proprietà Integer di un oggetto \_ RDSHCollection Win32.
ms.assetid: 2a9a5d83-d147-43b3-b57c-6c744da0923d
ms.tgt_platform: multiple
keywords:
- Metodo SetInt32Property Servizi Desktop remoto
- Metodo SetInt32Property Servizi Desktop remoto , Win32_RDSHCollection classe
- Win32_RDSHCollection classe Servizi Desktop remoto, metodo SetInt32Property
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
ms.openlocfilehash: d19af81a807d6a2eb27693b88428df925644675093d3fbb80cb809a6011fb22b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127456"
---
# <a name="setint32property-method-of-the-win32_rdshcollection-class"></a>Metodo SetInt32Property della classe RDSHCollection Win32 \_

Aggiorna un valore della proprietà Integer di [**un oggetto \_ RDSHCollection Win32.**](win32-rdshcollection.md)

## <a name="syntax"></a>Sintassi


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Chiave* \[ Pollici\]
</dt> <dd>

Chiave che identifica la proprietà da aggiornare.

</dd> <dt>

*Valore* \[ Pollici\]
</dt> <dd>

Nuovo valore della proprietà.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Root \\ CIMv2 \\ rdms<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDSHCollection**](win32-rdshcollection.md)
</dt> </dl>

 

 





