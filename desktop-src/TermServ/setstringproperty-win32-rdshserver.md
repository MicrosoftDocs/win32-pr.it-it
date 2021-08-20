---
title: Metodo SetStringProperty della Win32_RDSHServer classe (Certenroll.h)
description: Aggiorna il valore di una proprietà stringa di un oggetto \_ RDSHServer Win32.
ms.assetid: 9a338872-27fc-4e37-afd6-20a42c7859e5
ms.tgt_platform: multiple
keywords:
- Metodo SetStringProperty Servizi Desktop remoto
- Metodo SetStringProperty Servizi Desktop remoto , Win32_RDSHServer classe
- Win32_RDSHServer classe Servizi Desktop remoto, metodo SetStringProperty
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
ms.openlocfilehash: a2715271bcb73efd15acbef2097a29a978774e575a4fb115a9ef9e727e3efa91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349392"
---
# <a name="setstringproperty-method-of-the-win32_rdshserver-class"></a>Metodo SetStringProperty della classe RDSHServer Win32 \_

Aggiorna il valore di una proprietà stringa di un [**oggetto \_ RDSHServer Win32.**](win32-rdshserver.md)

## <a name="syntax"></a>Sintassi


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
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

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Rdms \\ CIMv2 \\ radice<br/>                                                                |
| Intestazione<br/>                   | <dl> <dt>Certenroll.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 





