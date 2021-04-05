---
title: Classe MDM_DeviceStatus_TPM01
description: La \_ classe MDM DeviceStatus \_ TPM01 viene usata dall'azienda per eseguire una query sulla versione TPM dei dispositivi con i criteri aziendali.
ms.assetid: 9df10fbe-91b7-49f4-9e27-6c42218a6718
keywords:
- Classe MDM_DeviceStatus_TPM01
- Classe MDM_DeviceStatus_TPM01, descritta
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_TPM01
- MDM_DeviceStatus_TPM01.InstanceID
- MDM_DeviceStatus_TPM01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a7231e3801867ec7722afe40aae44b1b541a545
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874189"
---
# <a name="mdm_devicestatus_tpm01-class"></a>\_Classe MDM DeviceStatus \_ TPM01

\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La classe **MDM \_ DeviceStatus \_ TPM01** viene usata dall'azienda per eseguire una query sulla versione TPM dei dispositivi con i criteri aziendali.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_TPM01
{
  string InstanceID;
  string ParentID;
  string SpecificationVersion;
};
```

## <a name="members"></a>Members

La classe **MDM \_ DeviceStatus \_ TPM01** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **MDM \_ DeviceStatus \_ TPM01** dispone di queste proprietà.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nodo per la query TPM.

</dd> <dt>

**ParentID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe la stringa è "./Vendor/MSFT/DeviceStatus"

</dd> <dt>

[SpecificationVersion](/windows/client-management/mdm/devicestatus-csp#devicestatus-tpm-specificationversion)
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows 10\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | \\ \\ Dmmap MDM CIMV2 \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

