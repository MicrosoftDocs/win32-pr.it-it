---
description: Identifica una proprietà che deve essere impostata su una transizione o un effetto, insieme al numero di valori distinct che la proprietà presuppone per la durata della transizione o dell'effetto.
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: Struttura DEXTER_VALUE (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_VALUE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329146"
---
# <a name="dexter_value-structure"></a>\_Struttura del valore Dexter

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Identifica una proprietà che deve essere impostata su una transizione o un effetto, insieme al numero di valori distinct che la proprietà presuppone per la durata della transizione o dell'effetto.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a>Members

<dl> <dt>

**v**
</dt> <dd>

Valore della proprietà.

</dd> <dt>

**RT**
</dt> <dd>

Tempo in cui la proprietà presuppone il valore, relativo all'inizio della transizione o dell'effetto.

</dd> <dt>

**dwInterp**
</dt> <dd>

Flag che indica il modo in cui la proprietà avanza dal valore precedente a questo valore. I possibili valori sono i seguenti:



| Valore                                                                                                                                                                           | Significato                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <dt>**DEXTERF \_ Jump**</dt> </dl>                      | La proprietà passa immediatamente al nuovo valore all'ora specificata.<br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <dt>**\_interpolazione DEXTERF**</dt> </dl> | La proprietà viene interpolata in modo lineare nel tempo rispetto al valore precedente.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>Qedit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[**\_param Dexter**](dexter-param.md)
</dt> </dl>

 

 




