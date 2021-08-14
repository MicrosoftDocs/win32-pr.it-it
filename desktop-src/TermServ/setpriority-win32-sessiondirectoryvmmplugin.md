---
title: Metodo SetPriority della Win32_SessionDirectoryVMMPlugin classe
description: Imposta la priorità del plug-in.
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- Metodo SetPriority Servizi Desktop remoto
- Metodo SetPriority Servizi Desktop remoto , Win32_SessionDirectoryVMMPlugin classe
- Win32_SessionDirectoryVMMPlugin classe Servizi Desktop remoto, metodo SetPriority
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetPriority
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dfe18b5998a1b8576cbd1a8f3c793e355469cfeff44f585dcb167a3b154803a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987741"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Metodo SetPriority della classe \_ SessionDirectoryVMMPlugin Win32

Imposta la priorità del plug-in.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Priorità* \[ Pollici\]
</dt> <dd>

Priorità del plug-in. Maggiore è il valore, maggiore sarà la priorità del plug-in. La priorità è zero per impostazione predefinita.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                              |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                      |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





