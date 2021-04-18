---
title: Metodo FileAssociations della classe Win32_TSApplicationFileExtensions
description: Analizza il registro di sistema per ottenere le associazioni di file correnti per un'applicazione.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- Metodo FileAssociations Servizi Desktop remoto
- Servizi Desktop remoto del metodo FileAssociations, classe Win32_TSApplicationFileExtensions
- Classe Win32_TSApplicationFileExtensions Servizi Desktop remoto, metodo FileAssociations
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
ms.openlocfilehash: 23ee60033344c0c448d82680bdcacfc24cb4f214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302476"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a>Metodo FileAssociations della \_ classe TSApplicationFileExtensions di Win32

Analizza il registro di sistema per ottenere le associazioni di file correnti per un'applicazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Percorso app* \[ in\]
</dt> <dd>

Specifica il percorso dell'applicazione.

</dd> <dt>

*FileAssociation* \[ out\]
</dt> <dd>

Al termine dell'operazione sono contenute le associazioni di file per l'applicazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TsAllow. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSApplicationFileExtensions Win32**](win32-tsapplicationfileextensions.md)
</dt> <dt>

[**\_RDFileAssociation Win32**](win32-rdfileassociation.md)
</dt> </dl>

 

 





