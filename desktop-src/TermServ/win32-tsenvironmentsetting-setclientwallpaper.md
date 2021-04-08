---
title: Metodo SetClientWallPaper della classe Win32_TSEnvironmentSetting
description: Il metodo SetClientWallPaper imposta la proprietà ClientWallPaper.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetClientWallPaper
- Metodo SetClientWallPaper Servizi Desktop remoto, classe Win32_TSEnvironmentSetting
- Classe Win32_TSEnvironmentSetting Servizi Desktop remoto, metodo SetClientWallPaper
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
ms.openlocfilehash: 04ae476134cf526602a059b4714cded6fd6c990e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741258"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a>Metodo SetClientWallPaper della \_ classe TSEnvironmentSetting Win32

Il metodo **SetClientWallPaper** imposta la proprietà **ClientWallPaper** .

## <a name="syntax"></a>Sintassi


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ClientWallPaper* \[ in\]
</dt> <dd>

Flag che disabilita o Abilita la proprietà **ClientWallPaper** , che specifica se nel client viene visualizzata l'immagine dello sfondo o dello sfondo.

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

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSEnvironmentSetting Win32**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

