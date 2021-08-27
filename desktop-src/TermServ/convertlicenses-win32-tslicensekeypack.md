---
title: Metodo ConvertLicenses della Win32_TSLicenseKeyPack classe
description: Converte le licenze nel Key Pack corrente.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- Metodo ConvertLicenses Servizi Desktop remoto
- Metodo ConvertLicenses Servizi Desktop remoto , Win32_TSLicenseKeyPack classe
- Win32_TSLicenseKeyPack classe Servizi Desktop remoto , metodo ConvertLicenses
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edfb65ea7429af14e633c8dee655b4977427e3a685e1404856fd9b5f2daf2ce4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099571"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a>Metodo ConvertLicenses della classe \_ Win32 TSLicenseKeyPack

Converte le licenze nel Key Pack corrente. Se la licenza è una licenza per utente, viene convertita in una licenza per dispositivo. Se la licenza è una licenza per dispositivo, viene convertita in una licenza per utente.

## <a name="syntax"></a>Sintassi


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Conteggio* \[ Pollici\]
</dt> <dd>

Numero di licenze da convertire.

</dd> <dt>

*KeypackID* \[ Cambio\]
</dt> <dd>

Identificatore del key pack risultante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco dei codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI.](terminal-services-wmi-provider-error-codes.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





