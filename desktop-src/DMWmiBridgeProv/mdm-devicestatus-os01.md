---
title: MDM_DeviceStatus_OS01 classe
description: La classe \_ MDM DeviceStatus OS01 viene usata dall'azienda per eseguire query sul sistema operativo nei dispositivi \_ con i criteri aziendali.
ms.assetid: 887dc453-f6b5-4f09-8ce1-b87f71dd8396
keywords:
- MDM_DeviceStatus_OS01 classe
- MDM_DeviceStatus_OS01 classe , descritta
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_OS01
- MDM_DeviceStatus_OS01.InstanceID
- MDM_DeviceStatus_OS01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae98ed55f2fb4b5177b2596b99bb03ba8bdd6e74e3ba4e1c0e028928fdc0acb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118165844"
---
# <a name="mdm_devicestatus_os01-class"></a>Classe \_ \_ OS01 DeviceStatus MDM

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe \_ MDM DeviceStatus \_ OS01** viene usata dall'azienda per eseguire query sul sistema operativo nei dispositivi con i criteri aziendali.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_OS01
{
  string InstanceID;
  string ParentID;
  string Edition;
};
```

## <a name="members"></a>Members

La **classe \_ MDM DeviceStatus \_ OS01** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ MDM DeviceStatus \_ OS01** ha queste proprietà.

<dl> <dt>

[Edizione](/windows/client-management/mdm/devicestatus-csp#devicestatus-os-edition)
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nodo per la query del sistema operativo.

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/DeviceStatus"

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

