---
description: Specifica il modo in cui IInkAnalyzer esegue l'analisi dell'input penna.
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: Enumerazione AnalysisModes (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisModes
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b9fdebd3ef3cd505b49ff6c82f7609bc339af0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401518"
---
# <a name="analysismodes-enumeration"></a>Enumerazione AnalysisModes

Specifica il modo in cui [**IInkAnalyzer**](iinkanalyzer.md) esegue l'analisi dell'input penna.

## <a name="syntax"></a>Sintassi


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes \_ None**
</dt> <dd>

Non è stata specificata alcuna modalità.

</dd> <dt>

<span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**\_AutomaticReconciliation AnalysisModes**
</dt> <dd>

Indica se il [**IInkAnalyzer**](iinkanalyzer.md) avvia automaticamente l'operazione di riconciliazione non appena i risultati intermedi o finali sono pronti.

Se questa modalità è abilitata, l'evento [**\_ IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md) non viene generato. Se questa modalità è disabilitata, viene generato l'evento **\_ IAnalysisEvents:: ReadyToReconcile** .

</dd> <dt>

<span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**\_StrokeCacheAutoCleanup AnalysisModes**
</dt> <dd>

Indica se [**IInkAnalyzer**](iinkanalyzer.md) cancella automaticamente i tratti non necessari dalla cache del tratto prima di eseguire l'analisi.

Se questa modalità è abilitata, [**IInkAnalyzer**](iinkanalyzer.md) Cancella i dati del tratto prima di eseguire l'analisi. Il codice deve anche gestire l'evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) . Se l'evento **\_ IAnalysisEvents:: UpdateStrokesCache** non è gestito, viene generata un'eccezione. Questa verifica viene eseguita sia in fase di analisi (o BackgroundAnalyze) che in fase di riconciliazione.

Se questa modalità è disabilitata, [**IInkAnalyzer**](iinkanalyzer.md) non cancella i dati del tratto. Per cancellare i dati del tratto, chiamare il [**Metodo IInkAnalyzer:: ClearStrokeData**](iinkanalyzer-clearstrokedata.md). Se questa modalità è disabilitata, viene generato l'evento [**\_ IAnalysisEvents:: UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md) in modo che **IInkAnalyzer** possa recuperare i dati del tratto più recenti per tutti i tratti per i quali la cache è stata cancellata. Se la cache del tratto viene deselezionata, ma l'evento **\_ IAnalysisEvents:: UpdateStrokesCache** non viene gestito, viene generata un'eccezione.

</dd> <dt>

<span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**\_PersonalizationEnabled AnalysisModes**
</dt> <dd>

Personalizzazione del riconoscimento della grafia abilitata.

</dd> <dt>

<span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**\_Impostazione predefinita AnalysisModes**
</dt> <dd>

Tutte le modalità sono abilitate.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa enumerazione consente una combinazione bit per bit dei relativi valori dei membri.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop Windows XP Tablet PC Edition \[\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom. h (richiede anche IACom \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Metodo IInkAnalyzer:: GetAnalysisModes**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: SetAnalysisModes**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**\_IAnalysisEvents:: IntermediateResults ()**](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[**\_IAnalysisEvents:: ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




