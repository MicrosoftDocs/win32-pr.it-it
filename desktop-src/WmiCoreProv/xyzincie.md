---
description: Contiene le coordinate dello schermo nello spazio dei colori di International Commission on illuminazione (CIE) XYZ.
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
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316997"
---
# <a name="xyzincie-class"></a>Classe XYZinCIE

La classe WMI **XYZinCIE** contiene le coordinate dello schermo nello spazio dei colori di International Commission on illuminazione (CIE) XYZ.

## <a name="syntax"></a>Sintassi

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a>Members

La classe **XYZinCIE** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **XYZinCIE** dispone di queste proprietà.

<dl> <dt>

**X**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Coordinata X.

</dd> <dt>

**S**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Coordinata Y.

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) contiene istanze incorporate della classe **XYZinCIE** per descrivere le caratteristiche dei colori di un monitoraggio.

Per calcolare la coordinata z, in base ai valori x e y, usare la relazione \| \| (x, y, z) \| \| = 1.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                         |
| Spazio dei nomi<br/>                | \\WMI radice<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




