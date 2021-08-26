---
description: Contiene una raccolta di oggetti che implementano l'interfaccia IAnalysisAlternate e che sono il risultato dell'analisi dell'input penna.
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: Interfaccia IAnalysisAlternates (IACom.h)
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
ms.openlocfilehash: e2643ef8ea90d029aee6bd0673931d27e9987b0af0a898e854cb87d74a89c0af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058091"
---
# <a name="ianalysisalternates-interface"></a>Interfaccia IAnalysisAlternates

Contiene una raccolta di oggetti che implementano [**l'interfaccia IAnalysisAlternate**](ianalysisalternate.md) e che sono il risultato dell'analisi dell'input penna.

## <a name="members"></a>Membri

**L'interfaccia IAnalysisAlternates** eredita dall'interfaccia [**IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IAnalysisAlternates** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

Questi metodi sono disponibili nell'interfaccia **IAnalysisAlternates.**



| Metodo                                                                   | Descrizione                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnalysisAlternate**](ianalysisalternates-getanalysisalternate.md) | Recupera [**l'oggetto IAnalysisAlternate**](ianalysisalternate.md) in corrispondenza dell'indice specificato all'interno della raccolta.<br/>                   |
| [**GetCount**](ianalysisalternates-getcount.md)                         | Recupera il numero di [**oggetti IAnalysisAlternate**](ianalysisalternate.md) contenuti nella raccolta **IAnalysisAlternates.**<br/> |



 

## <a name="remarks"></a>Commenti

Questa interfaccia equivale a [**System.Windows. Classe Ink.AnalysisCore.AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100)) nel .NET Framework.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetAlternates**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetAlternatesForContextNodes**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::GetAlternatesForStrokes**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

