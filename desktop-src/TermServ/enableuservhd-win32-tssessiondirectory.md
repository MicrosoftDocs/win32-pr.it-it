---
title: Metodo EnableUserVhd della Win32_TSSessionDirectory classe
description: Abilita un disco rigido virtuale del profilo utente in un server Host sessione Desktop remoto.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- Metodo EnableUserVhd Servizi Desktop remoto
- Metodo EnableUserVhd Servizi Desktop remoto , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Servizi Desktop remoto , metodo EnableUserVhd
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.EnableUserVhd
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19e042b51c7060e4d4c2a8302a87b2d27ee2cf89608a9831cb3497fd0566689a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871741"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a>Metodo EnableUserVhd della classe \_ TSSessionDirectory Win32

Abilita un disco rigido virtuale del profilo utente in un server Host sessione Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UvhdShareUrl* \[ Pollici\]
</dt> <dd>

Percorso della condivisione in cui sono archiviati tutti i dischi rigidi virtuali dei profili utente.

</dd> <dt>

*UvhdRoamingPolicyXml* \[ Pollici\]
</dt> <dd>

Criteri di roaming per il disco rigido virtuale del profilo utente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





