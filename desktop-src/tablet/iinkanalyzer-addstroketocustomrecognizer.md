---
description: Aggiunge i dati del tratto per un singolo tratto a un nodo di riconoscimento personalizzato.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: 'Metodo IInkAnalyzer:: AddStrokeToCustomRecognizer (IACom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokeToCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c04b60acd2f40b5ed3960c9932ce066b337d81cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307397"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a>Metodo IInkAnalyzer:: AddStrokeToCustomRecognizer

Aggiunge i dati del tratto per un singolo tratto a un nodo di riconoscimento personalizzato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddStrokeToCustomRecognizer(
  [in]  ULONG        ulStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  IContextNode *pCustomRecognizer,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeId* \[ in\]
</dt> <dd>

Identificatore del tratto da aggiungere.

</dd> <dt>

*ulStrokePacketDataCount* \[ in\]
</dt> <dd>

Numero di pacchetti nell'oggetto Stroke.

</dd> <dt>

*plStrokePacketData* \[ in\]
</dt> <dd>

Matrice contenente i dati del pacchetto per il tratto.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ in\]
</dt> <dd>

Numero di proprietà dei pacchetti in ogni pacchetto.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ in\]
</dt> <dd>

Matrice contenente gli identificatori di proprietà del pacchetto.

</dd> <dt>

*pCustomRecognizer* \[ in\]
</dt> <dd>

[**IContextNode**](icontextnode.md) di tipo **CustomRecognizer** a cui aggiungere il tratto.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ out\]
</dt> <dd>

[**IContextNode**](icontextnode.md) a cui l'analizzatore di input penna ha aggiunto il tratto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [classi e interfacce-analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodeStrokeAddedTo* quando non è più necessario utilizzare l'oggetto.

 

Quando *ppContextNodeStrokeAddedTo* è **null**, indica che il chiamante non è interessato al valore restituito dal metodo.

[**IInkAnalyzer**](iinkanalyzer.md) aggiunge il tratto a un [**IContextNode**](icontextnode.md) di tipo **CustomRecognizer** (vedere tipi di [nodo di contesto](context-node-types.md)). Questo nodo si trova nella raccolta dei sottonodi del nodo radice (vedere [**IInkAnalyzer:: GetRootNode Method**](iinkanalyzer-getrootnode.md) e [**IContextNode:: GetSubNodes**](icontextnode-getsubnodes.md) Methods).

[**IInkAnalyzer**](iinkanalyzer.md) assegna l'identificatore delle impostazioni cultura del thread di input attivo al tratto e aggiunge il tratto al primo nodo **UnclassifiedInk** nel nodo **CustomRecognizer** . Se non esiste alcun nodo **UnclassifiedInk** , viene creato. Se il [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associato al nodo **CustomRecognizer** non supporta l'identificatore delle impostazioni cultura, il **IInkAnalyzer** continua ad analizzare e genera un avviso [**IAnalysisWarning**](ianalysiswarning.md) . Questo avviso ha un valore [**AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) di **AnalysisWarningCode \_ LanguageIdNotRespected**.

*plStrokePacketData* contiene i dati dei pacchetti per tutti i punti del tratto. *pStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (Guid) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto in ogni tratto. Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [costanti PacketPropertyGuids](packetpropertyguids-constants.md).

Questo metodo espande l'area dirty all'Unione del valore corrente dell'area e del rettangolo di delimitazione del tratto aggiunto.

[**IInkAnalyzer**](iinkanalyzer.md) restituisce un valore **HRESULT** di **E \_ INVALIDARG** nelle circostanze seguenti.

-   [**IInkAnalyzer**](iinkanalyzer.md) contiene già un tratto con lo stesso identificatore del tratto da aggiungere.
-   Il parametro *pCustomRecognizer* contiene un nodo di riconoscimento personalizzato associato a un oggetto [**IInkAnalyzer**](iinkanalyzer.md) diverso.
-   Il parametro *pCustomRecognizer* contiene un [**IContextNode**](icontextnode.md) che non è di tipo **CustomRecognizer**.

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

[Tipi di nodo di contesto](context-node-types.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Metodo IInkAnalyzer:: CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Riferimento all'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

