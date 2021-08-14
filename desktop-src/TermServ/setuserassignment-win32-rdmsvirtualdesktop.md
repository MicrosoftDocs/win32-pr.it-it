---
title: Metodo SetUserAssignment della classe Win32_RDMSVirtualDesktop
description: Assegna un desktop virtuale a un utente.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- Metodo SetUserAssignment Servizi Desktop remoto
- Metodo SetUserAssignment Servizi Desktop remoto , Win32_RDMSVirtualDesktop classe
- Win32_RDMSVirtualDesktop classe Servizi Desktop remoto metodo SetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.SetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f38f87209ba8c8ebd82637f72cea2e798844e6081cd000f2161ee21681422e40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118349412"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Metodo SetUserAssignment della classe \_ RDMSVirtualDesktop Win32

Assegna un desktop virtuale a un utente.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetUserAssignment(
  [in] string UserName,
  [in] string UserDomain
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UserName* \[ Pollici\]
</dt> <dd>

Nome utente dell'utente.

</dd> <dt>

*UserDomain* \[ Pollici\]
</dt> <dd>

Nome di dominio dell'utente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Rdms \\ CIMv2 \\ radice<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ RDMSVirtualDesktop**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





