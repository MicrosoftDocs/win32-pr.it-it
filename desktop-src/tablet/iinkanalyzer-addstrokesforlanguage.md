---
description: Aggiunge i dati del tratto per più tratti a IInkAnalyzer e assegna l'identificatore delle impostazioni cultura specificato ai tratti.
ms.assetid: 1274b24f-204b-4a84-a7c0-0205b6068ae8
title: Metodo IInkAnalyzer::AddStrokesForLanguage (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStrokesForLanguage
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 52e2dc742dc91b37bce29d477cf91f7178f2ae2a62ce3a329d2b9bf79c46b33a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719609"
---
# <a name="iinkanalyzeraddstrokesforlanguage-method"></a>Metodo IInkAnalyzer::AddStrokesForLanguage

Aggiunge i dati del tratto per più tratti a [**IInkAnalyzer**](iinkanalyzer.md) e assegna l'identificatore delle impostazioni cultura specificato ai tratti.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddStrokesForLanguage(
  [in]  ULONG        ulStrokeIdsCount,
  [in]  LONG         *plIdofStrokesToAdd,
  [in]  LONG         lStrokesLCID,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [in]  ULONG        *pulPacketDataCountPerStroke,
  [in]  LONG         *plStrokePacketData,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ulStrokeIdsCount* \[ Pollici\]
</dt> <dd>

Numero di tratti da aggiungere.

</dd> <dt>

*plIdofStrokesToAdd* \[ Pollici\]
</dt> <dd>

Matrice contenente gli identificatori dei tratti.

</dd> <dt>

*lStrokesLCID* \[ Pollici\]
</dt> <dd>

Valore che rappresenta l'identificatore delle impostazioni cultura da assegnare ai tratti.

</dd> <dt>

*ulStrokePacketDescriptionCount* \[ Pollici\]
</dt> <dd>

Numero di proprietà in ogni pacchetto.

</dd> <dt>

*pStrokePacketDescriptionGuids* \[ Pollici\]
</dt> <dd>

Matrice contenente gli identificatori di proprietà del pacchetto.

</dd> <dt>

*pulPacketDataCountPerStroke* \[ Pollici\]
</dt> <dd>

Matrice contenente il numero di pacchetti in ogni tratto.

</dd> <dt>

*plStrokePacketData* \[ Pollici\]
</dt> <dd>

Matrice contenente i dati del pacchetto per i tratti.

</dd> <dt>

*ppContextNodeStrokeAddedTo* \[ Cambio\]
</dt> <dd>

[**IContextNode a**](icontextnode.md) cui l'analizzatore input penna ha aggiunto i tratti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodeStrokeAddedTo* quando non è più necessario usare l'oggetto .

 

Quando *ppContextNodeStrokeAddedTo* è **NULL,** indica che il chiamante non è interessato al valore restituito dal metodo.

[**IInkAnalyzer aggiunge**](iinkanalyzer.md) i tratti a un [**oggetto IContextNode**](icontextnode.md) di tipo UnclassifiedInk (vedere [Tipi di nodo di contesto).](context-node-types.md) Questo nodo si trova nella raccolta di sottonodi del nodo radice (vedere i [**metodi IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

[**IInkAnalyzer**](iinkanalyzer.md) assegna l'identificatore delle impostazioni cultura *lStrokeLCID* ai tratti e aggiunge i tratti al primo nodo di contesto UnclassifiedInk nel nodo radice dell'analizzatore input penna che contiene tratti con lo stesso identificatore delle impostazioni cultura. Se l'analizzatore input penna non ha un nodo con lo stesso identificatore delle impostazioni cultura, crea un nuovo nodo di contesto UnclassifiedInk sotto il nodo radice e aggiunge i tratti al nuovo nodo di contesto UnclassifiedInk.

*plStrokePacketData contiene* i dati dei pacchetti per tutti i tratti. *pStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (GUID) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto in ogni tratto. Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [Costanti PacketPropertyGuids](packetpropertyguids-constants.md).

> [!Note]  
> Solo i tratti con le stesse descrizioni dei pacchetti possono essere aggiunti in una singola chiamata al metodo [**IInkAnalyzer::AddStrokes**](iinkanalyzer-addstrokes.md).

 

Questo metodo espande l'area dirty all'unione del valore corrente dell'area e del rettangolo di selezione dei tratti aggiunti.

Se [**IInkAnalyzer**](iinkanalyzer.md) contiene già un tratto con lo stesso identificatore di uno dei tratti da aggiungere, **IInkAnalyzer** restituisce **un HRESULT** **di E \_ INVALIDARG**.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop tablet PC Edition \[ XP\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStroke**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::RemoveStroke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer::RemoveStrokes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi dell'input penna](ink-analysis-reference.md)
</dt> </dl>

 

