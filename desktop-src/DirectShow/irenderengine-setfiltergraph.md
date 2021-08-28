---
description: Il metodo SetFilterGraph specifica un grafo di filtro da usare per il motore di rendering.
ms.assetid: 6a245864-7d22-4608-995b-b28662a6ab90
title: Metodo IRenderEngine::SetFilterGraph (Qedit.h)
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
ms.openlocfilehash: 4472d1152d45ee160885a4cdbc898a55ece24b6795a9880a5eeb958e05330287
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767101"
---
# <a name="irenderenginesetfiltergraph-method"></a>Metodo IRenderEngine::SetFilterGraph

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `SetFilterGraph` metodo specifica un grafo di filtro da usare per il motore di rendering.

## <a name="syntax"></a>Sintassi


```C++
HRESULT SetFilterGraph(
   IGraphBuilder *pFG
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Pfg* 
</dt> <dd>

Puntatore [**all'interfaccia IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) del grafico dei filtri.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce uno dei valori **HRESULT** seguenti:



| Codice restituito                                                                                            | Descrizione                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Operazione completata.<br/>                            |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>           | Argomento non valido.<br/>                   |
| <dl> <dt>**E \_ DEVE \_ INIT \_ RENDERER**</dt> </dl> | Impossibile inizializzare il motore di rendering.<br/> |



 

## <a name="remarks"></a>Commenti

La maggior parte delle applicazioni non deve chiamare questo metodo. È più comune consentire al motore di rendering di compilare automaticamente il grafico chiamando il metodo [**IRenderEngine::ConnectFrontEnd.**](irenderengine-connectfrontend.md)

Questo metodo ha esito negativo se il motore di rendering ha già un grafico di filtro.

Non recuperare mai un puntatore a un grafo di filtro creato da un motore di rendering e quindi usarlo come parametro per questo metodo in un altro motore di rendering. Questa operazione causerà risultati imprevedibili.

Il **metodo ConnectFrontEnd** consente di disasciere qualsiasi grafo di filtro esistente, ma mantiene la stessa istanza di Graph Manager.

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

 

 




