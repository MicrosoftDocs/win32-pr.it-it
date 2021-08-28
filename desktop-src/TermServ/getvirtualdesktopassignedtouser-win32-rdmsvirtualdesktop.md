---
title: Metodo GetVirtualDesktopAssignedToUser della Win32_RDMSVirtualDesktop classe
description: Recupera il desktop virtuale assegnato all'utente specificato.
ms.assetid: cbc22c45-4492-4651-b164-a6fd717c5ab4
ms.tgt_platform: multiple
keywords:
- Metodo GetVirtualDesktopAssignedToUser Servizi Desktop remoto
- Metodo GetVirtualDesktopAssignedToUser Servizi Desktop remoto , Win32_RDMSVirtualDesktop classe
- Win32_RDMSVirtualDesktop classe Servizi Desktop remoto metodo , GetVirtualDesktopAssignedToUser
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopAssignedToUser
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fce30afea4a95ed462bfb1b456788fa54f045097c16c3d65070cdb343e928237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059549"
---
# <a name="getvirtualdesktopassignedtouser-method-of-the-win32_rdmsvirtualdesktop-class"></a>Metodo GetVirtualDesktopAssignedToUser della classe \_ WIN32 RDMSVirtualDesktop

Recupera il desktop virtuale assegnato all'utente specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetVirtualDesktopAssignedToUser(
  [in]  string CollectionAlias,
  [in]  string UserName,
  [in]  string UserDomain,
  [out] string VMName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CollectionAlias* \[ Pollici\]
</dt> <dd>

Alias della raccolta di desktop virtuali che contiene il desktop virtuale.

</dd> <dt>

*UserName* \[ Pollici\]
</dt> <dd>

Nome utente dell'utente.

</dd> <dt>

*UserDomain* \[ Pollici\]
</dt> <dd>

Nome di dominio dell'utente.

</dd> <dt>

*VMName* \[ Cambio\]
</dt> <dd>

Riceve il nome della macchina virtuale del desktop virtuale.

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

 

 





