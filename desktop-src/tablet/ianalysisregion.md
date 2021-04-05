---
description: Espone metodi e proprietà per un'area che rappresenta un'area di un documento.
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: Interfaccia IAnalysisRegion (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c9c5e7653790e193c03b1cf4e0c489ea39c3eec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751858"
---
# <a name="ianalysisregion-interface"></a>Interfaccia IAnalysisRegion

Espone metodi e proprietà per un'area che rappresenta un'area di un documento.

## <a name="members"></a>Membri

L'interfaccia **IAnalysisRegion** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisRegion** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAnalysisRegion** dispone di questi metodi.



| Metodo                                                           | Descrizione                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Clone**](ianalysisregion-clone.md)                           | Crea una copia di **IAnalysisRegion**.<br/>                                                                                          |
| [**ExcludeRectangle**](ianalysisregion-excluderectangle.md)     | Limita l'area di **IAnalysisRegion** alla parte dell'area che non interseca il rettangolo specificato.<br/>           |
| [**ExcludeRegion**](ianalysisregion-excluderegion.md)           | Limita l'area di **IAnalysisRegion** alla parte dell'area che non interseca il **IAnalysisRegion** specificato.<br/> |
| [**GetBounds**](ianalysisregion-getbounds.md)                   | Recupera il rettangolo di delimitazione di **IAnalysisRegion**.<br/>                                                                        |
| [**GetRegionScans**](ianalysisregion-getregionscans.md)         | Recupera una matrice di rettangoli che definisce l'area di **IAnalysisRegion**.<br/>                                                  |
| [**IntersectRectangle**](ianalysisregion-intersectrectangle.md) | Limita l'area di questo **IAnalysisRegion** all'area creata dalla relativa intersezione con il rettangolo specificato.<br/>                |
| [**IntersectRegion**](ianalysisregion-intersectregion.md)       | Limita l'area di **IAnalysisRegion** all'area creata dalla relativa intersezione con il **IAnalysisRegion** specificato.<br/>       |
| [**IntersectsWith**](ianalysisregion-intersectswith.md)         | Determina se l'area del **IAnalysisRegion** interseca il rettangolo specificato.<br/>                                     |
| [**IsEmpty**](ianalysisregion-isempty.md)                       | Recupera un valore che indica se **IAnalysisRegion** rappresenta un'area vuota.<br/>                                            |
| [**IsInfinite**](ianalysisregion-isinfinite.md)                 | Recupera un valore che indica se **IAnalysisRegion** rappresenta un'area infinita.<br/>                                         |
| [**MakeEmpty**](ianalysisregion-makeempty.md)                   | Riduce il **IAnalysisRegion** per rappresentare un'area vuota.<br/>                                                                         |
| [**MakeInfinite**](ianalysisregion-makeinfinite.md)             | Espande **IAnalysisRegion** per rappresentare un'area infinita.<br/>                                                                      |
| [**UnionRectangle**](ianalysisregion-unionrectangle.md)         | Espande l'area di questo **IAnalysisRegion** all'area creata dalla relativa unione con il rettangolo specificato.<br/>                         |
| [**UnionRegion**](ianalysisregion-unionregion.md)               | Espande l'area di questo **IAnalysisRegion** all'area creata dalla relativa unione con il **IAnalysisRegion** specificato.<br/>               |



 

## <a name="remarks"></a>Commenti

Questa interfaccia rappresenta un'area costruita da aree rettangolari. [**IInkAnalyzer**](iinkanalyzer.md) restituisce o interpreta le coordinate di un'area all'interno dello spazio delle coordinate in cui riceve i dati del tratto.

Per ottenere i limiti correnti di **IAnalysisRegion**, usare il metodo [**IAnalysisRegion:: GetBounds**](ianalysisregion-getbounds.md) o [**IAnalysisRegion:: GetRegionScans**](ianalysisregion-getregionscans.md).

Per modificare l'area di un **IAnalysisRegion** esistente, utilizzare i metodi seguenti.

-   [**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
-   [**Metodo IAnalysisRegion:: ExcludeRegion**](ianalysisregion-excluderegion.md)
-   [**Metodo IAnalysisRegion:: IntersectRectangle**](ianalysisregion-intersectrectangle.md)
-   [**Metodo IAnalysisRegion:: IntersectRegion**](ianalysisregion-intersectregion.md)
-   [**Metodo IAnalysisRegion:: MakeEmpty**](ianalysisregion-makeempty.md)
-   [**Metodo IAnalysisRegion:: MakeInfinite**](ianalysisregion-makeinfinite.md)
-   [**Metodo IAnalysisRegion:: UnionRectangle**](ianalysisregion-unionrectangle.md)
-   [**Metodo IAnalysisRegion:: UnionRegion**](ianalysisregion-unionregion.md)

Questa interfaccia è equivalente alla classe System. Windows. Ink. AnalysisCore. AnalysisRegionBase nel .NET Framework.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

