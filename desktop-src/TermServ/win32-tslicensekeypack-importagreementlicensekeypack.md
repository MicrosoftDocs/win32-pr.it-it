---
title: Metodo ImportAgreementLicenseKeyPack della classe Win32_TSLicenseKeyPack
description: Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo ImportAgreementLicenseKeyPack
- Metodo ImportAgreementLicenseKeyPack Servizi Desktop remoto, classe Win32_TSLicenseKeyPack
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, metodo ImportAgreementLicenseKeyPack
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportAgreementLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff61d022f9cf195eb357817f7733f4ec49e2986f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121367"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Metodo ImportAgreementLicenseKeyPack della \_ classe TSLicenseKeyPack Win32

Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.

## <a name="syntax"></a>Sintassi


```mof
uint32 ImportAgreementLicenseKeyPack(
  [in]  uint32 AgreementType,
  [in]  string sAgreementNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*AgreementType* \[ in\]
</dt> <dd>

Tipo di contratto.

<dt>

0
</dt> <dd>

Il Key Pack per le licenze è da un contratto Select Volume License (per i clienti con 250 o più computer). Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.

</dd> <dt>

1
</dt> <dd>

Il Key Pack per le licenze è da un contratto multilicenza Enterprise per i clienti con 250 o più computer. Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.

</dd> <dt>

2
</dt> <dd>

Il Key Pack per le licenze è da un contratto multilicenza campus per un Istituto di istruzione superiore. Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.

</dd> <dt>

3
</dt> <dd>

Il Key Pack per le licenze è di un contratto multilicenza School per le istituzioni primarie e secondarie. Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.

</dd> <dt>

4
</dt> <dd>

Il Key Pack per le licenze è da un contratto di licenza di Service provider per i provider di servizi di concedere in licenza il software Microsoft su base mensile. Il parametro *sAgreementNumber* è il numero di registrazione (sette cifre numeriche) trovato nel modulo firmato Agreement.

</dd> <dt>

5
</dt> <dd>

Il Key Pack per le licenze è da un altro contratto di licenza, ad esempio Open Value, multiyear Open License e Open Subscription License. Il parametro *sAgreementNumber* è il numero di contratto fornito con le informazioni sul programma.

</dd> </dl> </dd> <dt>

*sAgreementNumber* \[ in\]
</dt> <dd>

Numero di contratto o numero di registrazione. Il parametro *sAgreementNumber* è una stringa numerica di sette cifre senza trattini.

</dd> <dt>

*ProductVersion* \[ in\]
</dt> <dd>

Versione del prodotto.

<dt>

0
</dt> <dd>

Non supportata.

</dd> <dt>

1
</dt> <dd>

Non supportata.

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> </dl> </dd> <dt>

*ProductType* \[ in\]
</dt> <dd>

Tipo di prodotto.

<dt>

0
</dt> <dd>

Il tipo di prodotto Servizi Desktop remoto License Key Pack è per dispositivo. Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve disporre di una licenza.

</dd> <dt>

1
</dt> <dd>

Il tipo di prodotto Servizi Desktop remoto License Key Pack è per utente. Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve disporre di una licenza.

</dd> <dt>

2
</dt> <dd>

Questo tipo di prodotto non è valido.

</dd> </dl> </dd> <dt>

*LicenseCount* \[ in\]
</dt> <dd>

Numero di licenze da importare.

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

 

 





