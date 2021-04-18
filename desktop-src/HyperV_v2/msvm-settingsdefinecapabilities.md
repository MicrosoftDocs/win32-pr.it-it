---
description: Fornisce un collegamento tra l'istanza di funzionalità e le impostazioni minime, massime, incrementali e predefinite per una risorsa.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Classe Msvm_SettingsDefineCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingsDefineCapabilities
- Msvm_SettingsDefineCapabilities.SupportStatement
- Msvm_SettingsDefineCapabilities.GroupComponent
- Msvm_SettingsDefineCapabilities.PartComponent
- Msvm_SettingsDefineCapabilities.PropertyPolicy
- Msvm_SettingsDefineCapabilities.ValueRole
- Msvm_SettingsDefineCapabilities.ValueRange
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7a312d3453b783c3d72f909ec6cb0b37d83feb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308206"
---
# <a name="msvm_settingsdefinecapabilities-class"></a>\_Classe MSVM SettingsDefineCapabilities

Fornisce un collegamento tra l'istanza di funzionalità e le impostazioni minime, massime, incrementali e predefinite per una risorsa.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingsDefineCapabilities : CIM_SettingsDefineCapabilities
{
  uint16               SupportStatement;
  CIM_Capabilities REF GroupComponent;
  CIM_SettingData  REF PartComponent;
  uint16               PropertyPolicy = 0;
  uint16               ValueRole = 3;
  uint16               ValueRange = 0;
};
```

## <a name="members"></a>Members

La **classe \_ SettingsDefineCapabilities di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ SettingsDefineCapabilities di MSVM** dispone di queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ funzionalità CIM**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Istanza delle funzionalità. Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Impostazione utilizzata per definire l'istanza delle funzionalità associate. Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se le proprietà non null e non chiave dell'istanza dei dati di impostazione associata vengono gestite in modo indipendente o come set correlato. Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) ed è sempre impostata su 0 (Independent).

</dd> <dt>

**SupportStatement**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica l'istruzione di supporto.

> [!Note]  
> Questa proprietà è stata aggiunta in Windows 10, versione 1703.

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Produzione** (0)


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Versione preliminare** (1)


</dt> <dd>

> [!Note]  
> Non è **prodotto** in Windows 10, versione 1703.

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualsiasi altra semantica sull'interpretazione di tutte le proprietà non null e non chiave dei dati dell'impostazione. Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).

</dd> <dt>

**ValueRole**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualsiasi altra semantica sull'interpretazione delle proprietà non null e non chiave dei dati dell'impostazione. Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori per le proprietà **ValueRole** e **ValueRange** vengono usati nelle coppie seguenti:

-   Punto/predefinito (0/0)
-   Minima/supportata (1/3)
-   Massimo/supportato (2/3)
-   Incrementi/supportati (3/3).

"Point" indica che ognuna delle proprietà dell'oggetto **PartComponent** rappresenta l'impostazione predefinita della piattaforma.

"Minimums" e "Maximers" indicano che ognuna delle proprietà nell'oggetto **PartComponent** rappresenta i valori più piccoli e massimi possibili per queste proprietà supportate dalla piattaforma in base alla configurazione del computer corrente.

"Incrementi" indica la granularità in cui è possibile aumentare o diminuire le impostazioni.

L'accesso alla **classe \_ SettingsDefineCapabilities di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SETTINGSDEFINECAPABILITIES CIM**](cim-settingsdefinecapabilities.md)
</dt> <dt>

[**\_SETTINGSDEFINECAPABILITIES CIM**](/previous-versions//cc136913(v=vs.85))
</dt> <dt>

[**MSVM \_ SettingsDefineCapabilities (V1)**](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[Classi di gestione delle risorse](resource-management-classes.md)
</dt> </dl>

 

