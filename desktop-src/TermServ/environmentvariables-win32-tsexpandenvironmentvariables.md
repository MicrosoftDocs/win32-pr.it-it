---
title: Metodo EnvironmentVariables della classe Win32_TSExpandEnvironmentVariables
description: Espande le variabili di ambiente definite dal sistema. | Metodo EnvironmentVariables della classe Win32_TSExpandEnvironmentVariables
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo EnvironmentVariables
- Metodo EnvironmentVariables Servizi Desktop remoto, classe Win32_TSExpandEnvironmentVariables
- Classe Win32_TSExpandEnvironmentVariables Servizi Desktop remoto, metodo EnvironmentVariables
topic_type:
- apiref
api_name:
- Win32_TSExpandEnvironmentVariables.EnvironmentVariables
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6f038ee1d5f93c11336657f9b8c1a80ecc05d6d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321265"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a>Metodo EnvironmentVariables della \_ classe TSExpandEnvironmentVariables Win32

Espande le variabili di ambiente definite dal sistema.

## <a name="syntax"></a>Sintassi


```mof
uint32 EnvironmentVariables(
  [in]  string OriginalString,
  [out] string ExpandedString
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*OriginalString* \[ in\]
</dt> <dd>

Stringa che contiene le variabili di ambiente da espandere.

</dd> <dt>

*ExpandedString* \[ out\]
</dt> <dd>

Stringa con le variabili di ambiente espanse.

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

[**\_TSExpandEnvironmentVariables Win32**](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

