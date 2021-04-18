---
description: Rappresenta un elemento logico che contiene informazioni per rappresentare e gestire la funzionalità fornita da una funzionalità del dispositivo o software.
ms.assetid: 0b2312da-433b-43d8-8d21-babab12a5b2c
title: Classe CIM_Service (gestione Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service
- CIM_Service.SystemCreationClassName
- CIM_Service.SystemName
- CIM_Service.CreationClassName
- CIM_Service.Name
- CIM_Service.PrimaryOwnerName
- CIM_Service.PrimaryOwnerContact
- CIM_Service.StartMode
- CIM_Service.Started
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b6ee3c51b6af50d77e94bb0a29bd1c8148cda8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307766"
---
# <a name="cim_service-class-hyper-v-management"></a>Classe CIM_Service (gestione Hyper-V)

Rappresenta un elemento logico che contiene informazioni per rappresentare e gestire la funzionalità fornita da una funzionalità del dispositivo o software. Un servizio è un oggetto generico per la configurazione e la gestione dell'implementazione di funzionalità. non si tratta della funzionalità stessa.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Version("2.14.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_Service : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  string  Name;
  string  PrimaryOwnerName;
  string  PrimaryOwnerContact;
  string  StartMode;
  boolean Started;
};
```

## <a name="members"></a>Members

La classe del **\_ servizio CIM** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe del **\_ servizio CIM** presenta questi metodi.



| Metodo                                           | Descrizione                    |
|:-------------------------------------------------|:-------------------------------|
| [**StartService**](cim-service-startservice.md) | avvia il servizio.<br/> |
| [**StopService**](cim-service-stopservice.md)   | arresta il servizio.<br/>  |



 

### <a name="properties"></a>Proprietà

La classe del **\_ servizio CIM** dispone di queste proprietà.

<dl> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Nome della classe utilizzato per creare un'istanza di questa classe. **CreationClassName** è combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**chiave**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificatore univoco del servizio che indica la funzionalità del servizio.

</dd> <dt>

**PrimaryOwnerContact**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni generali \| 001,4 ")
</dt> </dl>

Informazioni di contatto per il proprietario principale del servizio.

</dd> <dt>

**PrimaryOwnerName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| informazioni generali \| 001,3 ")
</dt> </dl>

Nome del proprietario primario del servizio.

</dd> <dt>

**Avviato**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**true** se il servizio è stato avviato. in caso contrario, **false**.

</dd> <dt>

**Modalità avvio**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**deprecato**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**\_ servizio CIM**.**EnabledDefault**"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Questa proprietà è deprecata. Usare invece la proprietà **EnabledDefault** ereditata da [**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md).

> [!Note]  
> Deprecated Description: indica se il servizio viene avviato automaticamente, ad esempio da un sistema operativo, oppure è stato avviato solo su richiesta.

 

<dt>



 ("Automatico")


</dt> <dd></dd> <dt>



 ("Manuale")


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**CreationClassName**")
</dt> </dl>

Nome della classe utilizzato per creare un'istanza del sistema che contiene il servizio. **SystemCreationClassName** è combinato con altre proprietà chiave di questa classe per identificare in modo univoco le istanze di questa classe e le relative sottoclassi.

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**propagato**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ sistema CIM**](cim-system.md).**Nome**")
</dt> </dl>

Nome del sistema di ambito.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8<br/>                                                                                    |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                                          |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ENABLEDLOGICALELEMENT CIM**](cim-enabledlogicalelement.md)
</dt> </dl>

 

