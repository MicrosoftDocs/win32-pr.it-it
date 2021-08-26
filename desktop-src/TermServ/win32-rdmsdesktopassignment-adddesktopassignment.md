---
title: Metodo AddDesktopAssignment della Win32_RDMSDesktopAssignment classe
description: Aggiungere un'assegnazione desktop.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- Metodo AddDesktopAssignment Servizi Desktop remoto
- Metodo AddDesktopAssignment Servizi Desktop remoto , Win32_RDMSDesktopAssignment classe
- Win32_RDMSDesktopAssignment classe Servizi Desktop remoto , metodo AddDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.AddDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0d8145318cfd749772d2dcf417b71c6a1862ee31ec363957554e06b3aa6257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868221"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Metodo AddDesktopAssignment della classe \_ WIN32 RDMSDesktopAssignment

Aggiungere un'assegnazione desktop

## <a name="syntax"></a>Sintassi


```mof
uint32 AddDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*CollectionAlias* \[ Pollici\]
</dt> <dd>

Alias della raccolta.

</dd> <dt>

*DesktopName* \[ Pollici\]
</dt> <dd>

Nome del desktop.

</dd> <dt>

*UserDomain* \[ Pollici\]
</dt> <dd>

Nome di dominio dell'account utente.

</dd> <dt>

*UserName* \[ Pollici\]
</dt> <dd>

Nome dell'account utente.

</dd> </dl>

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

[**Win32 \_ RDMSDesktopAssignment**](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





