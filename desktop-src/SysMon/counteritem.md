---
title: Oggetto CounterItem (Isysmon. h)
description: Utilizzare questa classe per recuperare il percorso e il valore di un contatore e per specificare il colore utilizzato per il grafico del contatore. Per recuperare questo oggetto, chiamare Counters. Item.
ms.assetid: 76b69395-efd8-4321-b7ed-63daa46e2636
keywords:
- Oggetto CounterItem SysMon
- Oggetto CounterItem SysMon, descritto
topic_type:
- apiref
api_name:
- CounterItem
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df999e327591309f015d8720f61643625eced4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741914"
---
# <a name="counteritem-object"></a>Oggetto CounterItem

Utilizzare questa classe per recuperare il percorso e il valore di un contatore e per specificare il colore utilizzato per il grafico del contatore.

Per recuperare questo oggetto, chiamare [**Counters. Item**](counters-item.md).

## <a name="members"></a>Membri

L'oggetto **CounterItem** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **CounterItem** dispone di questi metodi.



| Metodo                                             | Descrizione                                                                    |
|:---------------------------------------------------|:-------------------------------------------------------------------------------|
| [**GetDataAt**](counteritem-getdataat.md)         | Recupera i dati del contatore da un punto specifico nel grafico a linee.<br/> |
| [**GetStatistics**](counteritem-getstatistics.md) | Recupera i valori medio, massimo e minimo per il contatore.<br/> |
| [**GetValue**](counteritem-getvalue.md)           | Recupera l'ultimo valore del contatore.<br/>                            |



 

### <a name="properties"></a>Proprietà

L'oggetto **CounterItem** dispone di queste proprietà.



| Proprietà                                                  | Descrizione                                                                     |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**Colore**](counteritem-color.md)<br/>             | Recupera o imposta il colore utilizzato per rappresentare il valore del contatore.<br/>         |
| [**LineStyle**](counteritem-linestyle.md)<br/>     | Recupera o imposta lo stile di linea utilizzato per rappresentare il valore del contatore.<br/>    |
| [**Percorso**](counteritem-path.md)<br/>               | Recupera il percorso del contatore.<br/>                                   |
| [**ScaleFactor**](counteritem-scalefactor.md)<br/> | Recupera o imposta il fattore di scala utilizzato per rappresentare il valore del contatore.<br/>  |
| [**Selezionato**](counteritem-selected.md)<br/>       | Recupera o imposta un valore che indica se il contatore è selezionato.<br/> |
| [**Valore**](counteritem-value.md)<br/>             | Recupera il valore corrente del contatore.<br/>                          |
| [**Visible**](counteritem-visible.md)<br/>         | Recupera o imposta un valore che indica se il contatore è associato a un grafico.<br/>  |
| [**Larghezza**](counteritem-width.md)<br/>             | Recupera o imposta la lunghezza riga utilizzata per rappresentare il valore del contatore.<br/>    |



 

## <a name="remarks"></a>Commenti

[**Value**](counteritem-value.md) è la proprietà predefinita di **CounterItem**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                            |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi SYSMON](sysmon-classes.md)
</dt> </dl>

 

 





