---
description: Il metodo GetFilterGraph Recupera il grafico di filtro creato dal motore di rendering, se disponibile.
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: 'Metodo IRenderEngine:: GetFilterGraph (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4c4750e6127c0d57758e46b2309f4d91afc110e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324416"
---
# <a name="irenderenginegetfiltergraph-method"></a>Metodo IRenderEngine:: GetFilterGraph

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `GetFilterGraph` metodo recupera il grafico di filtro creato dal motore di rendering, se disponibile.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppFG* \[ out\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del grafico dei filtri. Riceve il valore **null** se non è presente alcun grafico di filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                            | Descrizione                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Esito positivo.<br/>                            |
| <dl> <dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt> </dl> | Impossibile inizializzare il motore di rendering.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>              | Puntatore non valido.<br/>                    |



 

## <a name="remarks"></a>Commenti

Usare il metodo [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) per compilare il front-end del grafico del filtro. Per l'anteprima, usare [**IRenderEngine:: RenderOutputPins**](irenderengine-renderoutputpins.md) per completare il grafo. Per l'output del file, connettere il front-end a una combinazione di MUX/file writer. Per ulteriori informazioni, vedere [rendering di un progetto](rendering-a-project.md).

Il grafico risultante può essere eseguito, sospeso, arrestato e cercato; Tuttavia, non è possibile modificare la velocità di riproduzione.

In caso di restituzione, se il valore di *\* ppFG* è diverso da **null**, l'interfaccia **IGraphBuilder** include un conteggio dei riferimenti in attesa. Assicurarsi di rilasciare l'interfaccia al termine dell'utilizzo.

> [!Note]  
> Il file di intestazione qedit. h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere qedit. h, scaricare l' [aggiornamento Microsoft Windows SDK per Windows Vista e .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h non è disponibile nel Microsoft Windows SDK per Windows 7 e .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




