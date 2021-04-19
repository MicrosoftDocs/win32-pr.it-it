---
description: 'Il metodo WaitForReceiveToComplete attende il completamento del metodo CBaseRenderer:: Receive.'
ms.assetid: 3c722680-e54b-4ba1-8e98-36647cd027bc
title: Metodo CBaseRenderer. WaitForReceiveToComplete (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForReceiveToComplete
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9033474c71d23fed106205839071bad200df6a23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324197"
---
# <a name="cbaserendererwaitforreceivetocomplete-method"></a>CBaseRenderer. WaitForReceiveToComplete, metodo

Il `WaitForReceiveToComplete` metodo attende il completamento del metodo [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) .

## <a name="syntax"></a>Sintassi


```C++
void WaitForReceiveToComplete();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

I metodi [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) e [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) chiamano questo metodo per sincronizzare la modifica dello stato con il metodo **Receive** .

In particolare, questo metodo invia i messaggi mentre è in attesa che il flag [**\_ BInReceive di CBaseRenderer:: m**](cbaserenderer-m-binreceive.md) diventi **false**. Il flag diventa **true** nel metodo [**CBaseRenderer::P reparereceive**](cbaserenderer-preparereceive.md) e ritorna a **false** dopo che il metodo **Receive** chiama il metodo [**CBaseRenderer::P reparerender**](cbaserenderer-preparerender.md) . La classe derivata può utilizzare **PrepareRender** per impostare la tavolozza. In attesa del completamento di **PrepareRender** si garantisce che i messaggi di modifica della tavolozza vengano inviati prima che si verifichi la modifica dello stato. In questo modo si evita un potenziale deadlock.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Renbase. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseRenderer**](cbaserenderer.md)
</dt> </dl>

 

 




