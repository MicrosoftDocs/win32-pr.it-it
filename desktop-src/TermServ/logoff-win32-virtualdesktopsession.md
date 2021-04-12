---
title: Metodo di disconnessione della classe Win32_VirtualDesktopSession (Sensevts. h)
description: Disconnette l'utente dalla sessione desktop virtuale.
ms.assetid: a9c90ace-324c-4eec-86e1-30ce35307e52
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto metodo di disconnessione
- Servizi Desktop remoto metodo di disconnessione, classe Win32_VirtualDesktopSession
- Classe Win32_VirtualDesktopSession Servizi Desktop remoto, metodo di disconnessione
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.Logoff
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4582744f0d8ba9300bd620a45190ec1de4819ee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400780"
---
# <a name="logoff-method-of-the-win32_virtualdesktopsession-class"></a>Metodo di disconnessione della \_ classe Win32 VirtualDesktopSession

Disconnette l'utente dalla sessione desktop virtuale.

## <a name="syntax"></a>Sintassi


```mof
uint32 Logoff();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ RDBMS<br/>                                                                |
| Intestazione<br/>                   | <dl> <dt>Sensevts. h</dt> </dl>       |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VirtualDesktopSession Win32**](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





