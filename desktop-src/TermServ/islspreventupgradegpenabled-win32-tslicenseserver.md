---
title: Metodo IsLSPreventUpgradeGPEnabled della classe Win32_TSLicenseServer
description: Recupera un valore che indica se \ 0034; Impedisci l'aggiornamento della licenza \ 0034; l'impostazione di criteri di gruppo è abilitata nel server licenze Desktop remoto.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo IsLSPreventUpgradeGPEnabled
- Metodo IsLSPreventUpgradeGPEnabled Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo IsLSPreventUpgradeGPEnabled
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.IsLSPreventUpgradeGPEnabled
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205dc1ac05f5dca44297f8d80653ad51b7518d38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301868"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a>Metodo IsLSPreventUpgradeGPEnabled della \_ classe TSLicenseServer Win32

Recupera un valore che indica se l'impostazione di criteri di gruppo "Impedisci aggiornamento licenza" è abilitata nel server licenze Desktop remoto.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Abilitato* \[ out\]
</dt> <dd>

Valore booleano che indica se l'impostazione dei criteri "Impedisci aggiornamento licenza" è abilitata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Se è abilitata l'impostazione dei criteri "Impedisci aggiornamento licenza", il server licenze emetterà solo una licenza di autorizzazione Servizi Desktop remoto temporanea per il client se non è disponibile una licenza CAL Servizi Desktop remoto appropriata per il server host sessione Desktop remoto (host sessione Desktop remoto).

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

 

