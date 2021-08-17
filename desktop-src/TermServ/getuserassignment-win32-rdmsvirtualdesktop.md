---
title: Metodo GetUserAssignment della classe Win32_RDMSVirtualDesktop
description: Recupera il nome utente e il nome di dominio dell'utente assegnato al desktop virtuale.
ms.assetid: 1887c49d-85df-4fb4-9b40-42fb7763bf95
ms.tgt_platform: multiple
keywords:
- Metodo GetUserAssignment Servizi Desktop remoto
- Metodo GetUserAssignment Servizi Desktop remoto , Win32_RDMSVirtualDesktop classe
- Win32_RDMSVirtualDesktop classe Servizi Desktop remoto metodo , GetUserAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetUserAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff3d63179ec68c38ada5738390979e4844ff2950f91decf82245a6b164dbab2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059559"
---
# <a name="getuserassignment-method-of-the-win32_rdmsvirtualdesktop-class"></a>Metodo GetUserAssignment della classe \_ RDMSVirtualDesktop Win32

Recupera il nome utente e il nome di dominio dell'utente assegnato al desktop virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetUserAssignment(
  [out] string UserName,
  [out] string UserDomain
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UserName* \[ Cambio\]
</dt> <dd>

Riceve il nome utente.

</dd> <dt>

*UserDomain* \[ Cambio\]
</dt> <dd>

Riceve il nome di dominio.

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

 

 





