---
description: Specifica la guida o l'area in cui viene disegnato e riconosciuto l'input penna.
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: Struttura InkAnalysisRecognizerGuide (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerGuide
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: eab5b1d09354f021f2c0a7e66a41b53e761d51e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306741"
---
# <a name="inkanalysisrecognizerguide-structure"></a>Struttura InkAnalysisRecognizerGuide

Specifica la guida o l'area in cui viene disegnato e riconosciuto l'input penna.

## <a name="syntax"></a>Sintassi


```C++
typedef struct InkAnalysisRecognizerGuide {
  RECT rectWritingBox;
  RECT rectDrawnBox;
  long cRows;
  long cColumns;
  long midline;
} InkAnalysisRecognizerGuide;
```



## <a name="members"></a>Members

<dl> <dt>

**rectWritingBox**
</dt> <dd>

Area di scrittura invisibile della Guida al riconoscimento in cui è possibile eseguire effettivamente la scrittura.

</dd> <dt>

**rectDrawnBox**
</dt> <dd>

Rettangolo disegnato sulla schermata del tablet e in cui viene effettuato la scrittura.

</dd> <dt>

**Corvi**
</dt> <dd>

Il numero di righe nella casella della Guida per il riconoscimento.

</dd> <dt>

**cColumns**
</dt> <dd>

Il numero di colonne nella casella della Guida per il riconoscimento.

</dd> <dt>

**midline**
</dt> <dd>

Altezza della linea media della casella della Guida per il riconoscimento. L'altezza del midline è la distanza tra la linea di base e la linea media, della casella disegnata.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un **InkAnalysisRecognizerGuide** definisce un'area di input prevista, ad esempio una riga o caselle, per i caratteri. Una struttura **InkAnalysisRecognizerGuide** può essere impostata solo in un nodo di contesto dell'hint di analisi (vedere [**IContextNode:: GetType**](icontextnode-gettype.md)). [**IInkAnalyzer**](iinkanalyzer.md) usa il percorso del nodo hint di analisi e i percorsi dei tratti di input penna per associare un tratto al nodo hint di analisi. Tutti i tratti con un'associazione al nodo hint di analisi avranno il **InkAnalysisRecognizerGuide** specificato usato quando riconosciuti da un **IInkAnalyzer**, purché **IInkAnalyzer** supporti **InkAnalysisRecognizerGuide**. I valori espressi nella classe **InkAnalysisRecognizerGuide** sono sempre relativi alla posizione del nodo hint di analisi e sono specificati nelle coordinate dello spazio di input penna.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Proprietà hint di analisi](analysis-hint-properties.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: CreateAnalysisHint**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IContextNode:: AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**IContextNode:: GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




