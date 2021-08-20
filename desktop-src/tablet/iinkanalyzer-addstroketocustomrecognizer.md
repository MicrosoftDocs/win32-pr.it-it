---
description: Aggiunge i dati del tratto per un singolo tratto a un nodo del riconoscitore personalizzato.
ms.assetid: ab43c9f8-15fe-49db-b9d1-57d34b95d99f
title: Metodo IInkAnalyzer::AddStrokeToCustomRecognizer (IACom.h)
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
ms.openlocfilehash: 0a3ce58f462053b48e6cecdc7eb276a1e162f88b0e7de373648a537b3b712cf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967330"
---
# <a name="iinkanalyzeraddstroketocustomrecognizer-method"></a>Metodo IInkAnalyzer::AddStrokeToCustomRecognizer

Aggiunge i dati del tratto per un singolo tratto a un nodo del riconoscitore personalizzato.

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

*ulStrokeId* \[ Pollici\]
</dt> <dd>

Identificatore del tratto da aggiungere.

</dd> <dt>

*ulStrokePacketDataCount* \[ Pollici\]
</dt> <dd>

Numero di pacchetti nel tratto.

</dd> <dt>

*plStrokePacketData* \[ Pollici\]
</dt> <dd>

Matrice contenente i dati del pacchetto per il tratto.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ Pollici\]
</dt> <dd>

Numero di proprietà del pacchetto in ogni pacchetto.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ Pollici\]
</dt> <dd>

Matrice contenente gli identificatori delle proprietà del pacchetto.

</dd> <dt>

*pCustomRecognizer* \[ Pollici\]
</dt> <dd>

[**IContextNode di**](icontextnode.md) tipo **CustomRecognizer** a cui aggiungere il tratto.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ Cambio\]
</dt> <dd>

Oggetto [**IContextNode a**](icontextnode.md) cui l'analizzatore input penna ha aggiunto il tratto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodeStrokeAddedTo* quando non è più necessario usare l'oggetto .

 

Quando *ppContextNodeStrokeAddedTo* è **NULL,** indica che il chiamante non è interessato al valore restituito dal metodo.

[**IInkAnalyzer aggiunge il**](iinkanalyzer.md) tratto a un [**oggetto IContextNode**](icontextnode.md) di tipo **CustomRecognizer** (vedere [Tipi di nodi di contesto).](context-node-types.md) Questo nodo si trova nella raccolta di sottonodi del nodo radice (vedere i metodi [**IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

[**IInkAnalyzer**](iinkanalyzer.md) assegna l'identificatore delle impostazioni cultura del thread di input attivo al tratto e aggiunge il tratto al primo nodo **UnclassifiedInk** nel nodo **CustomRecognizer.** Se non **esiste alcun nodo UnclassifiedInk,** viene creato. Se [**l'oggetto IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) associato al nodo **CustomRecognizer** non supporta l'identificatore delle impostazioni cultura, **IInkAnalyzer** continua l'analisi e genera un avviso [**IAnalysisWarning.**](ianalysiswarning.md) Questo avviso ha un [**valore AnalysisWarningCode**](/windows/desktop/tablet/analysiswarningcode) di **AnalysisWarningCode \_ LanguageIdNotRespected.**

*plStrokePacketData contiene* i dati dei pacchetti per tutti i punti nel tratto. *pStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (GUID) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto in ogni tratto. Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [Costanti PacketPropertyGuids.](packetpropertyguids-constants.md)

Questo metodo espande l'area dirty all'unione del valore corrente dell'area e del rettangolo di selezione del tratto aggiunto.

[**IInkAnalyzer**](iinkanalyzer.md) restituisce **un valore HRESULT** **di E \_ INVALIDARG** nelle circostanze seguenti.

-   [**IInkAnalyzer**](iinkanalyzer.md) contiene già un tratto con lo stesso identificatore del tratto da aggiungere.
-   Il *parametro pCustomRecognizer* contiene un nodo di riconoscimento personalizzato associato a un oggetto [**IInkAnalyzer**](iinkanalyzer.md) diverso.
-   Il *parametro pCustomRecognizer* contiene un [**oggetto IContextNode**](icontextnode.md) che non è di tipo **CustomRecognizer.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[Tipi di nodi di contesto](context-node-types.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokesToCustomRecognizer**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::CreateCustomRecognizer**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

