---
title: Metodo RemoveDesktopAssignment della classe Win32_RDMSDesktopAssignment
description: Rimuove un'assegnazione desktop.
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveDesktopAssignment
- Metodo RemoveDesktopAssignment Servizi Desktop remoto, classe Win32_RDMSDesktopAssignment
- Classe Win32_RDMSDesktopAssignment Servizi Desktop remoto, metodo RemoveDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302569"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Metodo RemoveDesktopAssignment della \_ classe RDMSDesktopAssignment Win32

Rimuove un'assegnazione desktop

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveDesktopAssignment(
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

 

 





