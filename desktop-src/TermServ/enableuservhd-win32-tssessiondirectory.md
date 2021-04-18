---
title: Metodo EnableUserVhd della classe Win32_TSSessionDirectory
description: Abilita un VHD del profilo utente in un server RDSH.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo EnableUserVhd
- Metodo EnableUserVhd Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo EnableUserVhd
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
ms.openlocfilehash: 464e105d2f8f0c80126e6b9ca5e5a383b2d17628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302746"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a>Metodo EnableUserVhd della \_ classe TSSessionDirectory Win32

Abilita un VHD del profilo utente in un server RDSH.

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UvhdShareUrl* \[ in\]
</dt> <dd>

Percorso della condivisione in cui vengono archiviati tutti i dischi rigidi virtuali del profilo utente.

</dd> <dt>

*UvhdRoamingPolicyXml* \[ in\]
</dt> <dd>

Criteri di roaming per il VHD del profilo utente.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





