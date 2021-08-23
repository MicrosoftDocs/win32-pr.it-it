---
title: Metodo IsLSPreventUpgradeGPEnabled della classe Win32_TSLicenseServer
description: Recupera un valore che indica se \ 0034; impedisci l'aggiornamento della licenza \ 0034; l'impostazione di Criteri di gruppo è abilitata Desktop remoto server licenze.
ms.assetid: f78585b8-a50c-402b-ab20-f405eba0c079
ms.tgt_platform: multiple
keywords:
- Metodo IsLSPreventUpgradeGPEnabled Servizi Desktop remoto
- Metodo IsLSPreventUpgradeGPEnabled Servizi Desktop remoto , Win32_TSLicenseServer classe
- Win32_TSLicenseServer classe Servizi Desktop remoto , metodo IsLSPreventUpgradeGPEnabled
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
ms.openlocfilehash: 7958df7d153db0abafd8e463f22a181f2e5a639afa5c21cb7529a9cd5c005c5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119511696"
---
# <a name="islspreventupgradegpenabled-method-of-the-win32_tslicenseserver-class"></a>Metodo IsLSPreventUpgradeGPEnabled della classe \_ TSLicenseServer Win32

Recupera se l'impostazione dei criteri di gruppo "Impedisci l'aggiornamento delle licenze" è abilitata Desktop remoto server licenze.

## <a name="syntax"></a>Sintassi


```mof
uint32 IsLSPreventUpgradeGPEnabled(
  [out] boolean Enabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Abilitato* \[ Cambio\]
</dt> <dd>

Valore booleano che indica se l'impostazione del criterio "Impedisci l'aggiornamento della licenza" è abilitata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

Se l'impostazione del criterio "Impedisci aggiornamento licenze" è abilitata, il server licenze emettere una licenza CAL Servizi Desktop remoto temporanea al client solo se non è disponibile una licenza CAL Servizi Desktop remoto appropriata per il server Host sessione Desktop remoto Desktop remoto.

L'impostazione dei criteri si trova nel nodo seguente dell'editor Criteri di gruppo locali:

Configurazione computer Modelli amministrativi Windows licenze Servizi terminal di Servizi \\ \\ \\ \\ terminal

Managed Object Format file MOF contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

