---
description: Il metodo GetBorderColour Recupera il colore del bordo della finestra corrente, m \_ BorderColour.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Metodo CBaseControlWindow. GetBorderColour (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329267"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a>CBaseControlWindow. GetBorderColour, metodo

Il `GetBorderColour` metodo recupera il colore del bordo della finestra corrente, **m \_ BorderColour**.

## <a name="syntax"></a>Sintassi


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il colore del bordo.

## <a name="remarks"></a>Commenti

Un'applicazione può impostare un rettangolo di destinazione per visualizzare il video. Questo rettangolo deve essere relativo all'area client per la finestra. Se questa operazione viene eseguita (l'impostazione predefinita consiste nel disegnare sempre l'intera finestra), esiste un'area che racchiude il video; ovvero il bordo. Il colore del bordo può essere impostato tramite la funzione membro [**CBaseControlWindow::p UT \_ BorderColor**](cbasecontrolwindow-put-bordercolor.md) . Questa proprietà influiscono sul colore del bordo. Usare questa funzione membro anziché [**CBaseControlWindow:: Get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), a meno che non si chiami esternamente tramite il metodo [**IVideoWindow:: Get \_ BorderColor**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




