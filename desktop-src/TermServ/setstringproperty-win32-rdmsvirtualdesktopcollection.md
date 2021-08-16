---
title: Metodo SetStringProperty della Win32_RDMSVirtualDesktopCollection classe (Certenroll.h)
description: Aggiorna una proprietà stringa di una raccolta di desktop virtuali.
ms.assetid: d76d5f77-3b51-41b9-8ec5-a737ddc0a9d3
ms.tgt_platform: multiple
keywords:
- Metodo SetStringProperty Servizi Desktop remoto
- Metodo SetStringProperty Servizi Desktop remoto , Win32_RDMSVirtualDesktopCollection classe
- Win32_RDMSVirtualDesktopCollection classe Servizi Desktop remoto, metodo SetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8fa0f8302ca2b4c843e552bed8de9145d74c6492626694bb9da0b127d0a07d2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349355"
---
# <a name="setstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Metodo SetStringProperty della classe \_ RDMSVirtualDesktopCollection Win32

Aggiorna una proprietà stringa di una raccolta di desktop virtuali.

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

[**Win32 \_ RDMSVirtualDesktopCollection**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





