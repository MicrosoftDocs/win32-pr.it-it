---
title: Metodo RemoveUserAssignment della classe Win32_RDMSVirtualDesktop
description: Rimuove l'assegnazione utente dal desktop virtuale.
ms.assetid: 7ebb34b4-94f6-4a00-87a9-44ad28d103cb
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RemoveUserAssignment
- Metodo RemoveUserAssignment Servizi Desktop remoto, classe Win32_RDMSVirtualDesktop
- Classe Win32_RDMSVirtualDesktop Servizi Desktop remoto, metodo RemoveUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.RemoveUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01675c777603f0eab2d22c0136b1ef6cc3522b7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301859"
---
# <a name="removeuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Metodo RemoveUserAssignment della \_ classe RDMSVirtualDesktop Win32

Rimuove l'assegnazione utente dal desktop virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveUserAssignment(
  [in] string VMName
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*VMName* \[ in\]
</dt> <dd>

Nome della macchina virtuale del desktop virtuale.

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

 

 





