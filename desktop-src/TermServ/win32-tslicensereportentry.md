---
title: Win32_TSLicenseReportEntry classe
description: Fornisce i dettagli delle licenze Servizi Desktop remoto licenza di accesso client per utente (Servizi Desktop remoto \ 160; Licenza CAL per utente).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseReportEntry classe Servizi Desktop remoto
- Win32_TSLicenseReportEntry classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSLicenseReportEntry
- Win32_TSLicenseReportEntry.User
- Win32_TSLicenseReportEntry.ExpirationDate
- Win32_TSLicenseReportEntry.CALType
- Win32_TSLicenseReportEntry.ProductVersion
- Win32_TSLicenseReportEntry.ProductVersionID
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e08041ac0878f3466712001a0a5e2cc90eb74ea1e360da9785b5d84805574389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126521"
---
# <a name="win32_tslicensereportentry-class"></a>Classe \_ Win32 TSLicenseReportEntry

Fornisce informazioni dettagliate sulle licenze cal per Servizi Desktop remoto client per utente rilasciate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Win32_TSLicenseReportEntry
{
  string   User;
  DATETIME ExpirationDate;
  string   CALType;
  string   ProductVersion;
  uint32   ProductVersionID;
};
```

## <a name="members"></a>Members

La **classe \_ Win32 TSLicenseReportEntry** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Win32 \_ TSLicenseReportEntry** ha queste proprietà.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di licenza CAL rilasciata. Si tratta di uno dei valori seguenti.

**Windows Server 2008 R2 e Windows Server 2008:** Questa proprietà non è supportata.

"Licenza CAL TS per dispositivo incorporata"

"TS Per Device CAL"

"TS Internet Connector CAL"

"TS Per User CAL"

"TS o Servizi Desktop remoto per licenza CAL per dispositivo"

"Licenza CAL Per Utente di Servizi Desktop remoto o Servizi Desktop remoto"

"Licenza di sottoscrizione di VDI Standard Suite per dispositivo"

"Licenza di sottoscrizione Premium Suite per dispositivo VDI"

"Licenza CAL Servizi Desktop remoto per dispositivo"

"Licenza CAL Servizi Desktop remoto per utente"

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DATETIME**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data di scadenza della licenza rilasciata all'utente.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione di Servizi Desktop remoto per cui è stata rilasciata la licenza CAL Per Utente di Servizi Desktop remoto.

<dt>

"Windows Server 2012"
</dt> <dd>

Solo i server che Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008 sono supportati con questa licenza.

</dd> <dt>

"Windows Server 7"
</dt> <dd>

Con questa licenza sono supportati solo i server che eseguono Windows Server 2008 R2 o Windows Server 2008.

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

Solo i server che Windows Server 2008 sono supportati con questa licenza.

</dd> </dl>

</dd> <dt>

**ProductVersionID**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore della versione del prodotto per il key pack Servizi Desktop remoto licenza.

<dt>

4
</dt> <dd>

Windows Server 2012

</dd> <dt>

3
</dt> <dd>

Windows Server 2008 R2

</dd> <dt>

2
</dt> <dd>

Windows Server 2008

</dd> <dt>

1
</dt> <dd>

Non supportata.

</dd> <dt>

0
</dt> <dd>

Non supportata.

</dd> </dl>

</dd> <dt>

**Utente**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome dell'utente a cui è stata rilasciata la licenza.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per utilizzare questa classe, è necessario essere un membro del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le Windows WMI (Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, [vedere Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

[**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseKeyPack**](win32-tslicensekeypack.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

