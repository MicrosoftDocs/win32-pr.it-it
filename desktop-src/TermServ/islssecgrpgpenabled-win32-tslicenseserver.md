---
title: Metodo IsLSSecGrpGPEnabled della Win32_TSLicenseServer classe
description: Recupera un valore che indica se \ 0034;gruppo di sicurezza del server licenze \ 0034; l'impostazione di Criteri di gruppo è abilitata Desktop remoto server licenze.
ms.assetid: 715b619b-f082-4fed-ac4c-70d5e286e37c
ms.tgt_platform: multiple
keywords:
- Metodo IsLSSecGrpGPEnabled Servizi Desktop remoto
- Metodo IsLSSecGrpGPEnabled Servizi Desktop remoto , Win32_TSLicenseServer classe
- Win32_TSLicenseServer classe Servizi Desktop remoto , metodo IsLSSecGrpGPEnabled
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
ms.openlocfilehash: 688843106583ea0ca32a3cc8ac7142d51aac737ad6722ab4ef95621b63b66eb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138364"
---
# <a name="islssecgrpgpenabled-method-of-the-win32_tslicenseserver-class"></a>Metodo IsLSSecGrpGPEnabled della classe \_ Win32 TSLicenseServer

Recupera un valore che indica se l'impostazione di Criteri di gruppo "gruppo di sicurezza del server licenze" è abilitata Desktop remoto server licenze.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsLSSecGrpGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Abilitato* \[ Cambio\]
</dt> <dd>

Valore booleano che indica se l'impostazione dei criteri "gruppo di sicurezza del server licenze" è abilitata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere un membro del gruppo Administrators.

L'impostazione dei criteri "Gruppo di sicurezza del server licenze" consente di specificare i server Host sessione Desktop remoto (Host sessione Desktop remoto) a cui è consentito contattare il Servizi Desktop remoto server licenze per ottenere licenze CAL Servizi Desktop remoto. Se l'impostazione dei criteri è abilitata nel server licenze, il server risponderà solo alle richieste CAL Servizi Desktop remoto dai server Host sessione Desktop remoto i cui account computer sono membri del gruppo locale Computer Terminal Server nel server licenze.

L'impostazione dei criteri si trova nel nodo seguente dell'editor Criteri di gruppo locali:

Gestione licenze \\ Servizi Modelli amministrativi Windows Terminal \\ \\ Services \\

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

