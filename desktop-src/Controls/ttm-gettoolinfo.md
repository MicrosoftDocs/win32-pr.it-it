---
title: TTM_GETTOOLINFO messaggio (Commctrl.h)
description: Recupera le informazioni mantenute da un controllo descrizione comando su uno strumento.
ms.assetid: b94d3b78-2437-4c60-ba46-b3f57cf9c876
keywords:
- TTM_GETTOOLINFO dei messaggi Windows controllo
topic_type:
- apiref
api_name:
- TTM_GETTOOLINFO
- TTM_GETTOOLINFOA
- TTM_GETTOOLINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77f19243603ab5d2ba62d498a5595528e39b33658c7a8e4aa0638888806684ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166374"
---
# <a name="ttm_gettoolinfo-message"></a>TTM \_ GETTOOLINFO message

Recupera le informazioni mantenute da un controllo descrizione comando su uno strumento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una [**struttura TOOLINFO.**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) Quando si invia il messaggio, i **membri hwnd** e **uId** identificano uno strumento e il membro **cbSize** deve specificare le dimensioni della struttura. Quando si usa questo messaggio per recuperare il testo della descrizione comando, assicurarsi che il membro **lpszText** della struttura **TOOLINFO** punti a un buffer valido di dimensioni adquate

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **TRUE in** caso di esito positivo oppure FALSE **in** caso contrario.

## <a name="remarks"></a>Commenti

Se il controllo descrizione comando include lo strumento, la [**struttura TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) riceve informazioni sullo strumento.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene riposizionato un controllo descrizione comando.


```C++
HRESULT MyToolTipClass::OffsetTooltip(int xOffset, int yOffset)  
{  
    HRESULT hr = S_OK;   
    DWORD   dwError = 0;  
  
    if (NULL != m_hWndToolTip)  
    {  
        TOOLINFO ti = {0};  
  
        ti.cbSize = sizeof(TOOLINFO);  
        ti.hwnd   = m_hWndToolTipOwner;  
  
        // Get the current tooltip definition.          
        if( SendMessage(m_hWndToolTip, TTM_GETTOOLINFO, 0, (LPARAM)&ti))  
        {  
            // Offset the tooltip rectangle as specified.              
            OffsetRect(&ti.rect, xOffset, yOffset);  
  
            // Apply the new rectangle to the tooltip.
            SendMessage(m_hWndToolTip, TTM_NEWTOOLRECT, 0, (LPARAM)&ti);  
        }  
        else  
        {  
            dwError = GetLastError();  
            hr = HRESULT_FROM_WIN32(dwError);  
            MyErrorHandler(hr);
       }  
    }  
    return hr;  
}  
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ GETTOOLINFOW** (Unicode) e **TTM \_ GETTOOLINFOA** (ANSI)<br/>           |



 

 





