---
title: Metodo Revoke della classe Win32_TSIssuedLicense
description: Revoca le licenze di accesso client per dispositivo Servizi Desktop remoto (RDS \ 160; Licenze CAL per dispositivo rappresentate dall' \_ oggetto Win32 TSIssuedLicense. Non si tratta di una funzione statica.
ms.assetid: b1eb7448-5d8e-4c2d-ba52-9363e8e0297a
ms.tgt_platform: multiple
keywords:
- Metodo Revoke Servizi Desktop remoto
- Revoke (metodo) Servizi Desktop remoto, classe Win32_TSIssuedLicense
- Classe Win32_TSIssuedLicense Servizi Desktop remoto, Metodo Revoke
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense.Revoke
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63993ede5346f5b3cb56fcfa458d4cdce7dd58b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743623"
---
# <a name="revoke-method-of-the-win32_tsissuedlicense-class"></a>Metodo Revoke della \_ classe Win32 TSIssuedLicense

Revoca le licenze CAL per dispositivo Servizi Desktop remoto per ogni dispositivo rappresentate dall'oggetto [**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md) . Non si tratta di una funzione statica.

## <a name="syntax"></a>Sintassi


```mof
uint32 Revoke(
  [out] uint32   RevokableCals,
  [out] DATETIME NextRevokeAllowedOn
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*RevokableCals* \[ out\]
</dt> <dd>

Numero di licenze CAL Servizi Desktop remoto dello stesso tipo dell'oggetto corrente che può essere revocato.

</dd> <dt>

*NextRevokeAllowedOn* \[ out\]
</dt> <dd>

Data in cui l'amministratore può provare a revocare le licenze. Questo parametro contiene solo dati validi quando la chiamata al metodo **Revoke** non è riuscita perché è stato raggiunto il numero massimo di revoche.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

È possibile revocare solo le licenze CAL per dispositivo.

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

[**\_TSIssuedLicense Win32**](win32-tsissuedlicense.md)
</dt> </dl>

 

