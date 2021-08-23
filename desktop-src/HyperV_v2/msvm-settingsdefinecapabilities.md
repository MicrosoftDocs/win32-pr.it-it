---
description: Fornisce un collegamento tra l'istanza delle funzionalità e le impostazioni minime, massime, incrementali e predefinite per una risorsa.
ms.assetid: 3B09ED8A-D4D0-41E2-B807-96AD8E990773
title: Msvm_SettingsDefineCapabilities classe
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
ms.openlocfilehash: 7194632af7bc1154e6a9bbca1dd5ef0bcca0fb46ab13693d20160ea404068adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950465"
---
# <a name="msvm_settingsdefinecapabilities-class"></a>Classe Msvm \_ SettingsDefineCapabilities

Fornisce un collegamento tra l'istanza delle funzionalità e le impostazioni minime, massime, incrementali e predefinite per una risorsa.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe Msvm \_ SettingsDefineCapabilities** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ SettingsDefineCapabilities** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **funzionalità \_ CIM**](/previous-versions//cc136806(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Istanza delle funzionalità. Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities.**](/previous-versions//cc136913(v=vs.85))

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Impostazione utilizzata per definire l'istanza di funzionalità associata. Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities.**](/previous-versions//cc136913(v=vs.85))

</dd> <dt>

**PropertyPolicy**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se le proprietà non null non chiave dell'istanza dei dati dell'impostazione associata vengono considerate in modo indipendente o come set correlato. Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities**](/previous-versions//cc136913(v=vs.85)) ed è sempre impostata su 0 (indipendente).

</dd> <dt>

**SupportStatement**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identifica l'istruzione di supporto.

> [!Note]  
> Questa proprietà è stata aggiunta Windows 10 versione 1703.

 

<dt>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>

<span id="Production"></span><span id="production"></span><span id="PRODUCTION"></span>**Produzione** (0)


</dt> <dd></dd> <dt>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>

<span id="Prerelease"></span><span id="prerelease"></span><span id="PRERELEASE"></span>**Versione preliminare** (1)


</dt> <dd>

> [!Note]  
> Was **NonProduction** in Windows 10, version 1703.

 

</dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>**Riservato** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ValueRange**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualsiasi ulteriore semantica sull'interpretazione di tutte le proprietà non null e non chiave dei dati dell'impostazione. Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities.**](/previous-versions//cc136913(v=vs.85))

</dd> <dt>

**Ruolo valore**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Qualsiasi ulteriore semantica sull'interpretazione delle proprietà non null e non chiave dei dati dell'impostazione. Questa proprietà viene ereditata da [**CIM \_ SettingsDefineCapabilities.**](/previous-versions//cc136913(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori per le **proprietà ValueRole** **e ValueRange** vengono usati nelle coppie seguenti:

-   Point/Default (0/0)
-   Valori minimi/supportati (1/3)
-   Valori massimi/supportati (2/3)
-   Incrementi/supportati (3/3).

"Punto" indica che ognuna delle proprietà nell'oggetto **PartComponent** rappresenta l'impostazione predefinita della piattaforma.

"Minimums" e "Maximums" significano che ognuna delle proprietà nell'oggetto **PartComponent** rappresenta i valori più piccoli e più grandi possibili per queste proprietà supportate dalla piattaforma in base alla configurazione corrente del computer.

"Incrementi" indica la granularità con cui è possibile aumentare o ridurre le impostazioni.

L'accesso alla **classe Msvm \_ SettingsDefineCapabilities** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Impostazioni \_ CIMDefineCapabilities**](cim-settingsdefinecapabilities.md)
</dt> <dt>

[**Impostazioni \_ CIMDefineCapabilities**](/previous-versions//cc136913(v=vs.85))
</dt> <dt>

[**Impostazioni \_ msvmDefineCapabilities (V1)**](/previous-versions/windows/desktop/virtual/msvm-settingsdefinecapabilities)
</dt> <dt>

[Classi di gestione delle risorse](resource-management-classes.md)
</dt> </dl>

 

