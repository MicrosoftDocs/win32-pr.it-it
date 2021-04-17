---
title: Classe Win32_TSLicenseKeyPack
description: Fornisce metodi e proprietà per la visualizzazione e l'installazione di Servizi Desktop remoto key pack per le licenze.
ms.assetid: 27450646-c51f-4911-bb42-410794e32003
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto
- Classe Win32_TSLicenseKeyPack Servizi Desktop remoto, descritta
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
ms.openlocfilehash: 9d78af398ebf7c137be5b31c9db427691a66a7a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517403"
---
# <a name="win32_tslicensekeypack-class"></a>Win32 \_ TSLicenseKeyPack (classe)

Fornisce metodi e proprietà per la visualizzazione e l'installazione di Servizi Desktop remoto key pack per le licenze.

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

La classe **Win32 \_ TSLicenseKeyPack** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSLicenseKeyPack** presenta questi metodi.



| Metodo                                                                                                        | Descrizione                                                                                                                                                                                                                               |
|:--------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ConvertLicenses**](convertlicenses-win32-tslicensekeypack.md)                                             | Converte le licenze nel Key Pack corrente.<br/>                                                                                                                                                                                 |
| [**ImportAgreementLicenseKeyPack**](win32-tslicensekeypack-importagreementlicensekeypack.md)                 | Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.<br/> |
| [**ImportLicenseKeyPackOffline**](win32-tslicensekeypack-importlicensekeypackoffline.md)                     | Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License che usa un identificatore di licenza ricevuto tramite Internet o il telefono.<br/>                                               |
| [**ImportOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-importopenpurchaselicensekeypack.md)           | Importazioni, da un altro Desktop remoto server licenze, un Key Pack per licenze Open License Servizi Desktop remoto.<br/>                                                                                                                 |
| [**ImportRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-importretailpurchaselicensekeypack.md)       | Importa, da un altro Desktop remoto server licenze, un Key Pack di Servizi Desktop remoto License acquistato tramite un canale di vendita al dettaglio.<br/>                                                                                   |
| [**InstallAgreementLicenseKeyPack**](installagreementlicensekeypack-win32-tslicensekeypack.md)               | Installa un Key Pack di licenza Servizi Desktop remoto acquistato tramite una licenza per il contratto.<br/>                                                                                                                           |
| [**InstallLicenseKeyPack**](installlicensekeypack-win32-tslicensekeypack.md)                                 | Installa un Key Pack per le licenze Servizi Desktop remoto che usa un ID del Key Pack per le licenze ricevuto tramite Internet o il telefono.<br/>                                                                                          |
| [**InstallOpenLicenseKeyPack**](installopenlicensekeypack-win32-tslicensekeypack.md)                         | Installa un Key Pack di licenza Servizi Desktop remoto acquistato tramite un contratto di licenza Open.<br/>                                                                                                                      |
| [**InstallRetailPurchaseLicenseKeyPack**](installretailpurchaselicensekeypack-win32-tslicensekeypack.md)     | Installa un Key Pack di licenza Servizi Desktop remoto acquistato tramite un negozio al dettaglio.<br/>                                                                                                                                 |
| [**ReinstallAgreementLicenseKeyPack**](win32-tslicensekeypack-reinstallagreementlicensekeypack.md)           | Reinstalla un Key Pack di Servizi Desktop remoto License acquistato tramite un contratto di licenza e si connette automaticamente tramite Internet per convalidare la licenza del Key Pack.<br/>                                           |
| [**ReinstallLicenseKeyPackOffline**](win32-tslicensekeypack-reinstalllicensekeypackoffline.md)               | Reinstalla un Key Pack di Servizi Desktop remoto License che utilizza l'identificatore di licenza ricevuto tramite Internet o il telefono.<br/>                                                                                       |
| [**ReinstallOpenPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallopenpurchaselicensekeypack.md)     | Reinstalla un Key Pack per licenze Open License Servizi Desktop remoto.<br/>                                                                                                                                                           |
| [**ReinstallRetailPurchaseLicenseKeyPack**](win32-tslicensekeypack-reinstallretailpurchaselicensekeypack.md) | Reinstalla un Key Pack di Servizi Desktop remoto License acquistato tramite un canale di vendita al dettaglio.<br/>                                                                                                                             |
| [**RemoveLicensesWithIdCount**](win32-tslicensekeypack-removelicenseswithidcount.md)                         | Rimuove il numero specificato di Servizi Desktop remoto licenze dal Key Pack specificato.<br/>                                                                                                                                  |
| [**UninstallLicenseKeyPack**](win32-tslicensekeypack-uninstalllicensekeypack.md)                             | Disinstalla un Key Pack per le licenze Servizi Desktop remoto.<br/>                                                                                                                                                                         |
| [**UninstallLicenseKeyPackWithId**](win32-tslicensekeypack-uninstalllicensekeypackwithid.md)                 | Disinstalla il Key Pack di Servizi Desktop remoto License con l'identificatore del Key Pack specificato.<br/>                                                                                                                                |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSLicenseKeyPack** dispone di queste proprietà.

<dl> <dt>

**AccessRights**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**bitmap**](/windows/desktop/WmiSdk/standard-qualifiers) ("0", "1", "2", "3"), [**BitValues**](/windows/desktop/WmiSdk/standard-qualifiers) ("sessione Desktop remoto", "VDI Session", "Calista", "VDI Partners")
</dt> </dl>

Qualificatore per i diritti di accesso del key pack licenze Servizi terminal

</dd> <dt>

**AvailableLicenses**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di licenze disponibili nel Key Pack di Servizi Desktop remoto License.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione del Key Pack di Servizi Desktop remoto License.

</dd> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **[DateTime](/windows/desktop/WmiSdk/datetime)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Data di scadenza del Key Pack di Servizi Desktop remoto License.

</dd> <dt>

**IssuedLicenses**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di licenze rilasciate nel Key Pack di Servizi Desktop remoto License.

</dd> <dt>

**KeyPackId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificatore per il Key Pack di Servizi Desktop remoto License.

</dd> <dt>

**KeyPackType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di Key Pack per il server licenze Desktop remoto.

| Valore | Descrizione |
|-------|-------------|
| 0 | Il tipo di Key Pack del Servizi Desktop remoto License è sconosciuto. |
| 1 | Il tipo di Key Pack per le licenze Servizi Desktop remoto è un acquisto al dettaglio. |
| 2 | Il tipo di Key Pack del Servizi Desktop remoto License è un Volume Purchase. |
| 3 | Il tipo di Key Pack del Servizi Desktop remoto License è una licenza simultanea. |
| 4 | Il tipo di Key Pack del Servizi Desktop remoto License è temporaneo. |
| 5 | Il tipo di Key Pack del Servizi Desktop remoto License è una licenza Open. |
| 6 | Non supportata. |

**ProductType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di prodotto del Key Pack di Servizi Desktop remoto License.

| Valore | Descrizione |
|-------|-------------|
| 0 | Il tipo di prodotto Servizi Desktop remoto License Key Pack è per dispositivo. Pertanto, ogni dispositivo che si connette al server Host sessione Desktop remoto deve disporre di una licenza. |
| 1 | Il tipo di prodotto Servizi Desktop remoto License Key Pack è per utente. Pertanto, ogni utente che si connette al server Host sessione Desktop remoto deve disporre di una licenza. |
| 2 | Questo tipo di prodotto non è valido. |

**ProductVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione del prodotto per il Key Pack di Servizi Desktop remoto License.

| Valore | Descrizione |
|-------|-------------|
| "Windows Server 2012" | Con questa licenza sono supportati solo i server che eseguono Windows Server 2012, Windows Server 2008 R2 o Windows Server 2008. |
| "Windows Server 7" | Con questa licenza sono supportati solo i server che eseguono Windows Server 2008 R2 o Windows Server 2008. |
| "Windows Server 2008" | Questo Key Pack supporta solo i server che eseguono Windows Server 2008. |

**ProductVersionID**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore della versione del prodotto per il Key Pack di Servizi Desktop remoto License.

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

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero totale di licenze nel Key Pack di Servizi Desktop remoto License.

</dd> <dt>

**TypeAndModel**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualificatore per il tipo e il modello del Key Pack per licenze Servizi terminal. Esempi: licenza di sottoscrizione per ogni dispositivo di VDI, licenza CAL per utente di Servizi terminal

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

[**\_TSIssuedLicense Win32**](win32-tsissuedlicense.md)
</dt> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseReportEntry Win32**](win32-tslicensereportentry.md)
</dt> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

