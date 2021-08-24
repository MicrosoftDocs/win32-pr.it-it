---
title: Metodo FileAssociations della classe Win32_TSApplicationFileExtensions
description: Analizza il Registro di sistema per ottenere le associazioni di file correnti per un'applicazione.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- Metodo FileAssociations Servizi Desktop remoto
- Metodo FileAssociations Servizi Desktop remoto , Win32_TSApplicationFileExtensions classe
- Win32_TSApplicationFileExtensions classe Servizi Desktop remoto , metodo FileAssociations
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a45548d055d6adc90ac55e26b646abab80470297847d5daa898e63b29769dc4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737511"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a>Metodo FileAssociations della classe \_ Win32 TSApplicationFileExtensions

Analizza il Registro di sistema per ottenere le associazioni di file correnti per un'applicazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AppPath* \[ Pollici\]
</dt> <dd>

Specifica il percorso dell'applicazione.

</dd> <dt>

*FileAssociations* \[ Cambio\]
</dt> <dd>

Al termine, contiene le associazioni di file per questa applicazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSApplicationFileExtensions**](win32-tsapplicationfileextensions.md)
</dt> <dt>

[**Win32 \_ RDFileAssociation**](win32-rdfileassociation.md)
</dt> </dl>

 

 





