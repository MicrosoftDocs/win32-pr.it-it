---
title: Metodo ImportLicenseKeyPackOffline della classe Win32_TSLicenseKeyPack
description: Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License che usa un identificatore di licenza ricevuto tramite Internet o il telefono.
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ImportLicenseKeyPackOffline
- Metodo ImportLicenseKeyPackOffline Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ImportLicenseKeyPackOffline
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de474cce6eb91cdc605588f7f4a63d97f985769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517871"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Metodo ImportLicenseKeyPackOffline della \_ classe TSLicenseKeyPack Win32

Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License che usa un identificatore di licenza ricevuto tramite Internet o il telefono.

## <a name="syntax"></a>Sintassi


```mof
uint32 ImportLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*sLicenseKeyPackId* \[ in\]
</dt> <dd>

Contiene il codice di licenza a 35 caratteri. Come input è necessario assegnare solo la stringa di caratteri alfanumerici a 35 caratteri. Nessun trattino da aggiungere.

</dd> <dt>

*sSourceLSName* \[ in\]
</dt> <dd>

Nome dell'origine Desktop remoto server licenze. Si tratta del nome distinto completo o dell'indirizzo IP del server.

</dd> <dt>

*sSourceLSProductId* \[ in\]
</dt> <dd>

Identificatore del server licenze Desktop remoto. È una stringa alfanumerica di 35 caratteri che non può includere trattini.

</dd> <dt>

*KeyPackId* \[ out\]
</dt> <dd>

Riceve l'identificatore del Key Pack.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

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

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





