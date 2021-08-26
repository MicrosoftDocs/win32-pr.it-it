---
title: MDM_DevDetail_Microsoft02 classe
description: La classe MDM \_ DevDetail \_ Microsoft02 gestisce l'oggetto di gestione che fornisce parametri specifici del dispositivo al server DM OMA.
ms.assetid: 22a8ba26-d215-4bc5-a51b-6933d5473da3
keywords:
- MDM_DevDetail_Microsoft02 classe
- MDM_DevDetail_Microsoft02 classe, descritta
topic_type:
- apiref
api_name:
- MDM_DevDetail_Microsoft02
- MDM_DevDetail_Microsoft02.InstanceID
- MDM_DevDetail_Microsoft02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc995d04452a49bfb6420d4b7e8424ab06b7f4023440568f841564fef532aa2f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053601"
---
# <a name="mdm_devdetail_microsoft02-class"></a>Classe \_ Mdm DevDetail \_ Microsoft02

\[Alcune informazioni riguardano prodotti pre-rilasciati che possono essere modificati in modo sostanziale prima che venga rilasciato commercialmente. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe MDM \_ DevDetail \_ Microsoft02** gestisce l'oggetto di gestione che fornisce parametri specifici del dispositivo al server DM OMA. Questi parametri del dispositivo non vengono inviati automaticamente dal client al server, ma possono essere sottoposti a query dai server usando i comandi DM OMA.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DevDetail_Microsoft02
{
  string InstanceID;
  string ParentID;
  string MobileID;
  string RadioSwV;
  string Resolution;
  string CommercializationOperator;
  sint32 ProcessorArchitecture;
  sint32 ProcessorType;
  string OSPlatform;
  string LocalTime;
  string DeviceName;
};
```

## <a name="members"></a>Members

La **classe MDM \_ DevDetail \_ Microsoft02** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM \_ DevDetail \_ Microsoft02** ha queste proprietà.

<dl> <dt>

[CommercializzazioneOperator](/windows/client-management/mdm/devdetail-csp#ext-microsoft-commercializationoperator)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[DeviceName](/windows/client-management/mdm/devdetail-csp#ext-microsoft-devicename)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifica il nome del nodo padre. Per questa classe, la stringa è "Microsoft"

</dd> <dt>

[LocalTime](/windows/client-management/mdm/devdetail-csp#ext-microsoft-localtime)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[MobileID](/windows/client-management/mdm/devdetail-csp#ext-microsoft-mobileid)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[OSPlatform](/windows/client-management/mdm/devdetail-csp#ext-microsoft-osplatform)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./DevDetail/Ext"

</dd> <dt>

[Processorarchitecture](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processorarchitecture)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[ProcessorType](/windows/client-management/mdm/devdetail-csp#ext-microsoft-processortype)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> <dt>

[RadioSwV](/windows/client-management/mdm/devdetail-csp#ext-microsoft-radioswv)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Restituisce il numero di versione del software dello stack di radio.

</dd> <dt>

[Risoluzione](/windows/client-management/mdm/devdetail-csp#ext-microsoft-resolution)
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                      |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di script di PowerShell con il provider bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

