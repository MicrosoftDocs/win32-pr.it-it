---
description: Descrive un set di classi con proprietà e metodi obbligatori, necessari per gestire un'entità reale o per supportare uno scenario di utilizzo, in modo interoperabile.
ms.assetid: 75644856-3B47-43B8-835C-783A6BEE7251
title: Msvm_RegisteredProfile classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredProfile
- Msvm_RegisteredProfile.InstanceID
- Msvm_RegisteredProfile.Caption
- Msvm_RegisteredProfile.Description
- Msvm_RegisteredProfile.ElementName
- Msvm_RegisteredProfile.RegisteredOrganization
- Msvm_RegisteredProfile.OtherRegisteredOrganization
- Msvm_RegisteredProfile.RegisteredName
- Msvm_RegisteredProfile.RegisteredVersion
- Msvm_RegisteredProfile.AdvertiseTypes
- Msvm_RegisteredProfile.AdvertiseTypeDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0773ad1b7c992211e8bc578ac2cf2bea7706313918581ef2da9df8e2887b536d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535771"
---
# <a name="msvm_registeredprofile-class"></a>Classe Msvm \_ RegisteredProfile

Descrive un set di classi con proprietà e metodi obbligatori, necessari per gestire un'entità reale o per supportare uno scenario di utilizzo, in modo interoperabile.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Msvm_RegisteredProfile : CIM_RegisteredProfile
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 RegisteredOrganization;
  string OtherRegisteredOrganization;
  string RegisteredName;
  string RegisteredVersion;
  uint16 AdvertiseTypes[];
  string AdvertiseTypeDescriptions[];
};
```

## <a name="members"></a>Members

La **classe Msvm \_ RegisteredProfile** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ RegisteredProfile** ha queste proprietà.

<dl> <dt>

**AdvertiseTypeDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe che fornisce informazioni aggiuntive correlate alla **proprietà AdvertiseType.** È necessario specificare una descrizione quando **AdvertiseType** è 1 (Altro). Una voce in questa matrice corrisponde allo stesso indice nella **matrice AdvertiseTypes.** Questa proprietà viene ereditata da [**CIM \_ RegisteredProfile.**](/previous-versions//ee309375(v=vs.85))

</dd> <dt>

**AdvertiseTypes**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica l'annuncio per le informazioni sul profilo. Viene usato dai servizi pubblicitari dell'infrastruttura WBEM per determinare gli elementi da annunciare tramite i meccanismi. La proprietà è una matrice in modo che il profilo possa essere annunciato usando diversi meccanismi. Se questa proprietà è **Null,** equivale a specificare il valore 2 (Non annunciato). Questa proprietà viene ereditata da [**CIM \_ RegisteredProfile.**](/previous-versions//ee309375(v=vs.85))

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Non annunciato** (2)
</dt> <dt>

<span id="SLP_"></span><span id="slp_"></span>**SLP** (3 )
</dt> </dl>

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**, **override**
</dt> </dl>

Stringa che identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**OtherRegisteredOrganization**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** ( 256 )
</dt> </dl>

Stringa che fornisce una descrizione dell'organizzazione quando **RegisteredOrganization** contiene 1 (Altro). Questa proprietà viene ereditata da [**CIM \_ RegisteredProfile.**](/previous-versions//ee309375(v=vs.85))

</dd> <dt>

**RegisteredName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **MaxLen** ( 256 )
</dt> </dl>

Nome del profilo registrato. Poiché possono esistere più versioni per lo stesso **RegisteredName,** la combinazione di **RegisteredName**, **RegisteredOrganization** e **RegisteredVersion** deve identificare in modo univoco il profilo registrato nell'ambito dell'organizzazione. Questa proprietà viene ereditata da [**CIM \_ RegisteredProfile.**](/previous-versions//ee309375(v=vs.85))

</dd> <dt>

**Registeredorganization**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Organizzazione che definisce questo profilo. Questa proprietà viene ereditata da [**CIM \_ RegisteredProfile.**](/previous-versions//ee309375(v=vs.85))

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)
</dt> <dt>

<span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)
</dt> <dt>

<span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)
</dt> <dt>

<span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consortium for Service Innovation** (4)
</dt> <dt>

<span id="FAST"></span><span id="fast"></span>**FAST** (5)
</dt> <dt>

<span id="GGF"></span><span id="ggf"></span>**GGF** (6)
</dt> <dt>

<span id="INTAP"></span><span id="intap"></span>**INTAP** (7)
</dt> <dt>

<span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)
</dt> <dt>

<span id="NAC"></span><span id="nac"></span>**NAC** (9)
</dt> <dt>

<span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**//10 Northwest Energy Efficiency Alliance** (10)
</dt> <dt>

<span id="SNIA"></span><span id="snia"></span>**SNIA** (11)
</dt> <dt>

<span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**Forum TM** (12)
</dt> <dt>

<span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**The Open Group** (13)
</dt> <dt>

<span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)
</dt> <dt>

<span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)
</dt> <dt>

<span id="IETF"></span><span id="ietf"></span>**IETF** (16)
</dt> <dt>

<span id="INCITS"></span><span id="incits"></span>**INCITS** (17)
</dt> <dt>

<span id="ISO"></span><span id="iso"></span>**ISO** (18)
</dt> <dt>

<span id="W3C"></span><span id="w3c"></span>**W3C** (19)
</dt> <dt>

<span id="__20___________OGF"></span><span id="__20___________ogf"></span>**//20 OGF** (20)
</dt> <dt>

<span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**Griglia verde** (21)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DmTF Reserved** (.. )
</dt> </dl>

</dd> <dt>

**Versione registrata**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Versione di questo profilo. La stringa deve essere nel formato: "*M*. *N*. *U*" Where:

-   *M* è la versione principale (in formato numerico) che descrive la creazione o l'ultima modifica del profilo.
-   *N* è la versione secondaria (in formato numerico) che descrive la creazione o l'ultima modifica del profilo.
-   *U* è l'aggiornamento (in formato numerico) che descrive la creazione o l'ultima modifica del profilo.

Questa proprietà viene ereditata da [**CIM \_ RegisteredProfile.**](/previous-versions//ee309375(v=vs.85))

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8.1 solo app desktop\]<br/>                                                            |
| Server minimo supportato<br/> | Windows Server 2012 Solo \[ app desktop R2\]<br/>                                                 |
| Spazio dei nomi<br/>                | Interoperabilità \\ radice<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

