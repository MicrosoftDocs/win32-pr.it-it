---
title: Metodo SetTSRedirectorMode della classe Win32_TSSessionDirectory
description: Imposta il valore per indicare se il server fungerà da Servizi Desktop remoto redirector.
ms.assetid: abdb92df-1e49-4445-ba02-bb83fd1ca541
ms.tgt_platform: multiple
keywords:
- Metodo SetTSRedirectorMode Servizi Desktop remoto
- Metodo SetTSRedirectorMode Servizi Desktop remoto , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Servizi Desktop remoto, metodo SetTSRedirectorMode
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
ms.openlocfilehash: 6350d4b9a4858991616d45eb2b1092fe406c59b55b11c494a7f19be53dbb60ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118127277"
---
# <a name="settsredirectormode-method-of-the-win32_tssessiondirectory-class"></a>Metodo SetTSRedirectorMode della classe \_ TSSessionDirectory Win32

Imposta il valore per indicare se il server fungerà da Servizi Desktop remoto redirector.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetTSRedirectorMode(
  [in] uint32 TSRedirValue
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TSRedirValue* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Specifica se il server fungerà da Servizi Desktop remoto client. Può essere uno dei valori seguenti.

<dt>

0
</dt> <dd>

Il server fungerà da Servizi Desktop remoto remoto.

</dd> <dt>

1
</dt> <dd>

Il server non fungerà da Servizi Desktop remoto client.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto codici di errore del provider WMI,](terminal-services-wmi-provider-error-codes.md) vedere . Il metodo restituisce un errore se l'impostazione è sotto il controllo di Criteri di gruppo.

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Fine del supporto client<br/>    | Nessuno supportato<br/>                                                               |
| Fine del supporto server<br/>    | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | TerminalServices \\ CIMv2 \\ radice<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

