---
title: Metodo FileExtensions della classe Win32_TSApplicationFileExtensions
description: Fornisce un elenco delle estensioni dei nomi di file gestite da un'applicazione.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- Metodo FileExtensions Servizi Desktop remoto
- Servizi Desktop remoto del metodo FileExtensions, classe Win32_TSApplicationFileExtensions
- Classe Win32_TSApplicationFileExtensions Servizi Desktop remoto, metodo FileExtensions
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa0bff92cdc274c8dba56aa11a44791e3ad9f01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964818"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a>Metodo FileExtensions della \_ classe TSApplicationFileExtensions di Win32

Fornisce un elenco delle estensioni dei nomi di file gestite da un'applicazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Percorso app* \[ in\]
</dt> <dd>

Percorso dell'applicazione.

</dd> <dt>

*Estensioni* \[ di out\]
</dt> <dd>

Estensioni dei nomi di file gestite dall'applicazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSApplicationFileExtensions Win32**](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

