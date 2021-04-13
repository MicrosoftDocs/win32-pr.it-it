---
title: Metodo SetUserAuthenticationRequired della classe Win32_TSGeneralSetting
description: Abilita o Disabilita il requisito per cui gli utenti devono essere autenticati al momento della connessione impostando il valore della proprietà UserAuthenticationRequired.
ms.assetid: a0581326-fecc-4d23-87bf-3696c93366e8
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo SetUserAuthenticationRequired
- Metodo SetUserAuthenticationRequired Servizi Desktop remoto, classe Win32_TSGeneralSetting
- Classe Win32_TSGeneralSetting Servizi Desktop remoto, metodo SetUserAuthenticationRequired
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetUserAuthenticationRequired
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c0eb711d2146130ff0fd879953fc71fcba965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341132"
---
# <a name="setuserauthenticationrequired-method-of-the-win32_tsgeneralsetting-class"></a>Metodo SetUserAuthenticationRequired della \_ classe TSGeneralSetting Win32

Abilita o Disabilita il requisito per cui gli utenti devono essere autenticati al momento della connessione impostando il valore della proprietà **UserAuthenticationRequired** nella classe [**\_ TSGeneralSetting Win32**](win32-tsgeneralsetting.md) . Se **true**, ovvero abilitato, **UserAuthenticationRequired** richiede l'autenticazione dell'utente in fase di connessione per aumentare la protezione del server contro gli attacchi alla rete. Solo i client Remote Desktop Protocol (RDP) che supportano la versione 6,0 o successiva di RDP sono in grado di connettersi. Per evitare le rotture per gli utenti remoti, è consigliabile distribuire i client RDP che supportano la versione del protocollo appropriata prima di abilitare la proprietà.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetUserAuthenticationRequired(
  [in] uint32 UserAuthenticationRequired
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*UserAuthenticationRequired* \[ in\]
</dt> <dd>

Indica se è necessaria l'autenticazione utente.

<dt>

0 (0x0)
</dt> <dd>

Disabilitare il requisito per cui l'utente deve essere autenticato

</dd> <dt>

1 (0x1)
</dt> <dd>

Abilita il requisito per cui l'utente deve essere autenticato.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 in caso di esito positivo, in caso contrario restituisce un codice di errore WMI. Per un elenco di questi valori, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md) .

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

 

