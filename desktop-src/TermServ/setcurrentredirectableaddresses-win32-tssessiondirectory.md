---
title: Metodo SetCurrentRedirectableAddresses della classe Win32_TSSessionDirectory
description: Imposta l'elenco configurato di indirizzi DNS idonei che possono essere usati per il reindirizzamento.
ms.assetid: cad6a8a8-fdf1-406e-abeb-37acb396ac16
ms.tgt_platform: multiple
keywords:
- Metodo SetCurrentRedirectableAddresses Servizi Desktop remoto
- Metodo SetCurrentRedirectableAddresses Servizi Desktop remoto , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Servizi Desktop remoto, metodo SetCurrentRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf1e9ab7b385111ccf91af9b4e3d6ed8bed0191f2d044c02a41705dbbc4f781
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756101"
---
# <a name="setcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>Metodo SetCurrentRedirectableAddresses della classe \_ Win32 TSSessionDirectory

Il **metodo SetCurrentRedirectableAddresses imposta** l'elenco configurato di indirizzi DNS idonei che possono essere usati per il reindirizzamento.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetCurrentRedirectableAddresses(
  [in] uint32 fTokenRedirection,
  [in] string IPAddresses[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fTokenRedirection* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Flag che indica se è necessario usare il reindirizzamento dei token.

</dd> <dt>

*Indirizzi IP* \[ Pollici\]
</dt> <dd>

Tipo: **\[ \] string**

Matrice di stringhe che rappresenta l'elenco di indirizzi IP dns idonei che possono essere usati per il reindirizzamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Restituisce 0 se l'operazione ha esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori.

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

