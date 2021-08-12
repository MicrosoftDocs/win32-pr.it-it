---
title: Metodo FileExtensions della classe Win32_TSApplicationFileExtensions
description: Fornisce un elenco delle estensioni di file gestite da un'applicazione.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- Metodo FileExtensions Servizi Desktop remoto
- Il metodo FileExtensions Servizi Desktop remoto , Win32_TSApplicationFileExtensions classe
- Win32_TSApplicationFileExtensions classe Servizi Desktop remoto , metodo FileExtensions
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
ms.openlocfilehash: a3c7c44acd410566c4f048cdf36bac904c18b21df42f53543051e3b94f49bfbb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118609373"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a>Metodo FileExtensions della classe \_ TSApplicationFileExtensions Win32

Fornisce un elenco delle estensioni di file gestite da un'applicazione.

## <a name="syntax"></a>Sintassi


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AppPath* \[ Pollici\]
</dt> <dd>

Percorso dell'applicazione.

</dd> <dt>

*Estensioni* \[ Cambio\]
</dt> <dd>

Estensioni di file gestite dall'applicazione.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per Windows di Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>Tsallow.mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSApplicationFileExtensions**](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

