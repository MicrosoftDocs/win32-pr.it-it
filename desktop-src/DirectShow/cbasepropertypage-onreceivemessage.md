---
description: Il metodo OnReceiveMessage viene chiamato quando la finestra di dialogo riceve un messaggio.
ms.assetid: ea93500d-fd0f-4820-a54a-a186c40899ad
title: Metodo CBasePropertyPage. OnReceiveMessage (Cprop. h)
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
ms.openlocfilehash: 69d9da708d45524d15f735273d47f242104ee22f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325195"
---
# <a name="cbasepropertypageonreceivemessage-method"></a>CBasePropertyPage. OnReceiveMessage, metodo

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

*HWND* 
</dt> <dd>

Handle per la finestra.

</dd> <dt>

*uMsg* 
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

Restituisce un valore booleano. La routine della finestra di dialogo restituisce questo valore. Per ulteriori informazioni, vedere la documentazione di Platform SDK.

## <a name="remarks"></a>Commenti

L'implementazione della classe di base chiama **DefWindowProc**. Eseguire l'override di questo metodo per gestire i messaggi correlati ai controlli della finestra di dialogo. Se il metodo che esegue l'override non gestisce un messaggio specifico, deve chiamare il metodo della classe base.

Se l'utente modifica le proprietà tramite i controlli della finestra di dialogo, impostare il flag [**CBasePropertyPage:: m \_ BDirty**](cbasepropertypage-m-bdirty.md) su **true**. Chiamare quindi il metodo **IPropertyPageSite:: OnStatusChange** sul puntatore [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) per informare il frame.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene risposto a un clic del pulsante aggiornando una variabile membro che si presuppone venga definita nella classe derivata. Questo esempio mostra anche una funzione helper per impostare lo stato dirty della pagina delle proprietà.


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
| Intestazione<br/>  | <dl> <dt>Cprop. h (include Streams. h)</dt> </dl>                                                                                     |
| Libreria<br/> | <dl> <dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Classe CBasePropertyPage**](cbasepropertypage.md)
</dt> </dl>

 

 




