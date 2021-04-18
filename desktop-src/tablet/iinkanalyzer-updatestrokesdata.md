---
description: Aggiorna i dati dei pacchetti per i tratti specificati.
ms.assetid: 7fca4c39-eef2-4019-86a0-27cd0e4e7510
title: 'Metodo IInkAnalyzer:: UpdateStrokesData (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.UpdateStrokesData
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 151403a7114bca2644d0425fdba0155135ac9ed8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307369"
---
# <a name="iinkanalyzerupdatestrokesdata-method"></a>Metodo IInkAnalyzer:: UpdateStrokesData

Aggiorna i dati dei pacchetti per i tratti specificati.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdateStrokesData(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds,
  [in] ULONG ulStrokePacketDescriptionCount,
  [in] GUID  *pStrokePacketDescriptionGuids,
  [in] ULONG *pulPacketDataCountPerStroke,
  [in] LONG  *plStrokePacketData
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeIdsCount* \[ in\]
</dt> <dd>

Numero di tratti da aggiornare.

</dd> <dt>

*plStrokeIds* \[ in\]
</dt> <dd>

Matrice contenente gli identificatori del tratto.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ in\]
</dt> <dd>

Numero di proprietà in ogni pacchetto.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ in\]
</dt> <dd>

Matrice contenente gli identificatori di proprietà del pacchetto.

</dd> <dt>

*pulPacketDataCountPerStroke* \[ in\]
</dt> <dd>

Matrice contenente il numero di pacchetti in ogni tratto.

</dd> <dt>

*plStrokePacketData* \[ in\]
</dt> <dd>

Matrice contenente i dati dei pacchetti per i tratti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

il parametro *plStrokePacketData* contiene i dati dei pacchetti per tutti i tratti. Il parametro *pStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (Guid) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto in ogni tratto. Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [costanti PacketPropertyGuids](packetpropertyguids-constants.md).

Solo i tratti con le stesse descrizioni di pacchetti possono essere aggiornati in una singola chiamata al **Metodo IInkAnalyzer:: UpdateStrokesData**.

Questo metodo non aggiorna l'area dirty dell'analizzatore di input penna (vedere il [**Metodo IInkAnalyzer:: GetDirtyRegion**](iinkanalyzer-getdirtyregion.md)).

Se un tratto specificato non è associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo ignora l'identificatore.

Se nessuno dei tratti specificati identifica un tratto associato a [**IInkAnalyzer**](iinkanalyzer.md), questo metodo restituisce senza aggiornare **IInkAnalyzer**.

Questo metodo restituisce un codice di errore quando *plStrokeIds* è **null**.

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

[**Metodo IInkAnalyzer:: AddStroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokeToCustomRecognizer**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: ClearStrokeData**](iinkanalyzer-clearstrokedata.md)
</dt> <dt>

[**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

 




