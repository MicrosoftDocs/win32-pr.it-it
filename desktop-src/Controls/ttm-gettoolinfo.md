---
title: Messaggio TTM_GETTOOLINFO (COMmctrl. h)
description: Recupera le informazioni che un controllo ToolTip gestisce su uno strumento.
ms.assetid: b94d3b78-2437-4c60-ba46-b3f57cf9c876
keywords:
- Controlli di Windows Message TTM_GETTOOLINFO
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
ms.openlocfilehash: cc0de37b97be3bec495c8777b2ddd1cc6fc1bd42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119806"
---
# <a name="ttm_gettoolinfo-message"></a>\_Messaggio TTM GETTOOLINFO

Recupera le informazioni che un controllo ToolTip gestisce su uno strumento.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>Deve essere zero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) . Quando si invia il messaggio, i membri **HWND** e **UID** identificano uno strumento e il membro **cbSize** deve specificare le dimensioni della struttura. Quando si usa questo messaggio per recuperare il testo della descrizione comando, verificare che il membro **lpszText** della struttura **TOOLINFO** punti a un buffer valido di dimensione adquate

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce **true** se l'operazione ha esito positivo o **false** in caso contrario.

## <a name="remarks"></a>Commenti

Se il controllo ToolTip include lo strumento, la struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) riceve informazioni sullo strumento.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene riposizionato un controllo ToolTip.


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
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomi Unicode e ANSI<br/>   | **TTM \_ GETTOOLINFOW** (Unicode) e **TTM \_ GETTOOLINFOA** (ANSI)<br/>           |



 

 





