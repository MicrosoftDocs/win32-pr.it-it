---
title: Metodo seenabled della classe Win32_SessionDirectoryVMMPlugin
description: Abilita o Disabilita il plug-in.
ms.assetid: 25ce0614-5c3b-4a79-9174-1a9de1eb6c33
ms.tgt_platform: multiple
keywords:
- Metodo seenabled Servizi Desktop remoto
- Metodo seenabled Servizi Desktop remoto, classe Win32_SessionDirectoryVMMPlugin
- Classe Win32_SessionDirectoryVMMPlugin Servizi Desktop remoto, metodo seenabled
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetEnabled
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7089a21f143b6f3b27fe9fe58563e6777bf2f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743610"
---
# <a name="setenabled-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Metodo seenabled della classe Win32 \_ SessionDirectoryVMMPlugin

Abilita o Disabilita il plug-in.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Abilitato* \[ in\]
</dt> <dd>

Indica se il plug-in è abilitato o disabilitato. **True** se il plug-in è abilitato o **false** in caso contrario.

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

 

 





