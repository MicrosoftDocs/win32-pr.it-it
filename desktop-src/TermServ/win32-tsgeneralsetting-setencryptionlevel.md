---
title: Metodo SetEncryptionLevel della classe Win32_TSGeneralSetting
description: Il metodo SetEncryptionLevel imposta il livello di crittografia.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- Metodo SetEncryptionLevel Servizi Desktop remoto
- Metodo SetEncryptionLevel Servizi Desktop remoto , Win32_TSGeneralSetting classe
- Win32_TSGeneralSetting classe Servizi Desktop remoto metodo SetEncryptionLevel
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetEncryptionLevel
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54aacf931a66d6d4bdd4daa24a6432e4caa7fb01695aebbe4324b17ab5f2bed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348843"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a>Metodo SetEncryptionLevel della classe \_ TSGeneralSetting Win32

Il **metodo SetEncryptionLevel** imposta il livello di crittografia.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MinEncryptionLevel* \[ Pollici\]
</dt> <dd>

Livello di crittografia minimo da impostare.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Basso livello di crittografia. Solo i dati inviati dal client al server vengono crittografati usando la crittografia a 56 bit. Si noti che i dati inviati dal server al client non sono crittografati.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Livello di crittografia compatibile con il client. Tutti i dati inviati dal client al server e dal server al client vengono crittografati alla massima potenza della chiave supportata dal client.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Livello elevato di crittografia. Tutti i dati inviati dal client al server e dal server al client vengono crittografati usando la crittografia avanzata a 128 bit. I client che non supportano questo livello di crittografia non possono connettersi.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Crittografia conforme a FIPS. Tutti i dati inviati dal client al server e dal server al client vengono crittografati e decrittografati con gli algoritmi di crittografia Federal Information Processing Standard (FIPS) usando i moduli di crittografia Microsoft. FIPS è uno standard intitolato "Requisiti di sicurezza per i moduli crittografici". FIPS 140-1 (1994) e FIPS 140-2 (2001) descrivono i requisiti governativi per i moduli di crittografia hardware e software usati all'interno del governo degli Stati Uniti.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce Success in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un [elenco Servizi Desktop remoto codici di errore del provider WMI,](terminal-services-wmi-provider-error-codes.md) vedere .

## <a name="remarks"></a>Commenti

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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
</dt> </dl>

 

