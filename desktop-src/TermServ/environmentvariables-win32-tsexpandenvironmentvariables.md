---
title: Metodo EnvironmentVariables della classe Win32_TSExpandEnvironmentVariables
description: Espande le variabili di ambiente definite dal sistema. | Metodo EnvironmentVariables della classe Win32_TSExpandEnvironmentVariables
ms.assetid: eff0dcdf-ef98-4730-9b0c-4f44250a607b
ms.tgt_platform: multiple
keywords:
- Metodo EnvironmentVariables Servizi Desktop remoto
- Metodo EnvironmentVariables Servizi Desktop remoto , Win32_TSExpandEnvironmentVariables classe
- Win32_TSExpandEnvironmentVariables classe Servizi Desktop remoto, metodo EnvironmentVariables
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
ms.openlocfilehash: 49416291293d621739ab7c721ca349f5d87bb4582d1289f431a8c443d3414da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353893"
---
# <a name="environmentvariables-method-of-the-win32_tsexpandenvironmentvariables-class"></a>Metodo EnvironmentVariables della classe \_ Win32 TSExpandEnvironmentVariables

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

*OriginalString* \[ Pollici\]
</dt> <dd>

Stringa contenente le variabili di ambiente da espandere.

</dd> <dt>

*ExpandedString* \[ Cambio\]
</dt> <dd>

Stringa con le variabili di ambiente espanse.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per Windows di Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**Win32 \_ TSExpandEnvironmentVariables**](win32-tsexpandenvironmentvariables.md)
</dt> </dl>

 

