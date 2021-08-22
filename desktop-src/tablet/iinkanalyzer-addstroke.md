---
description: Aggiunge i dati del tratto per un singolo tratto a IInkAnalyzer e assegna l'identificatore delle impostazioni cultura del thread di input attivo al tratto.
ms.assetid: 0e603e5a-d722-4ab8-bc59-605e131c863b
title: Metodo IInkAnalyzer::AddStroke (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.AddStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: f7ba08e779e115c243918d94e5b41e8a7d77f54fab92b045274135ead2ae0264
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590591"
---
# <a name="iinkanalyzeraddstroke-method"></a>Metodo IInkAnalyzer::AddStroke

Aggiunge i dati del tratto per un singolo tratto a [**IInkAnalyzer**](iinkanalyzer.md) e assegna l'identificatore delle impostazioni cultura del thread di input attivo al tratto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT AddStroke(
  [in]  LONG         lStrokeId,
  [in]  ULONG        ulStrokePacketDataCount,
  [in]  LONG         *plStrokePacketData,
  [in]  ULONG        ulStrokePacketDescriptionCount,
  [in]  GUID         *pStrokePacketDescriptionGuids,
  [out] IContextNode **ppContextNodeStrokeAddedTo
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lStrokeId* \[ Pollici\]
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

*ppContextNodeStrokeAddedTo* \[ Cambio\]
</dt> <dd>

Puntatore a [**IContextNode a**](icontextnode.md) cui [**L'IInkAnalyzer ha**](iinkanalyzer.md) aggiunto il tratto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Per una descrizione dei valori restituiti, vedere [Classi e interfacce - Analisi input penna.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Commenti

> [!Caution]  
> Per evitare una perdita di memoria, chiamare [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) su *ppContextNodeStrokeAddedTo* quando non è più necessario usare l'oggetto .

 

Quando *ppContextNodeStrokeAddedTo* è **NULL,** indica che il chiamante non è interessato al valore restituito dal metodo.

[**IInkAnalyzer aggiunge**](iinkanalyzer.md) il tratto a un [**IContextNode**](icontextnode.md) di tipo UnclassifiedInk (vedere [Context Node Types](context-node-types.md)). Questo nodo si trova nella raccolta di sottonodi del nodo radice (vedere i metodi [**IInkAnalyzer::GetRootNode**](iinkanalyzer-getrootnode.md) e [**IContextNode::GetSubNodes).**](icontextnode-getsubnodes.md)

[**IInkAnalyzer**](iinkanalyzer.md) assegna l'identificatore delle impostazioni cultura del thread di input attivo al tratto e aggiunge il tratto al primo nodo di contesto UnclassifiedInk sotto il nodo radice dell'analizzatore input penna che contiene tratti con lo stesso identificatore di impostazioni cultura. Se l'analizzatore input penna non ha un nodo con lo stesso identificatore di impostazioni cultura, crea un nuovo nodo di contesto UnclassifiedInk sotto il relativo nodo radice e aggiunge il tratto al nuovo nodo di contesto UnclassifiedInk.

*plStrokePacketData contiene* i dati dei pacchetti per tutti i punti nel tratto. *pStrokePacketDescriptionGuids* contiene gli identificatori univoci globali (GUID) che descrivono i tipi di dati dei pacchetti inclusi per ogni punto del tratto. Per un elenco completo delle proprietà dei pacchetti disponibili, vedere [Costanti PacketPropertyGuids.](packetpropertyguids-constants.md)

Questo metodo espande l'area dirty all'unione del valore corrente dell'area e del rettangolo di selezione del tratto aggiunto.

Se [**IInkAnalyzer**](iinkanalyzer.md) contiene già un tratto con lo stesso identificatore di tratto, **IInkAnalyzer** restituisce **un valore HRESULT** **di E \_ INVALIDARG.**

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo app desktop XP Tablet PC \[ Edition\]<br/>                                                 |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                                     |
| Intestazione<br/>                   | <dl> <dt>IACom.h (richiede anche IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Inkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokeForLanguage**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokes**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**Metodo IInkAnalyzer::AddStrokesForLanguage**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**Metodo IInkAnalyzer::RemoveStroke**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**Metodo IInkAnalyzer::RemoveStrokes**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[Informazioni di riferimento per l'analisi input penna](ink-analysis-reference.md)
</dt> </dl>

 

