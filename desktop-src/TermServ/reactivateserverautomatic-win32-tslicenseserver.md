---
title: Metodo ReactivateServerAutomatic della classe Win32_TSLicenseServer
description: Riattiva il server licenze Desktop remoto usando una connessione automatica a Internet.
ms.assetid: 98b9b8e5-4de4-418c-9175-58e8b84784d5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ReactivateServerAutomatic
- Metodo ReactivateServerAutomatic Servizi Desktop remoto, classe Win32_TSLicenseServer
- Classe Win32_TSLicenseServer Servizi Desktop remoto, metodo ReactivateServerAutomatic
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ReactivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b9df7314abc3dccf6458322911c50d6120ad10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302450"
---
# <a name="reactivateserverautomatic-method-of-the-win32_tslicenseserver-class"></a>Metodo ReactivateServerAutomatic della \_ classe TSLicenseServer Win32

Riattiva il server licenze Desktop remoto usando una connessione automatica a Internet.

## <a name="syntax"></a>Sintassi


```mof
uint32 ReactivateServerAutomatic(
  [in]  uint32 Reason,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Motivo* \[ in\]
</dt> <dd>

Motivo dell'attivazione. Può essere uno dei valori seguenti.

<dt>

0
</dt> <dd>

Il server è stato ridistribuito.

</dd> <dt>

1
</dt> <dd>

Il certificato è danneggiato.

</dd> <dt>

2
</dt> <dd>

La chiave privata è stata compromessa.

</dd> <dt>

3
</dt> <dd>

Il codice di attivazione è scaduto.

</dd> <dt>

4
</dt> <dd>

Il server è stato aggiornato.

</dd> </dl> </dd> <dt>

*ActivationStatus* \[ out\]
</dt> <dd>

Lo stato di attivazione restituito può essere uno dei valori seguenti.

<dt>

0
</dt> <dd>

Il server licenze Desktop remoto viene attivato.

</dd> <dt>

1
</dt> <dd>

Il server licenze Desktop remoto non è attivato.

</dd> <dt>

2
</dt> <dd>

Si è verificato un errore sconosciuto. Non è noto se il server licenze Desktop remoto è attivato.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco di codici di errore, vedere [Servizi Desktop remoto codici di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Commenti

Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.

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

 

