---
title: Metodo SetClientWallPaper della classe Win32_TSEnvironmentSetting
description: Il metodo SetClientWallPaper imposta la proprietà ClientWallPaper.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- Metodo SetClientWallPaper Servizi Desktop remoto
- Metodo SetClientWallPaper Servizi Desktop remoto , Win32_TSEnvironmentSetting classe
- Win32_TSEnvironmentSetting classe Servizi Desktop remoto , metodo SetClientWallPaper
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6b314148bf630dace88c08b532cf80d2bed68d9e41f5566a198a79eef6e52a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126855"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a>Metodo SetClientWallPaper della classe \_ Win32 TSEnvironmentSetting

Il **metodo SetClientWallPaper** imposta la **proprietà ClientWallPaper.**

## <a name="syntax"></a>Sintassi


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ClientWallPaper* \[ Pollici\]
</dt> <dd>

Flag che disabilita o abilita la **proprietà ClientWallPaper,** che specifica se l'immagine di sfondo (o sfondo) viene visualizzata nel client.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

L'immagine di sfondo (o sfondo) non viene visualizzata nel client.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

L'immagine di sfondo (o sfondo) viene visualizzata nel client.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori. Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

