---
title: Metodo InitialProgram della classe Win32_TSEnvironmentSetting
description: Il metodo InitialProgram imposta le proprietà del programma di avvio, ad esempio il nome, la directory di lavoro e il percorso del programma, da avviare immediatamente dopo l'accesso al server host sessione Desktop remoto (Host sessione Desktop remoto).
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- Metodo InitialProgram Servizi Desktop remoto
- Metodo InitialProgram Servizi Desktop remoto , Win32_TSEnvironmentSetting classe
- Win32_TSEnvironmentSetting classe Servizi Desktop remoto , metodo InitialProgram
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d13aaa0e4dfb4e0d16bea89bf871a7a890c0f375fd928e70fd99aed20c003be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126996"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a>Metodo InitialProgram della classe \_ TSEnvironmentSetting Win32

Il **metodo InitialProgram** imposta le proprietà del programma di avvio, ad esempio il nome, la directory di lavoro e il percorso del programma, da avviare immediatamente dopo l'accesso al server host sessione Desktop remoto (Host sessione Desktop remoto).

## <a name="syntax"></a>Sintassi


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*InitialProgramPath* \[ Pollici\]
</dt> <dd>

Nome e percorso del programma di avvio.

</dd> <dt>

*Startin* \[ Pollici\]
</dt> <dd>

Percorso della directory di lavoro del programma di avvio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori. Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

