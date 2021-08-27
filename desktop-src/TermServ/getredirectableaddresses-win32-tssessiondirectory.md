---
title: Metodo GetRedirectableAddresses della Win32_TSSessionDirectory classe
description: Ottiene l'intero elenco di indirizzi DNS idonei.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- Metodo GetRedirectableAddresses Servizi Desktop remoto
- Metodo GetRedirectableAddresses Servizi Desktop remoto , Win32_TSSessionDirectory classe
- Win32_TSSessionDirectory classe Servizi Desktop remoto metodo , GetRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ff3e5dda8459361855c6ff2b287b71cbe02136b906e7defc816d4e7df727a08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010106"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>Metodo GetRedirectableAddresses della classe \_ Win32 TSSessionDirectory

Ottiene l'intero elenco di indirizzi DNS idonei.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*fTokenRedirection* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Flag che indica se deve essere utilizzato il reindirizzamento dei token.

</dd> <dt>

*Indirizzi IP* \[ Cambio\]
</dt> <dd>

Tipo: **\[ \] string**

L'intero elenco di indirizzi IP disponibili per il reindirizzamento.

</dd> <dt>

*AdapterNames* \[ Cambio\]
</dt> <dd>

Tipo: **\[ \] string**

Elenco dei nomi delle schede di rete associati agli indirizzi disponibili per il reindirizzamento.

</dd> <dt>

*NetConName* \[ Cambio\]
</dt> <dd>

Tipo: **\[ \] string**

Elenco di nomi di connessione di rete associati agli indirizzi disponibili per il reindirizzamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Restituisce 0 in caso di esito positivo. In caso contrario, restituisce un codice di errore WMI. Fare riferimento [Servizi Desktop remoto di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) per un elenco di questi valori.

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

 

