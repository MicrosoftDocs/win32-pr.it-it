---
title: Metodo CreateUserDiskTemplate della classe Win32_TSSessionDirectory
description: Crea un modello di disco utente.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CreateUserDiskTemplate
- Metodo CreateUserDiskTemplate Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo CreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119203"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a>Metodo CreateUserDiskTemplate della \_ classe TSSessionDirectory Win32

Crea un modello di disco utente.

## <a name="syntax"></a>Sintassi


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UserDisksStorageUrl* \[ in\]
</dt> <dd>

Percorso della condivisione in cui sono archiviati tutti i dischi utente.

</dd> <dt>

*UserDiskMaxSizeInGB* \[ in\]
</dt> <dd>

Dimensione massima in gigabyte per tutti i dischi utente.

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

 

 





