---
description: Il metodo GetMinIdealImageSize recupera le dimensioni minime dell'immagine ideale.
ms.assetid: f2f2d10e-ee2c-4f8a-91ce-576319038e0d
title: Metodo CBaseControlWindow. GetMinIdealImageSize (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetMinIdealImageSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24eeb4cdb5972f81e6dd66a812c9a38b61dcab91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328092"
---
# <a name="cbasecontrolwindowgetminidealimagesize-method"></a>CBaseControlWindow. GetMinIdealImageSize, metodo

Il `GetMinIdealImageSize` metodo recupera le dimensioni minime dell'immagine ideale.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetMinIdealImageSize(
   long *pWidth,
   long *pHeight
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pWidth* 
</dt> <dd>

Puntatore alla larghezza minima ideale, in pixel.

</dd> <dt>

*pHeight* 
</dt> <dd>

Puntatore all'altezza minima ideale, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore **HRESULT** .

## <a name="remarks"></a>Commenti

Vari renderer presentano limitazioni delle prestazioni sulle dimensioni delle immagini che è possibile visualizzare. Sebbene debbano ancora funzionare correttamente quando viene richiesto di visualizzare immagini di dimensioni maggiori del valore massimo specificato, i renderer possono designare le dimensioni minime e massime ideali tramite l'interfaccia [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) . Questa interfaccia può essere chiamata solo quando il grafico del filtro è in pausa o in esecuzione, perché non è fino a quel momento che le risorse vengono allocate e il renderer è in grado di riconoscere le restrizioni. Se non esistono restrizioni, il renderer inserisce i parametri *pWidth* e *pHeight* con le dimensioni video native e restituisce \_ false. Se esistono restrizioni, viene immesso l'altezza e la larghezza con restrizioni e la funzione membro restituisce S \_ OK.

Le dimensioni si applicano alle dimensioni del video di destinazione e non alle dimensioni complessive della finestra. Quindi, quando si calcolano le dimensioni della finestra da impostare, tenere conto degli stili correnti della finestra, ad esempio WS \_ Caption e WS \_ Border.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




