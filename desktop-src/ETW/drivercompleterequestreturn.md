---
description: Questa classe è la classe del tipo di evento per gli eventi di restituzione della richiesta completa del driver. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 04505f8c-a11e-4bf7-91c0-fca1b5846d80
title: Classe DriverCompleteRequestReturn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequestReturn
- DriverCompleteRequestReturn.Irp
- DriverCompleteRequestReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: be19cd1a4b8f7cf4957d08f9ccebf01c5e8646ade06cce9708e645c1a7ea2a5b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901211"
---
# <a name="drivercompleterequestreturn-class"></a>Classe DriverCompleteRequestReturn

Questa classe è la classe del tipo di evento per gli eventi di restituzione della richiesta completa del driver.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{53}, EventTypeName{"DrvComplReqRet"}]
class DriverCompleteRequestReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Members

La **classe DriverCompleteRequestReturn** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe DriverCompleteRequestReturn** ha queste proprietà.

<dl> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Pointer
</dt> </dl>

Pacchetto di richiesta I/O.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2)
</dt> </dl>

Identificatore che identifica in modo univoco la richiesta. Usare questo identificatore per la correlazione con gli altri eventi del driver, ad esempio [**l'evento DriverCompleteRequest.**](drivercompleterequest.md)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




