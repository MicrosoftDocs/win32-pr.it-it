---
title: MDM_RemoteFind_Location01 classe
description: La classe MDM \_ RemoteFind \_ Location01 recupera le informazioni sulla posizione per un determinato dispositivo.
ms.assetid: 0c26bb3c-99b4-43ed-99ce-d976d48c4445
keywords:
- MDM_RemoteFind_Location01 classe
- MDM_RemoteFind_Location01 classe , descritta
topic_type:
- apiref
api_name:
- MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01.InstanceID
- MDM_RemoteFind_Location01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36942badfe975a28d5212e502ab28984fa745f4a7563c39ed1cebb7d1b5dbcef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077025"
---
# <a name="mdm_remotefind_location01-class"></a>Classe \_ MDM RemoteFind \_ Location01

\[Alcune informazioni riguardano un prodotto pre-rilasciato che può essere modificato sostanzialmente prima del rilascio in commercio. Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]

La **classe MDM \_ RemoteFind \_ Location01** recupera le informazioni sulla posizione per un determinato dispositivo.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind_Location01
{
  string   InstanceID;
  string   ParentID;
  real32   Latitude;
  real32   Longitude;
  real32   Altitude;
  sint32   Accuracy;
  sint32   AltitudeAccuracy;
  datetime Age;
};
```

## <a name="members"></a>Members

La **classe MDM \_ RemoteFind \_ Location01** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe MDM \_ RemoteFind \_ Location01** ha queste proprietà.

<dl> <dt>

[Precisione](/windows/client-management/mdm/remotefind-csp#accuracy)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[Age](/windows/client-management/mdm/remotefind-csp#age)
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[Altitudine](/windows/client-management/mdm/remotefind-csp#altitude)
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[AltitudineAccuracy](/windows/client-management/mdm/remotefind-csp#altitudeaccuracy)
</dt> <dd> <dl> <dt>

Tipo di dati: **sint32**
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

Identifica il nome del nodo padre. Per questa classe, la stringa è "Location".

</dd> <dt>

[Latitude](/windows/client-management/mdm/remotefind-csp#latitude)
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

[Longitudine](/windows/client-management/mdm/remotefind-csp#longitude)
</dt> <dd> <dl> <dt>

Tipo di dati: **real32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

</dd> <dt>

**Parentid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **key**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Descrive il percorso completo del nodo padre. Per questa classe, la stringa è "./Vendor/MSFT/RemoteFind"

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 10 solo app desktop\]<br/>                                                     |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                       |
| Spazio dei nomi<br/>                | Dmmap \\ mdm cimv2 \\ \\ radice<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso di script di PowerShell con il provider Bridge WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

