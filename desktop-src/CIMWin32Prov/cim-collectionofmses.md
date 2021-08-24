---
description: L'oggetto CIM CollectionOfMSEs consente il raggruppamento di oggetti CIM ManagedSystemElement allo scopo di \_ \_ associare impostazioni e configurazioni. È astratto richiedere ulteriori definizioni e perfezionamento semantico nelle sottoclassi.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: CIM_CollectionOfMSEs classe (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d67b51e90a9a3c2eff420a5251c1b4e75f323d48e796a3190b662fb844c1517a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579051"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a>CIM_CollectionOfMSEs classe (provider WMI CIMWin32)

**L'oggetto CIM \_ CollectionOfMSEs** consente il raggruppamento di [**oggetti CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) allo scopo di associare impostazioni e configurazioni. È astratto richiedere ulteriori definizioni e perfezionamento semantico nelle sottoclassi.

**L'oggetto CIM \_ CollectionOfMSEs** non contiene informazioni sullo stato o sullo stato, ma rappresenta solo un raggruppamento di elementi. Per questo motivo, non è corretto per i gruppi di sottoclassi con stato/stato da **CIM \_ CollectionOfMSEs**, Un esempio è [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) (che è correttamente sottoclassato da [**CIM \_ LogicalElement).**](cim-logicalelement.md) Le raccolte aggregano in genere gli oggetti "like" e rappresentano un'ottimizzazione. Senza raccolte, è necessario definire singole associazioni [**CiM \_ ElementSetting**](cim-elementsetting.md) ed [**\_ ElementConfiguration CIM**](cim-elementconfiguration.md) per associare le impostazioni e gli oggetti di configurazione ai singoli [**elementi CIM \_ ManagedSystemElements.**](cim-managedsystemelement.md) Potrebbe esserci una grande duplicazione nell'assegnazione della stessa impostazione a più oggetti. Inoltre, l'uso dell'oggetto raccolta consente di determinato che le associazioni di impostazione e configurazione sono effettivamente le stesse per i membri della raccolta. Queste informazioni verrebbero altrimenti ottenute definendo la raccolta in modo proprietario e quindi query sulle associazioni **CIM \_ ElementSetting** e **CIM \_ ElementConfiguration** per determinare se il set di raccolta è completamente coperto.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a>Members

La **classe CIM \_ CollectionOfMSEs** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ CollectionOfMSEs** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione testuale dell'oggetto CollectionOfMSEs.

</dd> <dt>

**CollectionID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Identificazione dell'oggetto Collection. In caso di sottoclasse, la proprietà CollectionID può essere sottoposta a override come proprietà Key.

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto CollectionOfMSEs.

</dd> </dl>

## <a name="remarks"></a>Commenti

WMI non implementa questa classe. Vedere [Classi Win32 per](win32-provider.md) le classi WMI derivate da **CIM \_ CollectionOfMSEs**.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




