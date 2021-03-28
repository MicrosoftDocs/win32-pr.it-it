---
description: Questa classe è la classe del tipo di evento per gli eventi di restituzione della chiamata di funzione principale del driver. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: b3358935-d6fb-49eb-bdf7-4366b4fd14c5
title: Classe DriverMajorFunctionReturn
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DriverMajorFunctionReturn
- DriverMajorFunctionReturn.Irp
- DriverMajorFunctionReturn.UniqMatchId
api_type:
- NA
api_location: ''
ms.openlocfilehash: 21340224253d1eb3f3ddc733bf2d43e847844282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525249"
---
# <a name="drivermajorfunctionreturn-class"></a>Classe DriverMajorFunctionReturn

Questa classe è la classe del tipo di evento per gli eventi di restituzione della chiamata di funzione principale del driver.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType{35}, EventTypeName{"DrvMjFnRet"}]
class DriverMajorFunctionReturn : DiskIo
{
  uint32 Irp;
  uint32 UniqMatchId;
};
```

## <a name="members"></a>Members

La classe **DriverMajorFunctionReturn** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **DriverMajorFunctionReturn** dispone di queste proprietà.

<dl> <dt>

**IRP**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1), puntatore
</dt> </dl>

Pacchetto di richiesta IO.

</dd> <dt>

**UniqMatchId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2)
</dt> </dl>

Identificatore che identifica in modo univoco la richiesta. Usare questo identificatore per la correlazione con gli altri eventi del driver, ad esempio l'evento [**DriverCompleteRequest**](drivercompleterequest.md) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DiskIo**](diskio.md)
</dt> </dl>

 

 




