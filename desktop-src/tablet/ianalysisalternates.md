---
description: Contiene una raccolta di oggetti che implementano l'interfaccia IAnalysisAlternate e che sono il risultato dell'analisi dell'input penna.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: Interfaccia IAnalysisAlternates (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4e43feaa40f519707531894936bf34ce19e57723
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307470"
---
# <a name="ianalysisalternates-interface"></a>Interfaccia IAnalysisAlternates

Contiene una raccolta di oggetti che implementano l'interfaccia [**IAnalysisAlternate**](ianalysisalternate.md) e che sono il risultato dell'analisi dell'input penna.

## <a name="members"></a>Membri

L'interfaccia **IAnalysisAlternates** eredita dall'interfaccia [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IAnalysisAlternates** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IAnalysisAlternates** dispone di questi metodi.



| Metodo                                                                   | Descrizione                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnalysisAlternate**](ianalysisalternates-getanalysisalternate.md) | Recupera l'oggetto [**IAnalysisAlternate**](ianalysisalternate.md) in corrispondenza dell'indice specificato all'interno dell'insieme.<br/>                   |
| [**GetCount**](ianalysisalternates-getcount.md)                         | Recupera il numero di oggetti [**IAnalysisAlternate**](ianalysisalternate.md) contenuti nella raccolta **IAnalysisAlternates** .<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia è equivalente alla classe [**System. Windows. Ink. AnalysisCore. AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) nel .NET Framework.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: getalters**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

