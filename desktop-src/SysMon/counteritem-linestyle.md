---
title: Proprietà CounterItem. LineStyle
description: Recupera o imposta lo stile di linea utilizzato per rappresentare il valore del contatore.
ms.assetid: 5801f0f8-37e5-4b15-a13f-24c71fea550d
keywords:
- Proprietà LineStyle SysMon
- Proprietà LineStyle SysMon, classe CounterItem
- Classe CounterItem SysMon, proprietà LineStyle
topic_type:
- apiref
api_name:
- CounterItem.LineStyle
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff1dd78c6fd65d72c28fe8f13f7bbf5603c75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964181"
---
# <a name="counteritemlinestyle-property"></a>Proprietà CounterItem. LineStyle

Recupera o imposta lo stile di linea utilizzato per rappresentare il valore del contatore.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Property LineStyle As Long
```



## <a name="property-value"></a>Valore proprietà

Stile di linea utilizzato per rappresentare il valore del contatore. I valori corrispondono alle costanti di sistema illustrate nella tabella seguente.



| Valore                                                                                                                                                                                                                                                                                                                                                                               | Significato                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="System.Drawing.Drawing2D.DashStyle.Solid"></span><span id="system.drawing.drawing2d.dashstyle.solid"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.SOLID"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. Solid**</dt> <dt>0</dt> </dl>                     | Linea continua. Si tratta del valore predefinito.<br/>                |
| <span id="System.Drawing.Drawing2D.DashStyle.Dash"></span><span id="system.drawing.drawing2d.dashstyle.dash"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASH"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. Dash**</dt> <dt>1</dt> </dl>                         | Linea tratteggiata con segmenti lunghi e spazi stretti.<br/>     |
| <span id="System.Drawing.Drawing2D.DashStyle.Dot"></span><span id="system.drawing.drawing2d.dashstyle.dot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DOT"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. dot**</dt> <dt>2</dt> </dl>                             | Linea tratteggiata con segmenti e spazi uniformi.<br/>         |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOT"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. DashDot**</dt> <dt>3</dt> </dl>             | Linea tratteggiata con segmenti alternati brevi e lunghi.<br/> |
| <span id="System.Drawing.Drawing2D.DashStyle.DashDotDot"></span><span id="system.drawing.drawing2d.dashstyle.dashdotdot"></span><span id="SYSTEM.DRAWING.DRAWING2D.DASHSTYLE.DASHDOTDOT"></span><dl> <dt>**System. Drawing. Drawing2D. DashStyle. TrattoPuntoPunto**</dt> <dt>4</dt> </dl> | Linea tratteggiata con trattini alternati e punti doppi.<br/>  |



 

## <a name="exceptions"></a>Eccezioni



| Tipo di eccezione               | Condizione                              |
|------------------------------|----------------------------------------|
| **System. ArgumentException** | Lo stile di linea specificato non è valido. |



 

## <a name="remarks"></a>Commenti

Per specificare un valore diverso da DashStyle. Solid, [**CounterItem. Width**](counteritem-width.md) deve essere impostato su 1. Se la larghezza è maggiore di 1, SYSMON ignora lo stile di linea specificato e USA DashStyle. Solid.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CounterItem**](counteritem.md)
</dt> </dl>

 

 





