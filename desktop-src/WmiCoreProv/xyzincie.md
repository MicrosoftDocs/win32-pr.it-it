---
description: Contiene le coordinate dello schermo nello spazio colori XYZ della International Commission on Illumination (CIE).
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: Classe XYZinCIE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: bc84f1550d2ba20daa0fb92dd3ce6f8d934207cff09de6d8b3e8b961bd341b6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110782"
---
# <a name="xyzincie-class"></a>Classe XYZinCIE

La classe WMI **XYZinCIE** contiene le coordinate dello schermo nello spazio colori XYZ della International Commission on Illumination (CIE).

## <a name="syntax"></a>Sintassi

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a>Members

La **classe XYZinCIE** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe XYZinCIE** ha queste proprietà.

<dl> <dt>

**X**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Coordinata X.

</dd> <dt>

**S**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Coordinata Y.

</dd> </dl>

## <a name="remarks"></a>Commenti

La [**classe WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) contiene istanze incorporate della **classe XYZinCIE** per descrivere le caratteristiche di colore di un monitoraggio.

Per calcolare la coordinata z, in base ai valori x e y, usare la relazione \| \| (x,y,z) \| \| = 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | Wmi \\ radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




