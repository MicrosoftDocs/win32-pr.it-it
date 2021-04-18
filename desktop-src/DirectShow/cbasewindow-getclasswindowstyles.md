---
description: Il metodo GetClassWindowStyles recupera gli stili della classe e gli stili della finestra.
ms.assetid: 6eec7912-c654-4e4f-b6f1-ec94c7284575
title: Metodo CBaseWindow. GetClassWindowStyles (Winutil. h)
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
ms.openlocfilehash: a34332f84a91ee88d61ee5f29f0b6a0b0cc44714
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327946"
---
# <a name="cbasewindowgetclasswindowstyles-method"></a>CBaseWindow. GetClassWindowStyles, metodo

Il `GetClassWindowStyles` metodo recupera gli stili della classe e gli stili della finestra.

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

Puntatore a una variabile che riceve gli stili della finestra estesa.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una stringa di testo statica che contiene il nome della classe.

## <a name="remarks"></a>Commenti

Il metodo [**CBaseWindow::P reparewindow**](cbasewindow-preparewindow.md) chiama questo metodo per recuperare gli stili della classe e gli stili della finestra della finestra.

Questo metodo è virtuale puro; la classe derivata deve implementarla. Nell'esempio seguente viene illustrata una possibile implementazione:


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



L'oggetto usa lo stile della classe per il membro **lpszClassName** di una struttura WNDCLASS, che passa alla funzione **registerClass** . L'oggetto utilizza gli stili della finestra per i parametri *dwExStyle* e *DwStyle* della funzione **CreateWindowEx** . Per ulteriori informazioni, vedere Platform SDK.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>WinUtil. h (include Streams. h)</dt> </dl>                                                                                   |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




