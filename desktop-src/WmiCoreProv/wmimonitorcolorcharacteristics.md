---
description: Rappresenta le caratteristiche dei colori CIE (International Commission on illuminazione) di un monitor del computer.
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: Classe WmiMonitorColorCharacteristics
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 9fbb7d56e56519576d257b077311a144e923d6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346506"
---
# <a name="wmimonitorcolorcharacteristics-class"></a>Classe WmiMonitorColorCharacteristics

La classe **WmiMonitorColorCharacteristics** rappresenta le caratteristiche dei colori CIE (International Commission on illuminazione) di un monitor del computer. I dati corrispondono ai dati nel blocco delle caratteristiche dei colori della struttura di EDID (video Electronics Standard Association) Enhanced Extended Display Data.

## <a name="syntax"></a>Sintassi

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a>Members

La classe **WmiMonitorColorCharacteristics** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **WmiMonitorColorCharacteristics** dispone di queste proprietà.

<dl> <dt>

**Attivo**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica il monitoraggio attivo.

</dd> <dt>

**Blue**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Coordinate CIE per il blu, rappresentate da un'istanza della classe [**XYZinCIE**](xyzincie.md) .

</dd> <dt>

**DefaultWhite**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Coordinate CIE bianche predefinite.

</dd> <dt>

**Green**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Coordinate CIE per il verde, rappresentate da un'istanza della classe [**XYZinCIE**](xyzincie.md) .

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Nome dell'istanza di monitoraggio specifica.

</dd> <dt>

**Red**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Coordinate CIE per il rosso, rappresentate da un'istanza della classe [**XYZinCIE**](xyzincie.md) .

</dd> </dl>

## <a name="remarks"></a>Commenti

I valori della cromaticità e del punto bianco sono espressi come numeri frazionari usando un formato di codifica. Questo formato è accurato per la millesima posizione, con una lunghezza di 10 bit. Il bit più significativo (MSB) rappresenta 2 ^-1 e il bit meno significativo (LSB) rappresenta i coefficienti rispettivamente 2 ^-10. La precisione dei valori archiviati nella struttura E-EDID V1. x deve essere precisa a +/-0,005 del valore effettivo.

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

 

 




