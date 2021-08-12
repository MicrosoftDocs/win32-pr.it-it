---
title: Metodo ImportAgreementLicenseKeyPack della Win32_TSLicenseKeyPack classe
description: Importa, da un altro server licenze Desktop remoto, un key pack di licenza Servizi Desktop remoto acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del key pack.
ms.assetid: 3C29E691-3734-4D39-A89F-F381F285DC9E
ms.tgt_platform: multiple
keywords:
- Metodo ImportAgreementLicenseKeyPack Servizi Desktop remoto
- Il metodo ImportAgreementLicenseKeyPack Servizi Desktop remoto , Win32_TSLicenseKeyPack classe
- Win32_TSLicenseKeyPack classe Servizi Desktop remoto , metodo ImportAgreementLicenseKeyPack
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
ms.openlocfilehash: 3b911a722f4f26aaf83debcb70413cb9dad2b40d2ca12b4ad3310aee4510ca1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603804"
---
# <a name="importagreementlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a>Metodo ImportAgreementLicenseKeyPack della classe \_ Win32 TSLicenseKeyPack

Importa, da un altro server licenze Desktop remoto, un key pack di licenza Servizi Desktop remoto acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del key pack.

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

*Tipo di contratto* \[ Pollici\]
</dt> <dd>

Tipo di contratto.

<dt>

0
</dt> <dd>

Il Key Pack di licenza deriva da un Contratto Multilicenza Selezionato (per i clienti con 250 o più computer). Il *parametro sAgreementNumber è* il numero di registrazione (sette cifre numeriche) trovato nel modulo del contratto firmato.

</dd> <dt>

1
</dt> <dd>

Il Key Pack di licenza deriva da Enterprise contratto multilicenza per i clienti con 250 o più computer. Il *parametro sAgreementNumber è* il numero di registrazione (sette cifre numeriche) trovato nel modulo del contratto firmato.

</dd> <dt>

2
</dt> <dd>

Il key pack di licenza deriva da un contratto multilicenza Campus per un istituto di istruzione superiore. Il *parametro sAgreementNumber è* il numero di registrazione (sette cifre numeriche) trovato nel modulo del contratto firmato.

</dd> <dt>

3
</dt> <dd>

Il key pack di licenza deriva da un contratto multilicenza school per istituti primari e secondari. Il *parametro sAgreementNumber è* il numero di registrazione (sette cifre numeriche) trovato nel modulo del contratto firmato.

</dd> <dt>

4
</dt> <dd>

Il Key Pack di licenza deriva da un contratto di licenza del provider di servizi per i provider di servizi per la licenza del software Microsoft su base mensile. Il *parametro sAgreementNumber è* il numero di registrazione (sette cifre numeriche) trovato nel modulo del contratto firmato.

</dd> <dt>

5
</dt> <dd>

Il key pack di licenza deriva da un altro contratto di licenza, ad esempio Open Value, Multi-Year Open License e Open Subscription License. Il *parametro sAgreementNumber* è il numero di contratto fornito con le informazioni sul programma.

</dd> </dl> </dd> <dt>

*sAgreementNumber* \[ Pollici\]
</dt> <dd>

Numero di contratto o numero di registrazione. Il *parametro sAgreementNumber è* una stringa numerica di sette cifre senza trattini.

</dd> <dt>

*ProductVersion* \[ Pollici\]
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

*ProductType* \[ Pollici\]
</dt> <dd>

Tipo di prodotto.

<dt>

0
</dt> <dd>

Il Servizi Desktop remoto di prodotto del key pack di licenza è per ogni dispositivo. Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve avere una licenza.

</dd> <dt>

1
</dt> <dd>

Il Servizi Desktop remoto di prodotto del key pack di licenza è per utente. Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve avere una licenza.

</dd> <dt>

2
</dt> <dd>

Questo tipo di prodotto non è valido.

</dd> </dl> </dd> <dt>

*LicenseCount* \[ Pollici\]
</dt> <dd>

Numero di licenze da importare.

</dd> <dt>

*sSourceLSName* \[ Pollici\]
</dt> <dd>

Nome del server licenze Desktop remoto di origine. Si tratta del nome distinto completo o dell'indirizzo IP del server.

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

Se il metodo ha esito positivo, restituisce zero. Se il metodo ha esito negativo, restituisce un valore diverso da zero. Per un elenco dei codici di errore, vedere Servizi Desktop remoto [di errore del provider WMI](terminal-services-wmi-provider-error-codes.md).

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

 

 





