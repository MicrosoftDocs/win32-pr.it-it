---
title: Metodo ImportLicenseKeyPackOffline della classe Win32_TSLicenseKeyPack
description: Importa, da un altro server licenze Desktop remoto, un key pack di licenza Servizi Desktop remoto che usa un identificatore di licenza ricevuto tramite Internet o il telefono.
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- Metodo ImportLicenseKeyPackOffline Servizi Desktop remoto
- Metodo ImportLicenseKeyPackOffline Servizi Desktop remoto , Win32_TSLicenseKeyPack classe
- Win32_TSLicenseKeyPack classe Servizi Desktop remoto , metodo ImportLicenseKeyPackOffline
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
ms.openlocfilehash: 5c7d5be5dc8cfd9f654c09d989149a423351689f420a52ca1756fb197260e800
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348632"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a>Metodo ImportLicenseKeyPackOffline della classe \_ Win32 TSLicenseKeyPack

Importa, da un altro server licenze Desktop remoto, un key pack di licenza Servizi Desktop remoto che usa un identificatore di licenza ricevuto tramite Internet o il telefono.

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

*sLicenseKeyPackId* \[ Pollici\]
</dt> <dd>

Contiene il codice di licenza di 35 caratteri. Come input deve essere specificata solo la stringa di caratteri alfanumerici di 35 caratteri. Non è necessario aggiungere trattini.

</dd> <dt>

*sSourceLSName* \[ Pollici\]
</dt> <dd>

Nome del server licenze Desktop remoto origine. Si tratta del nome distinto completo o dell'indirizzo IP del server.

</dd> <dt>

*sSourceLSProductId* \[ Pollici\]
</dt> <dd>

Identificatore Desktop remoto server licenze. è una stringa alfanumerica di 35 caratteri che non può includere trattini.

</dd> <dt>

*KeyPackId* \[ Cambio\]
</dt> <dd>

Riceve l'identificatore del key pack.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

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

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





