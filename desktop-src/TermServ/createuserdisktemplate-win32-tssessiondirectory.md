---
title: Metodo CreateUserDiskTemplate della Win32_TSSessionDirectory personalizzata
description: Crea un modello di disco utente.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- Metodo CreateUserDiskTemplate Servizi Desktop remoto
- Metodo CreateUserDiskTemplate Servizi Desktop remoto , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Servizi Desktop remoto, metodo CreateUserDiskTemplate
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
ms.openlocfilehash: cdc16d293f901efb6fc684d03ec7b47aa7496120c462a32414c747d15c02810a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010231"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a>Metodo CreateUserDiskTemplate della classe \_ TSSessionDirectory Win32

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

*UserDisksStorageUrl* \[ Pollici\]
</dt> <dd>

Percorso della condivisione in cui sono archiviati tutti i dischi utente.

</dd> <dt>

*UserDiskMaxSizeInGB* \[ Pollici\]
</dt> <dd>

Dimensione massima in gigabyte per tutti i dischi utente.

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

 

 





