---
description: Il metodo GetBorderColour recupera il colore del bordo della finestra corrente, m \_ BorderColour.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Metodo CBaseControlWindow.GetBorderColour (Ctlutil.h)
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
ms.openlocfilehash: 9b5b94e0fa58c95e74fd140c04710e8aaacef9402397fa475983c0e01e586528
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017369"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a>Metodo CBaseControlWindow.GetBorderColour

Il `GetBorderColour` metodo recupera il colore del bordo della finestra corrente, m **\_ BorderColour.**

## <a name="syntax"></a>Sintassi


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce il colore del bordo.

## <a name="remarks"></a>Commenti

Un'applicazione può impostare un rettangolo di destinazione per visualizzare il video. Questo rettangolo deve essere relativo all'area client per la finestra. Se questa operazione viene eseguita (per impostazione predefinita viene sempre disegnata l'intera finestra), è presente un'area che circonda il video. cio, il bordo. Il colore del bordo può essere impostato tramite la funzione membro [**CBaseControlWindow::p ut \_ BorderColor.**](cbasecontrolwindow-put-bordercolor.md) Questa proprietà influisce sul colore del bordo. Usare questa funzione membro anziché [**CBaseControlWindow::get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), a meno che non venga chiamato esternamente tramite il metodo [**IVideoWindow::get \_ BorderColor.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Ctlutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




