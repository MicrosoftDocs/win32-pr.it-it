---
description: Questa classe è la classe del tipo di evento per gli eventi di richiesta completa del driver. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: c9c9be05-c1c6-4d77-a47a-44a61ebfcdc7
title: Classe DriverCompleteRequest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverCompleteRequest
- DriverCompleteRequest.RoutineAddr
- DriverCompleteRequest.Irp
- DriverCompleteRequest.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2ef20d7bf097c35e03e94ee9bb80e7fd74ad93d3f28830c66b155b3cacf400b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151632"
---
# <a name="drivercompleterequest-class"></a>Classe DriverCompleteRequest

Questa classe è la classe del tipo di evento per gli eventi di richiesta completa del driver.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{52}, EventTypeName{"DrvComplReq"}]
class DriverCompleteRequest : DiskIo
{
  uint32 RoutineAddr;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Members

La **classe DriverCompleteRequest** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe DriverCompleteRequest** ha queste proprietà.

<dl> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2), Pointer
</dt> </dl>

Pacchetto di richiesta I/O.

</dd> <dt>

**RoutineAddr**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1), Pointer
</dt> </dl>

Indirizzo della funzione driver chiamata.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3)
</dt> </dl>

Identificatore che identifica in modo univoco la richiesta. Usare questo identificatore per la correlazione con gli altri eventi del driver, ad esempio [**l'evento DriverCompleteRequestReturn.**](drivercompleterequestreturn.md)

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

 

 




