---
description: Il metodo GetClassWindowStyles recupera gli stili di classe e di finestra della finestra.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Metodo CBaseWindow.GetClassWindowStyles (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.GetClassWindowStyles
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba7042069d4f1190a88b25ea4cc349e8230c149dd61d2d06fc91fa3439a9e55f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074631"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a>Metodo CBaseWindow.GetClassWindowStyles

Il `GetClassWindowStyles` metodo recupera gli stili della classe della finestra e gli stili della finestra.

## <a name="syntax"></a>Sintassi


```C++
virtual LPTSTR GetClassWindowStyles(
   DWORD *pClassStyles,
   DWORD *pWindowStyles,
   DWORD *pWindowStylesEx
) = 0;
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pClassStyles* 
</dt> <dd>

Puntatore a una variabile che riceve gli stili della classe.

</dd> <dt>

*pWindowStyles* 
</dt> <dd>

Puntatore a una variabile che riceve gli stili della finestra.

</dd> <dt>

*pWindowStylesEx* 
</dt> <dd>

Puntatore a una variabile che riceve gli stili di finestra estesi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una stringa di testo statico che contiene il nome della classe.

## <a name="remarks"></a>Commenti

Il [**metodo CBaseWindow::P repareWindow**](cbasewindow-preparewindow.md) chiama questo metodo per recuperare gli stili di classe e gli stili della finestra della finestra.

Questo metodo è virtuale puro. la classe derivata deve implementarla. L'esempio seguente illustra una possibile implementazione:


```C++
LPTSTR CMyWindowClass::GetClassWindowStyles(DWORD *pClassStyles,
                                            DWORD *pWindowStyles,
                                            DWORD *pWindowStylesEx)
{
    *pClassStyles = CS_HREDRAW | CS_VREDRAW;
    *pWindowStyles = WS_OVERLAPPEDWINDOW | WS_CLIPCHILDREN;
    *pWindowStylesEx = WS_EX_WINDOWEDGE;
    return TEXT("MyWindowClass");
}
```



L'oggetto usa lo stile di classe per il membro **lpszClassName** di una struttura WNDCLASS, che passa alla **funzione RegisterClass.** L'oggetto usa gli stili della finestra *per i parametri dwExStyle* *e dwStyle* della **funzione CreateWindowEx.** Per altre informazioni, vedere Platform SDK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Winutil.h (includere Flussi.h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




