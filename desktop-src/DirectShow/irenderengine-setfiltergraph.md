---
description: Il metodo SetFilterGraph specifica un grafico di filtro per il motore di rendering da usare.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: 'Metodo IRenderEngine:: SetFilterGraph (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetFilterGraph
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 72c93ef6610fd301c497589858a8941e2b8f71b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333581"
---
# <a name="irenderenginesetfiltergraph-method"></a>Metodo IRenderEngine:: SetFilterGraph

> [!Note]  
> \[Deprecato. Questa API può essere rimossa dalle versioni successive di Windows.\]

 

Il `SetFilterGraph` metodo specifica un grafico di filtro per il motore di rendering da usare.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pFG* 
</dt> <dd>

Puntatore all'interfaccia [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del grafico del filtro.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei seguenti valori **HRESULT** :



| Codice restituito                                                                                            | Descrizione                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                   | Esito positivo.<br/>                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Argomento non valido.<br/>                   |
| <dl> <dt>**E \_ deve \_ inizializzare il \_ RENDERER**</dt> </dl> | Impossibile inizializzare il motore di rendering.<br/> |



 

## <a name="remarks"></a>Commenti

Per la maggior parte delle applicazioni non è necessario chiamare questo metodo. È più tipico consentire al motore di rendering di compilare il grafo, chiamando il metodo [**IRenderEngine:: ConnectFrontEnd**](irenderengine-connectfrontend.md) .

Questo metodo ha esito negativo se il motore di rendering dispone già di un grafico a filtro.

Non recuperare mai un puntatore a un grafico di filtro creato da un motore di rendering e quindi usarlo come parametro per questo metodo su un altro motore di rendering. Questa operazione causerà risultati imprevedibili.

Il metodo **ConnectFrontEnd** rimuove qualsiasi grafico filtro esistente, ma mantiene la stessa istanza del gestore del grafico del filtro.

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

 

 




