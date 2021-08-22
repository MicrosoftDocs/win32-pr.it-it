---
title: Metodo SetSecurityLayer della classe Win32_TSGeneralSetting
description: Il metodo SetSecurityLayer imposta il livello di sicurezza.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- Metodo SetSecurityLayer Servizi Desktop remoto
- Metodo SetSecurityLayer Servizi Desktop remoto , Win32_TSGeneralSetting classe
- Win32_TSGeneralSetting classe Servizi Desktop remoto, metodo SetSecurityLayer
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e01f761b63be028e2c507644f160b6742f9d781e517ea03ce549e3ac84419c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513871"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a>Metodo SetSecurityLayer della classe \_ TSGeneralSetting Win32

Il **metodo SetSecurityLayer** imposta il livello di sicurezza.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SecurityLayer* \[ Pollici\]
</dt> <dd>

Livello di sicurezza da impostare. Se il livello di crittografia corrente è 1, il valore 2 per *SecurityLayer* non è valido.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Livello di sicurezza RDP** (0)


</dt> <dd>

La comunicazione tra il server e il client userà la crittografia RDP nativa.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (1)


</dt> <dd>

Verrà usato il livello più sicuro supportato dal client. Se supportato, verrà usato SSL (TLS 1.0).

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (2)


</dt> <dd>

SSL (TLS 1.0) verrà usato per l'autenticazione server e per crittografare tutti i dati trasferiti tra il server e il client. Questa impostazione richiede che il server abbia un certificato compatibile con SSL. Questa impostazione non è compatibile con un **valore MinEncryptionLevel** pari a 1.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce Success in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto codici di errore del provider WMI,](terminal-services-wmi-provider-error-codes.md) vedere .

## <a name="remarks"></a>Commenti

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**Win32 \_ TSGeneralSetting**](win32-tsgeneralsetting.md)
</dt> <dt>

[**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

