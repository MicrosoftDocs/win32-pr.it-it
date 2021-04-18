---
title: Classe Win32_TSLicenseReportEntry
description: Fornisce i dettagli della licenza di accesso client per utente Servizi Desktop remoto pubblicata (RDS \ 160; CAL per utente).
ms.assetid: 75fa7f39-af5b-45a0-ba2b-5c667edfec16
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseReportEntry Servizi Desktop remoto
- Classe Win32_TSLicenseReportEntry Servizi Desktop remoto, descritta
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
ms.openlocfilehash: 44fa97a91561a9d4cf3fd571c773288796754858
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400271"
---
# <a name="win32_tslicensereportentry-class"></a>Win32 \_ TSLicenseReportEntry (classe)

Fornisce i dettagli della licenza di accesso client per utente (CAL per utente) del Servizi Desktop remoto emesso.

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

La classe **Win32 \_ TSLicenseReportEntry** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSLicenseReportEntry** dispone di queste proprietà.

<dl> <dt>

**CALType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di licenza CAL rilasciata. Si tratta di uno dei valori seguenti.

**Windows server 2008 R2 e Windows server 2008:** Questa proprietà non è supportata.

"Licenze CAL per dispositivo predefinite"

"Licenze CAL per dispositivo"

"CAL Internet Connector CAL"

"Licenza CAL per utente di servizi Terminal"

Licenza CAL per dispositivo di Servizi terminal o RDS

Licenza CAL per utente di Servizi terminal o RDS

"Licenza abbonamento VDI Standard Suite per dispositivo"

"Licenza di sottoscrizione di VDI Premium Suite per dispositivo"

"RDS per dispositivo CAL"

"CAL per utente per utente"

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data di scadenza della licenza rilasciata all'utente.

</dd> <dt>

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione di Servizi Desktop remoto per cui è stata rilasciata la licenza CAL per utente.

<dt>

"Windows Server 2012"
</dt> <dd>

Con questa licenza sono supportati solo i server che eseguono Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008.

</dd> <dt>

"Windows Server 7"
</dt> <dd>

Con questa licenza sono supportati solo i server che eseguono Windows Server 2008 R2 o Windows Server 2008.

</dd> <dt>

"Windows Server 2008"
</dt> <dd>

Con questa licenza sono supportati solo i server che eseguono Windows Server 2008.

</dd> </dl>

</dd> <dt>

**ProductVersionID**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore della versione del prodotto per il Key Pack di Servizi Desktop remoto License.

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

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nome dell'utente a cui è stata emessa la licenza.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per utilizzare questa classe, è necessario essere membri del gruppo Administrators.

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

[**FetchReportEntries**](fetchreportentries-win32-tslicensereport.md)
</dt> <dt>

[**\_TSIssuedLicense Win32**](win32-tsissuedlicense.md)
</dt> <dt>

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

