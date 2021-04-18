---
description: Passaggio 7.
ms.assetid: 12bb1288-e764-4bc1-bea5-196e17cf3557
title: Passaggio 7. Gestire i messaggi della finestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd1c44dd65a4f9f430b4223f0a5a0e4763af981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316314"
---
# <a name="step-7-handle-window-messages"></a>Passaggio 7. Gestire i messaggi della finestra

Eseguire l'override del metodo [**CBasePropertyPage:: OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) per aggiornare i controlli della finestra di dialogo in risposta all'input dell'utente. Se non si gestisce un messaggio specifico, chiamare il metodo **OnReceiveMessage** sulla classe padre. Ogni volta che l'utente modifica una proprietà, eseguire le operazioni seguenti:

-   Impostare la variabile **m \_ bDirty** della pagina delle proprietà su **true**.
-   Chiamare il metodo **IPropertyPageSite:: OnStatusChange** del frame della proprietà con il \_ flag PROPPAGESTATUS Dirty. Questo flag informa il frame della proprietà che deve abilitare il pulsante **applica** . Il membro [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) include un puntatore all'interfaccia **IPropertyPageSite** .

Per semplificare questo passaggio, è possibile aggiungere la funzione helper seguente alla pagina delle proprietà:


```C++
private:
    void SetDirty()
    {
        m_bDirty = TRUE;
        if (m_pPageSite)
        {
            m_pPageSite->OnStatusChange(PROPPAGESTATUS_DIRTY);
        }
    }
```



Chiamare questo metodo privato all'interno di **OnReceiveMessage** ogni volta che un'azione utente modifica una proprietà, come illustrato nell'esempio seguente:


```C++
BOOL CGrayProp::OnReceiveMessage(HWND hwnd,
    UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
    case WM_COMMAND:
        if (LOWORD(wParam) == IDC_DEFAULT)
        {
            // User clicked the 'Revert to Default' button.
            m_lNewVal = SATURATION_DEFAULT;
            m_pGray->SetSaturation(m_lNewVal);

            // Update the slider control.
            SendDlgItemMessage(m_Dlg, IDC_SLIDER1, TBM_SETPOS, 1,
                m_lNewVal);
            SetDirty();
            return (LRESULT) 1;
        }
        break;

    case WM_HSCROLL:
        {
            // User moved the slider.
            switch(LOWORD(wParam))
            {
            case TB_PAGEDOWN:
            case SB_THUMBTRACK:
            case TB_PAGEUP:
                m_lNewVal = SendDlgItemMessage(m_Dlg, IDC_SLIDER1,
                    TBM_GETPOS, 0, 0);
                m_pGray->SetSaturation(m_lNewVal);
                SetDirty();
            }
            return (LRESULT) 1;
        }
    } // Switch.
    
    // Let the parent class handle the message.
    return CBasePropertyPage::OnReceiveMessage(hwnd,uMsg,wParam,lParam);
} 
```



La pagina delle proprietà in questo esempio ha due controlli, una barra di scorrimento e un pulsante **Ripristina impostazioni predefinite** . Se l'utente scorre la barra del dispositivo di scorrimento, nella pagina delle proprietà viene impostato il valore di saturazione sul filtro. Se l'utente fa clic sul pulsante, la pagina delle proprietà ripristina il valore di saturazione predefinito del filtro. In ogni caso, m \_ lNewVal include il valore corrente e m \_ LVAL include il valore originale. Il valore di m \_ LVAL non viene aggiornato fino a quando l'utente non esegue il commit della modifica, operazione che viene eseguita quando l'utente fa clic sul pulsante **OK** o **applica** nel frame della proprietà.

[Passaggio 8: Applicare le modifiche alle proprietà](step-8--apply-property-changes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione di una pagina delle proprietà del filtro](creating-a-filter-property-page.md)
</dt> </dl>

 

 



