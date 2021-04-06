---
title: Metodo AddDesktopAssignment della classe Win32_RDMSDesktopAssignment
description: Aggiungere un'assegnazione desktop.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo AddDesktopAssignment
- Metodo AddDesktopAssignment Servizi Desktop remoto, classe Win32_RDMSDesktopAssignment
- Classe Win32_RDMSDesktopAssignment Servizi Desktop remoto, metodo AddDesktopAssignment
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
ms.openlocfilehash: 571273e76b0bb45b748f1587e5a831fcf1e36b0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873626"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Metodo AddDesktopAssignment della \_ classe RDMSDesktopAssignment Win32

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

*CollectionAlias* \[ in\]
</dt> <dd>

Alias della raccolta.

</dd> <dt>

*Desktopname* \[ in\]
</dt> <dd>

Nome del desktop.

</dd> <dt>

*UserDomain* \[ in\]
</dt> <dd>

Nome di dominio dell'account utente.

</dd> <dt>

*Nome utente* \[ in\]
</dt> <dd>

Nome dell'account utente.

</dd> </dl>

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

[**\_RDMSDesktopAssignment Win32**](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





