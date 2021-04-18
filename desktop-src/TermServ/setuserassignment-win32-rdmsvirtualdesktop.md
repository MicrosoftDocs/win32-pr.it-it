---
title: Metodo SetUserAssignment della classe Win32_RDMSVirtualDesktop
description: Assegna un desktop virtuale a un utente.
ms.assetid: 6a96ccb7-5d3d-4164-a0a3-286a700b414c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetUserAssignment
- Metodo SetUserAssignment Servizi Desktop remoto, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Servizi Desktop remoto, metodo SetUserAssignment
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
ms.openlocfilehash: 5f02e1cc935e344edd6a9c52016052e082e08d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302446"
---
# <a name="setuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Metodo SetUserAssignment della \_ classe RDMSVirtualDesktop Win32

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

*Nome utente* \[ in\]
</dt> <dd>

Nome utente dell'utente.

</dd> <dt>

*UserDomain* \[ in\]
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
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_RDMSVirtualDesktop Win32**](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





