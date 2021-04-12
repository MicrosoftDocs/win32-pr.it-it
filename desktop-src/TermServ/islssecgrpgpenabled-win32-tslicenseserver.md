---
title: Metodo IsLSSecGrpGPEnabled della classe Win32_TSLicenseServer
description: Recupera un valore che indica se il gruppo di protezione \ 0034; License Server \ 0034; l'impostazione di criteri di gruppo è abilitata nel server licenze Desktop remoto.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLSSecGrpGPEnabled
- Metodo IsLSSecGrpGPEnabled Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsLSSecGrpGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSSecGrpGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27f3d7ec9de3d98849f9680f1b2a87bf5b22922a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120186"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a>Metodo IsLSSecGrpGPEnabled della \_ classe TSLicenseServer Win32

Recupera un valore che indica se l'impostazione di criteri di gruppo "gruppo di sicurezza del server licenze" è abilitata nel server licenze Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Abilitato* \[ out\]
</dt> <dd>

Valore booleano che indica se l'impostazione dei criteri "gruppo di sicurezza del server licenze" è abilitata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

L'impostazione dei criteri "gruppo di sicurezza del server licenze" consente di specificare i server di host sessione Desktop remoto (host sessione Desktop remoto) a cui è consentito contattare il server licenze per ottenere Servizi Desktop remoto licenze CAL (Client Access License). Se l'impostazione dei criteri è abilitata nel server licenze, il server risponderà solo alle richieste CAL Servizi Desktop remoto dei server Host sessione Desktop remoto i cui account computer sono membri del gruppo locale computer Terminal Server nel server licenze.

L'impostazione dei criteri si trova nel nodo seguente di Editor criteri di gruppo locali:

Configurazione computer \\ modelli amministrativi \\ componenti di \\ Servizi Terminal Servizi terminal di Windows \\

I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

