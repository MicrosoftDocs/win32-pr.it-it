---
description: Aggiunge i dati del tratto per più tratti a IInkAnalyzer e assegna l'identificatore delle impostazioni cultura del thread di input attivo ai tratti.
ms.assetid: 4a8d6828-699b-465d-b057-197866ff069f
title: 'Metodo IInkAnalyzer:: AddStrokes (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bc616f8a388010df2b3d39ea55622d81fa5ce3a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307400"
---
# <a name="iinkanalyzeraddstrokes-method"></a>Metodo IInkAnalyzer:: AddStrokes

Aggiunge i dati del tratto per più tratti a [**IInkAnalyzer**](iinkanalyzer.md) e assegna l'identificatore delle impostazioni cultura del thread di input attivo ai tratti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddStrokes(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plStrokeIds,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeIdsCount* \[ in\]
</dt> <dd>

Numero di tratti da aggiungere.

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

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ out\]
</dt> <dd>

[**IContextNode**](icontextnode.md) a cui sono stati aggiunti i tratti dall'analizzatore di input penna.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodeStrokeAddedTo* quando non è più necessario utilizzare l'oggetto.

 

Quando *ppContextNodeStrokeAddedTo* è **null**, indica che il chiamante non è interessato al valore restituito dal metodo.

[**IInkAnalyzer**](iinkanalyzer.md) aggiunge i tratti a un [**IContextNode**](icontextnode.md) di tipo UnclassifiedInk (vedere tipi di [nodo di contesto](context-node-types.md)). Questo nodo si trova nella raccolta dei sottonodi del nodo radice (vedere [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) Methods).

[**IInkAnalyzer**](iinkanalyzer.md) assegna l'identificatore delle impostazioni cultura del thread di input attivo ai tratti e aggiunge i tratti al primo nodo di contesto UnclassifiedInk nel nodo radice dell'analizzatore di input penna che contiene i tratti con lo stesso identificatore di impostazioni cultura. Se l'analizzatore di input penna non dispone di un nodo con lo stesso identificatore di impostazioni cultura, viene creato un nuovo nodo di contesto UnclassifiedInk nel nodo radice e i tratti vengono aggiunti al nuovo nodo di contesto UnclassifiedInk.

*plStrokePacketData* contiene i dati dei pacchetti per tutti i tratti. *pStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (Guid) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto in ogni tratto. Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [costanti PacketPropertyGuids](packetpropertyguids-constants.md).

> [!Note]  
> Solo i tratti con le stesse descrizioni di pacchetti possono essere aggiunti in una singola chiamata al **Metodo IInkAnalyzer:: AddStrokes**.

 

Questo metodo espande l'area dirty all'Unione del valore corrente dell'area e del rettangolo di delimitazione dei tratti aggiunti.

Se [**IInkAnalyzer**](iinkanalyzer.md) contiene già un tratto con lo stesso identificatore di uno dei tratti da aggiungere, il **IInkAnalyzer** restituisce un valore **HRESULT** di **E \_ INVALIDARG**.

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

[**Metodo IInkAnalyzer:: AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: RemoveStroke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: RemoveStrokes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

