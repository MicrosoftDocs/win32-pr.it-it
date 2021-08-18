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
ms.openlocfilehash: 07245e97e091f607d142de57c00109d3671bd81b5f34b9062681229090ff6b50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439401"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a>Metodo SetShareInfo della classe ClusterShare Win32 \_

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

Limite al numero massimo di utenti autorizzati a usare questa risorsa contemporaneamente.

</dd> <dt>

*Descrizione* \[ in, facoltativo\]
</dt> <dd>

Descrive la risorsa condivisa.

</dd> <dt>

*Accesso* \[ in, facoltativo\]
</dt> <dd>

Descrittore di sicurezza per le autorizzazioni a livello di utente. Un descrittore di sicurezza contiene informazioni sulle funzionalità di autorizzazione, proprietario e accesso della risorsa. Per altre informazioni, vedere [**Descrittore di sicurezza Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                    |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Condivisione cluster \_ Win32**](win32-clustershare.md)
</dt> </dl>

 

