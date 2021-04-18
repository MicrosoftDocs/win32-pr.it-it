---
description: Imposta i parametri della risorsa condivisa.
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Metodo SetShareInfo della classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bda6fe36d1168045ea9f8d331ff334920ed1dd19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305278"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a>Metodo SetShareInfo della \_ classe ClusterShare Win32

Imposta i parametri della risorsa condivisa.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MaximumAllowed* \[ in, facoltativo\]
</dt> <dd>

Limite per il numero massimo di utenti che possono usare questa risorsa contemporaneamente.

</dd> <dt>

*Descrizione* \[ di in, facoltativo\]
</dt> <dd>

Descrive la risorsa condivisa.

</dd> <dt>

*Accesso* \[ a in, facoltativo\]
</dt> <dd>

Descrittore di sicurezza per le autorizzazioni a livello di utente. Un descrittore di sicurezza contiene informazioni sulle funzionalità di autorizzazione, proprietario e accesso della risorsa. Per ulteriori informazioni, vedere [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                    |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ClusterShare Win32**](win32-clustershare.md)
</dt> </dl>

 

