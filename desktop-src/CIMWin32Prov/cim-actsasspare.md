---
description: L'associazione CIM ActsAsSpare indica quali elementi possono essere di riserva \_ o sostituire altri elementi aggregati. Una riserva può operare in modalità &\# 0034;hot standby&0034; come specificato in base a un elemento \# per elemento.
ms.assetid: bed8c552-f782-4af9-9441-ff3268182c3b
ms.tgt_platform: multiple
title: CIM_ActsAsSpare classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActsAsSpare
- CIM_ActsAsSpare.Group
- CIM_ActsAsSpare.HotStandby
- CIM_ActsAsSpare.Spare
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6b76b9dbd4a5a3302d1aae328bcd096dee5cd03e1615d3c7e30c58f3344ea67f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080955"
---
# <a name="cim_actsasspare-class"></a>Classe CIM \_ ActsAsSpare

**L'associazione CIM \_ ActsAsSpare** indica quali elementi possono essere di riserva o sostituire altri elementi aggregati. Una riserva può operare in modalità "hot standby" come specificato elemento per elemento.

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico, non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract, Association, UUID("{64C1726E-DB21-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_ActsAsSpare
{
  CIM_SpareGroup           REF Group;
  boolean                      HotStandby;
  CIM_ManagedSystemElement REF Spare;
};
```

## <a name="members"></a>Members

La **classe CIM \_ ActsAsSpare** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe CIM \_ ActsAsSpare** ha queste proprietà.

<dl> <dt>

**Gruppo**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ SpareGroup**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento alla **proprietà Group** che rappresenta la classe [**CIM \_ SpareGroup.**](cim-sparegroup.md)

</dd> <dt>

**HotStandby**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **TRUE,** il ricambio funziona come hot standby.

</dd> <dt>

**Ricambio**
</dt> <dd> <dl> <dt>

Tipo di dati: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento a un elemento di sistema gestito che funge da riserva e partecipa al gruppo di riserva.

</dd> </dl>

## <a name="remarks"></a>Commenti

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

[Classi CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

