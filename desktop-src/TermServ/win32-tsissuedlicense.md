---
title: Classe Win32_TSIssuedLicense
description: Descrive le istanze di Servizi Desktop remoto licenze di accesso client per dispositivo (RDS \ 160; Licenze CAL per dispositivo rilasciate da un server licenze Desktop remoto.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSIssuedLicense Servizi Desktop remoto
- Classe Win32_TSIssuedLicense Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSIssuedLicense
- Win32_TSIssuedLicense.LicenseId
- Win32_TSIssuedLicense.KeyPackId
- Win32_TSIssuedLicense.sIssuedToUser
- Win32_TSIssuedLicense.sIssuedToComputer
- Win32_TSIssuedLicense.LicenseStatus
- Win32_TSIssuedLicense.IssueDate
- Win32_TSIssuedLicense.ExpirationDate
- Win32_TSIssuedLicense.sHardwareId
api_location:
- TlsWmiProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d08a68ddcc15a912de4c674403928211a297e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301740"
---
# <a name="win32_tsissuedlicense-class"></a>Win32 \_ TSIssuedLicense (classe)

Vengono descritte le istanze delle licenze CAL per dispositivo Servizi Desktop remoto per dispositivo che vengono rilasciate da un server licenze Desktop remoto.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_TERMSERVLICENSING_Prov"), AMENDMENT]
class Win32_TSIssuedLicense
{
  uint32   LicenseId;
  uint32   KeyPackId;
  string   sIssuedToUser;
  string   sIssuedToComputer;
  uint32   LicenseStatus;
  DATETIME IssueDate;
  DATETIME ExpirationDate;
  string   sHardwareId;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSIssuedLicense** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ TSIssuedLicense** presenta questi metodi.



| Metodo                                         | Descrizione                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Revoke**](revoke-win32-tsissuedlicense.md) | Revoca le licenze CAL per dispositivo di Servizi Desktop remoto rappresentate dall'oggetto **Win32 \_ TSIssuedLicense** .<br/> |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSIssuedLicense** dispone di queste proprietà.

<dl> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica la data di scadenza della licenza.

</dd> <dt>

**IssueDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica la data di rilascio della licenza.

</dd> <dt>

**KeyPackId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il Key Pack di Servizi Desktop remoto License.

</dd> <dt>

**LicenseId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificatore univoco per questa licenza.

</dd> <dt>

**LicenseStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato della licenza.

<dt>

0
</dt> <dd>

Lo stato della licenza è sconosciuto.

</dd> <dt>

1
</dt> <dd>

La licenza è una licenza temporanea.

</dd> <dt>

2
</dt> <dd>

La licenza è attiva.

</dd> <dt>

3
</dt> <dd>

La licenza è una licenza per l'aggiornamento.

</dd> <dt>

4
</dt> <dd>

La licenza è stata revocata.

</dd> <dt>

5
</dt> <dd>

Lo stato della licenza è in sospeso.

</dd> <dt>

6
</dt> <dd>

La licenza è una licenza simultanea.

</dd> </dl>

</dd> <dt>

**sHardwareId**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore hardware per il quale è stata emessa la licenza.

</dd> <dt>

**sIssuedToComputer**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer per cui è stata emessa la licenza.

</dd> <dt>

**sIssuedToUser**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome utente per cui è stata emessa la licenza.

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

[**\_TSLicenseKeyPack Win32**](win32-tslicensekeypack.md)
</dt> <dt>

[**\_TSLicenseReport Win32**](win32-tslicensereport.md)
</dt> <dt>

[**\_TSLicenseReportEntry Win32**](win32-tslicensereportentry.md)
</dt> <dt>

[**\_TSLicenseServer Win32**](win32-tslicenseserver.md)
</dt> </dl>

 

