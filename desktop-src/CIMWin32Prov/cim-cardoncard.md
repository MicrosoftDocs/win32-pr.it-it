---
description: L'associazione CIM CardOnCard descrive le relazioni relative alle schede che possono essere collegate a schede madri/schede di base, schede figlie di un adattatore o schede che supportano moduli speciali simili a \_ schede.
ms.assetid: a500b29d-d836-4755-b5df-b296e3cbd2ab
ms.tgt_platform: multiple
title: CIM_CardOnCard classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CardOnCard
- CIM_CardOnCard.LocationWithinContainer
- CIM_CardOnCard.PartComponent
- CIM_CardOnCard.GroupComponent
- CIM_CardOnCard.MountOrSlotDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2f6b20d95505f1e6dbbda31506660f3825541f8f2a0ecdcb6cf293d7d6d4a0df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322441"
---
# <a name="cim_cardoncard-class"></a>Classe CIM \_ CardOnCard

**L'associazione CIM \_ CardOnCard** descrive le relazioni relative alle schede che possono essere collegate a schede madri/schede di base, schede figlie di un adattatore o schede che supportano moduli speciali simili a schede.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, UUID("{FAF76B77-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_CardOnCard : CIM_Container
{
  string       LocationWithinContainer;
  CIM_Card REF PartComponent;
  CIM_Card REF GroupComponent;
  string       MountOrSlotDescription;
};
```

## <a name="members"></a>Members

La **classe CIM \_ CardOnCard** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ CardOnCard** ha queste proprietà.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **scheda CIM \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Scheda [**CIM \_ che**](cim-card.md) descrive la scheda che ospita un'altra scheda.

</dd> <dt>

**LocationWithinContainer**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che rappresenta il posizionamento dell'elemento fisico all'interno del pacchetto fisico. In questa proprietà è possibile registrare informazioni relative agli elementi stazionari nel contenitore ,ad esempio "second drive bay from the top", angolazioni, altitudini e altri dati. Questa stringa può integrare o essere usata al posto della creazione di un'istanza [**dell'oggetto \_ Location CIM.**](cim-location.md)

Questa proprietà viene ereditata dal [**contenitore CIM. \_**](cim-container.md)

</dd> <dt>

**MountOrSlotDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrive e identifica il modo in cui la scheda viene montata o collegata alla scheda "altro". Le informazioni sugli slot possono essere incluse in questo campo e possono essere sufficienti per determinati scopi di gestione, evitando così di creare istanze di oggetti connettore/slot solo per modellare la relazione delle schede con le schede di hosting o altri adattatori. D'altra parte, se sono disponibili informazioni su slot e connettori, questo campo può essere usato per fornire dati di montaggio o inserimento dello slot dettagliati.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo di dati: **scheda CIM \_**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Scheda [**CIM \_ che**](cim-card.md) descrive la scheda collegata o montata in altro modo in un'altra scheda.

</dd> </dl>

## <a name="remarks"></a>Commenti

La **classe CIM \_ CardOnCard** deriva da [**CIM \_ Container.**](cim-container.md)

WMI non implementa questa classe.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Contenitore \_ CIM**](cim-container.md)
</dt> </dl>

 

