---
title: CIM_Setting classe (Servizi Desktop remoto)
description: Rappresenta i parametri operativi e correlati alla configurazione per uno o più elementi di sistema gestiti.
ms.assetid: d0007762-5d13-421b-a73a-3392a77686a6
ms.tgt_platform: multiple
keywords:
- CIM_Setting classe Servizi Desktop remoto
- CIM_Setting classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- CIM_Setting
- CIM_Setting.Caption
- CIM_Setting.Description
- CIM_Setting.InstallDate
- CIM_Setting.Name
- CIM_Setting.Status
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d53499c383c6fcf9ae2774427afcea2ea339408ff0292a3d4ce15286a4a75298
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118131320"
---
# <a name="cim_setting-class-remote-desktop-services"></a>CIM_Setting classe (Servizi Desktop remoto)

Rappresenta i parametri operativi e correlati alla configurazione per uno o più elementi di sistema gestiti.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{8502C518-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Setting : CIM_ManagedSystemElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
};
```

## <a name="members"></a>Members

La **classe \_ CiM Setting** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ CiM Setting** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione (stringa di una riga) dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**mappingstring**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Data di installazione dell'oggetto. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: "OK", "Degraded" e "Pred Fail" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente ma prevedere un errore nel prossimo futuro). Gli stati nonoperational includono: "Error", "Starting", "Stopping" e "Service". Quest'ultimo, "Servizio", può essere applicato durante il ridimensionamento del mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono in linea, ma l'elemento gestito non è né "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Danneggiato")


</dt> <dd></dd> <dt>



 ("Sconosciuto")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Starting")


</dt> <dd></dd> <dt>



 ("Arresto")


</dt> <dd></dd> <dt>



 ("Servizio")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ cimv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> </dl>

 

