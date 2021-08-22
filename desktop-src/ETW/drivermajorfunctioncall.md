---
description: Questa classe è la classe del tipo di evento per gli eventi di chiamata di funzione principali del driver. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 8c913145-ac50-4d40-8519-5fed79d977ba
title: Classe DriverMajorFunctionCall
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionCall
- DriverMajorFunctionCall.MajorFunction
- DriverMajorFunctionCall.MinorFunction
- DriverMajorFunctionCall.RoutineAddr
- DriverMajorFunctionCall.FileObject
- DriverMajorFunctionCall.Irp
- DriverMajorFunctionCall.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: b69012ae3d9dd46d2dd54c3859895288b9113fa89c772172e3f66a730b058d4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070241"
---
# <a name="drivermajorfunctioncall-class"></a>Classe DriverMajorFunctionCall

Questa classe è la classe del tipo di evento per gli eventi di chiamata di funzione principali del driver.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{34}, EventTypeName{"DrvMjFnCall"}]
class DriverMajorFunctionCall : DiskIo
{
  uint32 MajorFunction;
  uint32 MinorFunction;
  uint32 RoutineAddr;
  uint32 FileObject;
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Members

La **classe DriverMajorFunctionCall** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe DriverMajorFunctionCall** ha queste proprietà.

<dl> <dt>

**FileObject**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4), Pointer
</dt> </dl>

Trova la corrispondenza del valore di questo puntatore al valore del puntatore **FileObject** in un evento [**\_ DiskIo TypeGroup1**](diskio-typegroup1.md) per determinare il tipo di operazione di I/O.

</dd> <dt>

**Irp**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(5), Pointer
</dt> </dl>

Pacchetto di richiesta I/O.

</dd> <dt>

**MajorFunction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1)
</dt> </dl>

Codice che identifica la funzione principale chiamata.

</dd> <dt>

**MinorFunction**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2)
</dt> </dl>

Codice che indica la funzione secondaria chiamata.

</dd> <dt>

**RoutineAddr**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3), Pointer
</dt> </dl>

Indirizzo della funzione driver chiamata.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(6)
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

 

 




