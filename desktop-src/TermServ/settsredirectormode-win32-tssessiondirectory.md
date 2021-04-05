---
title: Metodo SetTSRedirectorMode della classe Win32_TSSessionDirectory
description: Imposta il valore per indicare se il server fungerà da redirector Servizi Desktop remoto.
ms.assetid: abdb92df-1e49-4445-ba02-bb83fd1ca541
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetTSRedirectorMode
- Metodo SetTSRedirectorMode Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo SetTSRedirectorMode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetTSRedirectorMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95e3195a83a32dca0c8e4a96de211a72a66a8f3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874445"
---
# <a name="settsredirectormode-method-of-the-win32_tssessiondirectory-class"></a>Metodo SetTSRedirectorMode della \_ classe TSSessionDirectory Win32

Imposta il valore per indicare se il server fungerà da redirector Servizi Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetTSRedirectorMode(
  [in] uint32 TSRedirValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TSRedirValue* \[ in\]
</dt> <dd>

Tipo: **UInt32**

Consente di specificare se il server fungerà da redirector Servizi Desktop remoto. Può corrispondere a uno dei valori seguenti.

<dt>

0
</dt> <dd>

Il server fungerà da redirector Servizi Desktop remoto.

</dd> <dt>

1
</dt> <dd>

Il server non fungerà da redirector Servizi Desktop remoto.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) . Il metodo restituisce un errore se l'impostazione è sotto il controllo criteri di gruppo.

## <a name="remarks"></a>Commenti

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                               |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

