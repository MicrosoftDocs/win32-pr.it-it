---
description: Il metodo OnReceiveMessage viene chiamato quando la finestra di dialogo riceve un messaggio.
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: Metodo CBasePropertyPage.OnReceiveMessage (Cprop.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePropertyPage.OnReceiveMessage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 833f0f7ab9192d88440afff75a36fee744ac2fe053c6fe99d1940686c452799a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158133"
---
# <a name="cbasepropertypageonreceivemessage-method"></a>Metodo CBasePropertyPage.OnReceiveMessage

Il `OnReceiveMessage` metodo viene chiamato quando la finestra di dialogo riceve un messaggio.

## <a name="syntax"></a>Sintassi


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Hwnd* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*Umsg* 
</dt> <dd>

Message.

</dd> <dt>

*wParam* 
</dt> <dd>

Primo parametro del messaggio.

</dd> <dt>

*lParam* 
</dt> <dd>

Secondo parametro del messaggio.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano. La routine della finestra di dialogo restituisce questo valore. Per altre informazioni, vedere la documentazione di Platform SDK.

## <a name="remarks"></a>Commenti

L'implementazione della classe base **chiama DefWindowProc**. Eseguire l'override di questo metodo per gestire i messaggi correlati ai controlli finestra di dialogo. Se il metodo che esegue l'override non gestisce un messaggio specifico, deve chiamare il metodo della classe base.

Se l'utente modifica le proprietà tramite i controlli finestra di dialogo, impostare il flag [**CBasePropertyPage::m \_ bDirty**](cbasepropertypage-m-bdirty.md) su **TRUE.** Chiamare quindi il **metodo IPropertyPageSite::OnStatusChange** sul puntatore [**CBasePropertyPage::m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) per informare il frame.

## <a name="examples"></a>Esempio

L'esempio seguente risponde a un clic su un pulsante aggiornando una variabile membro, che si presuppone sia definita nella classe derivata. Questo esempio mostra anche una funzione helper per impostare lo stato dirty della pagina delle proprietà.


```C++
INT_PTR CMyProp::OnReceiveMessage(HWND hwnd,
  UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_BUTTON1)
        {
            m_lNewVal = GetDlgItemInt(m_Dlg, IDC_EDIT1, 0, TRUE);
            SetDirty();
            return (INT_PTR)TRUE;
        }
        break;
    } // switch

    // Did not handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd, uMsg, wParam, lParam);
}

// Helper function to update the dirty status.
void CMyProp::SetDirty()
{
    m_bDirty = TRUE;
    if (m_pPageSite)
    {
        m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
    }
}
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>Cprop.h (include Flussi.h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase.lib (build di vendita al dettaglio); </dt> <dt>Strmbasd.lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




