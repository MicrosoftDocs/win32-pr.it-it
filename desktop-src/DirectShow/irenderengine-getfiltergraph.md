---
description: Il metodo GetFilterGraph recupera il grafico di filtro costruito dal motore di rendering, se presente.
ms.assetid: 509b2c9c-c21b-4855-880f-f09ad342e758
title: Metodo IRenderEngine::GetFilterGraph (Qedit.h)
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
ms.openlocfilehash: 8208d886cd23dab797a9f89d3c050c9f46eff60c8cdd78c27c89dae7396c557a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397582"
---
# <a name="irenderenginegetfiltergraph-method"></a>Metodo IRenderEngine::GetFilterGraph

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future di Windows.\]

 

Il `GetFilterGraph` metodo recupera il grafico di filtro costruito dal motore di rendering, se presente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetFilterGraph(
  [out] IGraphBuilder **ppFG
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ppFG* \[ Cambio\]
</dt> <dd>

Riceve un puntatore all'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del grafico filtri. Riceve il valore **NULL** se non è presente alcun grafico di filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                                            | Descrizione                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione completata.<br/>                            |
| <dl> <dt>**E \_ DEVE \_ INIT \_ RENDERER**</dt> </dl> | Impossibile inizializzare il motore di rendering.<br/> |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>              | Puntatore non valido.<br/>                    |



 

## <a name="remarks"></a>Commenti

Usare il [**metodo IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) per compilare il front-end del grafico dei filtri. Per l'anteprima, [**usare IRenderEngine::RenderOutputPins**](irenderengine-renderoutputpins.md) per completare il grafico. Per l'output del file, connettere il front-end a una combinazione mux/writer di file. Per altre informazioni, vedere [Rendering di un Project](rendering-a-project.md).

Il grafo risultante può essere eseguito, sospeso, arrestato e cercato; La velocità di riproduzione non può tuttavia essere modificata.

In caso di restituzione, se il valore di *\* ppFG* è diverso da **NULL,** **l'interfaccia IGraphBuilder** ha un conteggio dei riferimenti in sospeso. Assicurarsi di rilasciare l'interfaccia al termine dell'uso.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IRenderEngine**](irenderengine.md)
</dt> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> </dl>

 

 




