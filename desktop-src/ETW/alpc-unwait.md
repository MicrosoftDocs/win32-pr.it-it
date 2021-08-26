---
description: Questa classe è la classe del tipo di evento per gli eventi di attesa di fine ALPC. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: 89a357dd-c217-4b55-994a-4252fa3cae1c
title: ALPC_Unwait classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Unwait
- ALPC_Unwait.Status
api_type:
- NA
api_location: ''
ms.openlocfilehash: de6e04fce0f581b3f37e3a049590914b1355d197952c74190457a402e597edcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901711"
---
# <a name="alpc_unwait-class"></a>Classe ALPC \_ Unwait

Questa classe è la classe del tipo di evento per gli eventi di attesa di fine ALPC.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(37), EventTypeName("ALPC-Unwait")]
class ALPC_Unwait : ALPC
{
  uint32 Status;
};
```

## <a name="members"></a>Members

La **classe ALPC \_ Unwait** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe ALPC \_ Unwait** ha queste proprietà.

<dl> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stato dell'operazione di attesa.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 




