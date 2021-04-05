---
title: Metodo seprovider della classe Win32_SessionDirectoryVMMPlugin
description: Imposta il nome del provider del plug-in.
ms.assetid: fefb7c19-2bab-4ae3-b88b-20da5fd19ff3
ms.tgt_platform: multiple
keywords:
- Metodo seprovider Servizi Desktop remoto
- Metodo seprovider Servizi Desktop remoto, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Servizi Desktop remoto, metodo seprovider
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetProvider
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205a88ecbd67dcf3b009577fa7384e074cc68487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741479"
---
# <a name="setprovider-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Metodo seprovider della classe Win32 \_ SessionDirectoryVMMPlugin

Imposta il nome del provider del plug-in.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetProvider(
  [in] string sProvider
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sProvider* \[ in\]
</dt> <dd>

Nome del provider del plug-in.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SessionDirectoryVMMPlugin Win32**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





