---
title: Metodo InstallAgreementLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Installa un Key Pack di licenza Servizi Desktop remoto acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.
ms.assetid: 70a0aac3-2709-47ba-bf6a-549393c4c115
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo InstallAgreementLicenseKeyPack
- Metodo InstallAgreementLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo InstallAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb891469feae169c1267c12c04af6d21415c309
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302459"
---
# <a name="installagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Metodo InstallAgreementLicenseKeyPack della \_ classe TSLicenseKeyPack Win32

Installa un Key Pack di licenza Servizi Desktop remoto acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.

## <a name="syntax"></a>Sintassi


```mof
uint32 InstallAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```

## <a name="parameters"></a>Parametri

*AgreementType* \[ in\]

Tipo di contratto.

| Valore | Descrizione |
|-------|-------------|
| 0 | Il Key Pack per le licenze è da un contratto Select Volume License (per i clienti con 250 o più computer). Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement. |
| 1 | Il Key Pack per le licenze è da un contratto multilicenza Enterprise per i clienti con 250 o più computer. Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement. |
| 2 | Il Key Pack per le licenze è da un contratto multilicenza campus per un Istituto di istruzione superiore. Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement. |
| 3 | Il Key Pack per le licenze è di un contratto multilicenza School per le istituzioni primarie e secondarie. Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement. |
| 4 | Il Key Pack per le licenze è da un contratto di licenza di Service provider per i provider di servizi di concedere in licenza il software Microsoft su base mensile. Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement. |
| 5 | Il Key Pack per le licenze è da un altro contratto di licenza, ad esempio Open Value, multiyear Open License e Open Subscription License. Il parametro *sAgreementNumber* è il numero di contratto fornito con le informazioni sul programma. |

*sAgreementNumber* \[ in\]

Numero di contratto o numero di registrazione. Il parametro *sAgreementNumber* è una stringa numerica di sette cifre senza trattini.

*ProductVersion* \[ in\]

Versione del prodotto.

| Valore | Descrizione |
|-------|-------------|
| 0 | Non supportato |
| 1 | Non supportato |
| 2 | Windows Server 2008/Windows Server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

*ProductType* \[ in\]

Tipo di prodotto.

| Valore | Descrizione |
|-------|-------------|
| 0 | Il tipo di prodotto Servizi Desktop remoto License Key Pack è per dispositivo. Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve disporre di una licenza. |
| 1 | Il tipo di prodotto Servizi Desktop remoto License Key Pack è per utente. Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve disporre di una licenza. |
| 2 | Questo tipo di prodotto non è valido. |

*LicenseCount* \[ in\]

Numero di licenze da installare.

*KeyPackId* \[ out\]

Riceve l'identificatore del Key Pack.

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

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> </dl>

 

