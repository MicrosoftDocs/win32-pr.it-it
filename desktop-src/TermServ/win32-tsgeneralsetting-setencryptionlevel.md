---
title: Metodo SetEncryptionLevel della classe Win32_TSGeneralSetting
description: Il metodo SetEncryptionLevel imposta il livello di crittografia.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetEncryptionLevel
- Metodo SetEncryptionLevel Servizi Desktop remoto, classe Win32_TSGeneralSetting
- Classe Win32_TSGeneralSetting Servizi Desktop remoto, metodo SetEncryptionLevel
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
ms.openlocfilehash: b1fbe727c75851bb13252d196e1fe7d599f881c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120382"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a>Metodo SetEncryptionLevel della \_ classe TSGeneralSetting Win32

Il metodo **SetEncryptionLevel** imposta il livello di crittografia.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*MinEncryptionLevel* \[ in\]
</dt> <dd>

Livello di crittografia minimo da impostare.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Basso livello di crittografia. Solo i dati inviati dal client al server vengono crittografati con la crittografia a 56 bit. Si noti che i dati inviati dal server al client non sono crittografati.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Livello di crittografia compatibile con il client. Tutti i dati inviati da client a server e da server a client vengono crittografati al livello di attendibilità massima supportato dal client.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Livello elevato di crittografia. Tutti i dati inviati da client a server e da server a client vengono crittografati con la crittografia a 128 bit avanzata. I client che non supportano questo livello di crittografia non possono connettersi.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Crittografia conforme a FIPS. Tutti i dati inviati da client a server e da server a client vengono crittografati e decrittografati con gli algoritmi di crittografia Federal Information Processing Standard (FIPS) usando i moduli di crittografia Microsoft. FIPS è uno standard denominato "requisiti di sicurezza per i moduli di crittografia". FIPS 140-1 (1994) e FIPS 140-2 (2001) descrivono i requisiti governativi per i moduli di crittografia hardware e software utilizzati all'interno del governo degli Stati Uniti.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce l'esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

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

[**\_TSGeneralSetting Win32**](win32-tsgeneralsetting.md)
</dt> </dl>

 

