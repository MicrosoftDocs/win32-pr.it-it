---
title: Classe Win32_TSLicenseKeyPack
description: Fornisce metodi e proprietà per la visualizzazione e l'installazione Servizi Desktop remoto key pack di licenza.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Win32_TSLicenseKeyPack classe Servizi Desktop remoto
- Win32_TSLicenseKeyPack classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack
- Win32_TSLicenseKeyPack.KeyPackId
- Win32_TSLicenseKeyPack.Description
- Win32_TSLicenseKeyPack.KeyPackType
- Win32_TSLicenseKeyPack.ProductType
- Win32_TSLicenseKeyPack.ProductVersion
- Win32_TSLicenseKeyPack.ProductVersionID
- Win32_TSLicenseKeyPack.TotalLicenses
- Win32_TSLicenseKeyPack.IssuedLicenses
- Win32_TSLicenseKeyPack.AvailableLicenses
- Win32_TSLicenseKeyPack.ExpirationDate
- Win32_TSLicenseKeyPack.AccessRights
- Win32_TSLicenseKeyPack.TypeAndModel
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7927270f262d0a66722660bf4b2c8f15cf75f49bb807abcff604af9edf58d99b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137814"
---
# <a name="win32_tslicensekeypack-class"></a>Classe \_ Win32 TSLicenseKeyPack

Fornisce metodi e proprietà per la visualizzazione e l'installazione Servizi Desktop remoto key pack di licenza.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSLicenseKeyPack
{
  uint32   KeyPackId;
  string   Description;
  uint32   KeyPackType;
  uint32   ProductType;
  string   ProductVersion;
  uint32   ProductVersionID;
  uint32   TotalLicenses;
  uint32   IssuedLicenses;
  uint32   AvailableLicenses;
  DATETIME ExpirationDate;
  uint32   AccessRights;
  string   TypeAndModel;
};
```

## <a name="members"></a>Members

La **classe \_ Win32 TSLicenseKeyPack** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Win32 \_ TSLicenseKeyPack** include questi metodi.



| Metodo                                                                                                        | Descrizione                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertLicenses**](convertlicenses-win32-tslicensekeypack.md)                                             | Converte le licenze nel Key Pack corrente.<br/>                                                                                                                                                                                 |
| [**ImportAgreementLicenseKeyPack**](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | Importa, da un altro server licenze Desktop remoto, un key pack di licenza Servizi Desktop remoto acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del key pack.<br/> |
| [**ImportLicenseKeyPackOffline**](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | Importa, da un altro server licenze Desktop remoto, un key pack di licenza Servizi Desktop remoto che usa un identificatore di licenza ricevuto tramite Internet o il telefono.<br/>                                               |
| [**ImportOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | Importa, da un altro server Desktop remoto licenze, un key pack open license Servizi Desktop remoto licenza.<br/>                                                                                                                 |
| [**ImportRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | Importa, da un altro server Desktop remoto licenze, un key pack Servizi Desktop remoto licenza acquistata tramite un canale di vendita al dettaglio.<br/>                                                                                   |
| [**InstallAgreementLicenseKeyPack**](installagreementlicensekeypack-win32-tslicensekeypack.md)               | Installa un key pack Servizi Desktop remoto licenza acquistata tramite una licenza con contratto.<br/>                                                                                                                           |
| [**InstallLicenseKeyPack**](installlicensekeypack-win32-tslicensekeypack.md)                                 | Installa un key pack Servizi Desktop remoto licenza che usa un ID del key pack di licenza ricevuto tramite Internet o il telefono.<br/>                                                                                          |
| [**InstallOpenLicenseKeyPack**](installopenlicensekeypack-win32-tslicensekeypack.md)                         | Installa un key pack Servizi Desktop remoto licenza che è stato acquistato tramite un contratto di licenza aperto.<br/>                                                                                                                      |
| [**InstallRetailPurchaseLicenseKeyPack**](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | Installa un key pack Servizi Desktop remoto licenza acquistata tramite un punto vendita al dettaglio.<br/>                                                                                                                                 |
| [**ReinstallaAgreementLicenseKeyPack**](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | Reinstalla un key pack Servizi Desktop remoto licenza acquistata tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del key pack.<br/>                                           |
| [**ReinstallLicenseKeyPackOffline**](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | Reinstalla un key pack Servizi Desktop remoto licenza che usa l'identificatore di licenza ricevuto tramite Internet o il telefono.<br/>                                                                                       |
| [**ReinstallaApriPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | Reinstalla un Key Pack Servizi Desktop remoto licenza Open License.<br/>                                                                                                                                                           |
| [**ReinstallRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | Reinstalla un key pack Servizi Desktop remoto licenza acquistata tramite un canale di vendita al dettaglio.<br/>                                                                                                                             |
| [**RemoveLicensesWithIdCount**](win32-tslicensekeypack-removelicenseswithidcount.md)                         | Rimuove il numero specificato di Servizi Desktop remoto licenze dal key pack specificato.<br/>                                                                                                                                  |
| [**UninstallLicenseKeyPack**](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | Disinstalla un key pack Servizi Desktop remoto licenza.<br/>                                                                                                                                                                         |
| [**UninstallLicenseKeyPackWithId**](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | Disinstalla il key pack Servizi Desktop remoto licenza con l'identificatore del key pack specificato.<br/>                                                                                                                                |



 

### <a name="properties"></a>Proprietà

La **classe Win32 \_ TSLicenseKeyPack** ha queste proprietà.

<dl> <dt>

**AccessRights**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**BitMap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("Sessione Desktop remoto", "Sessione VDI", "Calista", "Partner VDI")
</dt> </dl>

Qualificatore per i diritti di accesso del key pack per le licenze di Servizi terminal

</dd> <dt>

**AvailableLicenses**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di licenze disponibili nel key pack Servizi Desktop remoto licenza.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione del key pack Servizi Desktop remoto licenza.

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **[DATETIME](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data di scadenza del key pack Servizi Desktop remoto licenza.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di licenze rilasciate nel key pack Servizi Desktop remoto licenza.

</dd> <dt>

**KeyPackId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificatore del key pack Servizi Desktop remoto licenza.

</dd> <dt>

**KeyPackType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di key pack per il server Desktop remoto licenze.

| Valore | Descrizione |
|-------|-------------|
| 0 | Il tipo Servizi Desktop remoto key pack della licenza è sconosciuto. |
| 1 | Il tipo Servizi Desktop remoto key pack di licenza è un acquisto al dettaglio. |
| 2 | Il Servizi Desktop remoto di key pack per le licenze è un volume purchase. |
| 3 | Il Servizi Desktop remoto key pack di licenza è una licenza simultanea. |
| 4 | Il tipo Servizi Desktop remoto key pack della licenza è temporaneo. |
| 5 | Il Servizi Desktop remoto key pack di licenza è una licenza aperta. |
| 6 | Non supportata. |

**ProductType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di prodotto del key pack Servizi Desktop remoto licenza.

| Valore | Descrizione |
|-------|-------------|
| 0 | Il Servizi Desktop remoto di prodotto del key pack di licenza è per ogni dispositivo. Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve avere una licenza. |
| 1 | Il Servizi Desktop remoto del prodotto key pack di licenza è per utente. Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve avere una licenza. |
| 2 | Questo tipo di prodotto non è valido. |

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione del prodotto per il key pack Servizi Desktop remoto licenza.

| Valore | Descrizione |
|-------|-------------|
| "Windows Server 2012" | Solo i server che Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008 sono supportati con questa licenza. |
| "Windows Server 7" | Con questa licenza sono supportati solo i server che eseguono Windows Server 2008 R2 o Windows Server 2008. |
| "Windows Server 2008" | Solo i server che Windows Server 2008 sono supportati da questo Key Pack. |

**ProductVersionID**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore della versione del prodotto per il key pack Servizi Desktop remoto licenza.

| Valore | Descrizione |
|-------|-------------|
| 0 | Non supportato |
| 1 | Non supportato |
| 2 | Windows Server 2008 |
| 3 | Windows Server 2008 R2 |
| 4 | Windows Server 2012/Windows Server 2012 R2 |
| 5 | Windows Server 2016 |
| 6 | Windows Server 2019 |

**TotalLicenses**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di licenze nel key pack Servizi Desktop remoto licenza.

</dd> <dt>

**TypeAndModel**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatore per il tipo e il modello del key pack di licenze TS. Esempi: licenza di sottoscrizione VDI per dispositivo, licenza CAL per utente di Servizi terminal

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

[**Win32 \_ TSIssuedLicense**](win32-tsissuedlicense.md)
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

