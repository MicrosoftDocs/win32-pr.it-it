---
title: Win32_TSIssuedLicense classe
description: Descrive le istanze di Servizi Desktop remoto licenze di accesso client per dispositivo (Servizi Desktop remoto \ 160; Licenze CAL per dispositivo) rilasciate da un server Desktop remoto licenze.
ms.assetid: 15825dc5-9ada-4c11-ac77-beb681e9b33c
ms.tgt_platform: multiple
keywords:
- Win32_TSIssuedLicense classe Servizi Desktop remoto
- Win32_TSIssuedLicense classe Servizi Desktop remoto , descritto
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
ms.openlocfilehash: b76127d41c6a571b6bc75bc74378b21f76f4b38c05f0a223d36e979dccf89a4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656161"
---
# <a name="win32_tsissuedlicense-class"></a>Classe \_ TSIssuedLicense Win32

Vengono descritte le istanze Servizi Desktop remoto licenze CAL Per Dispositivo rilasciate da un server licenze Desktop remoto per dispositivo.

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

La **classe Win32 \_ TSIssuedLicense** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Win32 \_ TSIssuedLicense** dispone di questi metodi.



| Metodo                                         | Descrizione                                                                                               |
|:-----------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [**Revocare**](revoke-win32-tsissuedlicense.md) | Revoca le licenze CAL Per Dispositivo di Servizi Desktop remoto rappresentate dall'oggetto **\_ TSIssuedLicense Win32.**<br/> |



 

### <a name="properties"></a>Proprietà

La **classe Win32 \_ TSIssuedLicense** ha queste proprietà.

<dl> <dt>

**ExpirationDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DATETIME**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica la data di scadenza della licenza.

</dd> <dt>

**IssueDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DATETIME**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica la data di emissione della licenza.

</dd> <dt>

**KeyPackId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il key pack Servizi Desktop remoto licenza.

</dd> <dt>

**LicenseId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificatore univoco per questa licenza.

</dd> <dt>

**LicenseStatus**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
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

La licenza è una licenza di aggiornamento.

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

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificatore hardware per cui è stata rilasciata la licenza.

</dd> <dt>

**sIssuedToComputer**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome computer per cui è stata rilasciata la licenza.

</dd> <dt>

**sIssuedToUser**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome utente per cui è stata rilasciata la licenza.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare questa classe, è necessario essere membri del gruppo Administrators.

Managed Object Format (MOF) contengono le definizioni per le classi WMI (Windows Management Instrumentation). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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
</dt> <dt>

[**Win32 \_ TSLicenseReport**](win32-tslicensereport.md)
</dt> <dt>

[**Win32 \_ TSLicenseReportEntry**](win32-tslicensereportentry.md)
</dt> <dt>

[**Win32 \_ TSLicenseServer**](win32-tslicenseserver.md)
</dt> </dl>

 

