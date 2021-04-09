---
title: Classe MDM_BitLocker
description: La \_ classe BITLOCKER MDM viene usata dall'azienda per gestire la crittografia di PC e dispositivi.
ms.assetid: e8bea6dc-8d3d-46d2-b2e3-9a4c547a639f
keywords:
- Classe MDM_BitLocker
- Classe MDM_BitLocker, descritta
topic_type:
- apiref
api_name:
- MDM_BitLocker
- MDM_BitLocker.InstanceID
- MDM_BitLocker.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b94db491333cada64b6287dc87ec233b420bf0f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121410"
---
# <a name="mdm_bitlocker-class"></a>\_Classe BITLOCKER MDM

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La \_ classe BITLOCKER MDM viene usata dall'azienda per gestire la crittografia di PC e dispositivi.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_BitLocker
{
  string InstanceID;
  string ParentID;
  sint32 RequireStorageCardEncryption;
  sint32 RequireDeviceEncryption;
  string EncryptionMethodByDriveType;
  string SystemDrivesRequireStartupAuthentication;
  string SystemDrivesMinimumPINLength;
  string SystemDrivesRecoveryMessage;
  string SystemDrivesRecoveryOptions;
  string FixedDrivesRecoveryOptions;
  string FixedDrivesRequireEncryption;
  string RemovableDrivesRequireEncryption;
  sint32 AllowWarningForOtherDiskEncryption;
};
```

## <a name="members"></a>Members

La **classe \_ BitLocker di MDM** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ BitLocker di MDM** presenta queste proprietà.

<dl> <dt>

[AllowWarningForOtherDiskEncryption](/windows/client-management/mdm/bitlocker-csp#allowwarningforotherdiskencryption)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[EncryptionMethodByDriveType](/windows/client-management/mdm/bitlocker-csp#encryptionmethodbydrivetype)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[FixedDrivesRecoveryOptions](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[FixedDrivesRequireEncryption](/windows/client-management/mdm/bitlocker-csp#fixeddrivesrequireencryption)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

</dd> <dt>

[RemovableDrivesRequireEncryption](/windows/client-management/mdm/bitlocker-csp#removabledrivesrequireencryption)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[RequireDeviceEncryption](/windows/client-management/mdm/bitlocker-csp#requiredeviceencryption)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[RequireStorageCardEncryption](/windows/client-management/mdm/bitlocker-csp#requirestoragecardencryption)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[SystemDrivesMinimumPINLength](/windows/client-management/mdm/bitlocker-csp#systemdrivesminimumpinlength)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[SystemDrivesRecoveryMessage](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoverymessage)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[SystemDrivesRecoveryOptions](/windows/client-management/mdm/bitlocker-csp#systemdrivesrecoveryoptions)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> <dt>

[SystemDrivesRequireStartupAuthentication](/windows/client-management/mdm/bitlocker-csp#systemdrivesrequirestartupauthentication)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                     |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                       |
| Spazio dei nomi<br/>                | \\ \\ Dmmap MDM CIMV2 \\ radice<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 

