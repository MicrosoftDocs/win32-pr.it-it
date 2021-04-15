---
title: Metodo ConvertLicenses della classe Win32_TSLicenseKeyPack
description: Converte le licenze nel Key Pack corrente.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ConvertLicenses
- Metodo ConvertLicenses Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ConvertLicenses
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
ms.openlocfilehash: 54f37b1d9804c5f14f89a7ff6b48f5f8fcbdc60b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400335"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a>Metodo ConvertLicenses della \_ classe TSLicenseKeyPack Win32

Converte le licenze nel Key Pack corrente. Se la licenza è una licenza per utente, viene convertita in una licenza per dispositivo. Se la licenza è una licenza per ogni dispositivo, viene convertita in una licenza per singolo utente.

## <a name="syntax"></a>Sintassi


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Numero* \[ di in\]
</dt> <dd>

Numero di licenze da convertire.

</dd> <dt>

*KeypackID* \[ out\]
</dt> <dd>

Identificatore del Key Pack risultante.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                 |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                            |
| Spazio dei nomi<br/>                | Root\\CIMv2<br/>                                                                    |
| MOF<br/>                      | <dl> <dt>TlsWmiProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TlsWmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> </dl>

 

 





