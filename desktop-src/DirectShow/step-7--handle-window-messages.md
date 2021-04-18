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
# <a name="step-7-handle-window-messages"></a><span data-ttu-id="636db-104">Passaggio 7.</span><span class="sxs-lookup"><span data-stu-id="636db-104">Step 7.</span></span> <span data-ttu-id="636db-105">Gestire i messaggi della finestra</span><span class="sxs-lookup"><span data-stu-id="636db-105">Handle Window Messages</span></span>

<span data-ttu-id="636db-106">Eseguire l'override del metodo [**CBasePropertyPage:: OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) per aggiornare i controlli della finestra di dialogo in risposta all'input dell'utente.</span><span class="sxs-lookup"><span data-stu-id="636db-106">Override the [**CBasePropertyPage::OnReceiveMessage**](cbasepropertypage-onreceivemessage.md) method to update the dialog controls in response to user input.</span></span> <span data-ttu-id="636db-107">Se non si gestisce un messaggio specifico, chiamare il metodo **OnReceiveMessage** sulla classe padre.</span><span class="sxs-lookup"><span data-stu-id="636db-107">If you don't handle a particular message, call the **OnReceiveMessage** method on the parent class.</span></span> <span data-ttu-id="636db-108">Ogni volta che l'utente modifica una proprietà, eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="636db-108">Whenever the user changes a property, do the following:</span></span>

-   <span data-ttu-id="636db-109">Impostare la variabile **m \_ bDirty** della pagina delle proprietà su **true**.</span><span class="sxs-lookup"><span data-stu-id="636db-109">Set the **m\_bDirty** variable of the property page to **TRUE**.</span></span>
-   <span data-ttu-id="636db-110">Chiamare il metodo **IPropertyPageSite:: OnStatusChange** del frame della proprietà con il \_ flag PROPPAGESTATUS Dirty.</span><span class="sxs-lookup"><span data-stu-id="636db-110">Call the **IPropertyPageSite::OnStatusChange** method of the property frame with the PROPPAGESTATUS\_DIRTY flag.</span></span> <span data-ttu-id="636db-111">Questo flag informa il frame della proprietà che deve abilitare il pulsante **applica** .</span><span class="sxs-lookup"><span data-stu-id="636db-111">This flag informs the property frame that it should enable the **Apply** button.</span></span> <span data-ttu-id="636db-112">Il membro [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) include un puntatore all'interfaccia **IPropertyPageSite** .</span><span class="sxs-lookup"><span data-stu-id="636db-112">The [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) member holds a pointer to the **IPropertyPageSite** interface.</span></span>

<span data-ttu-id="636db-113">Per semplificare questo passaggio, è possibile aggiungere la funzione helper seguente alla pagina delle proprietà:</span><span class="sxs-lookup"><span data-stu-id="636db-113">To simplify this step, you can add the following helper function to your property page:</span></span>


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



<span data-ttu-id="636db-114">Chiamare questo metodo privato all'interno di **OnReceiveMessage** ogni volta che un'azione utente modifica una proprietà, come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="636db-114">Call this private method inside **OnReceiveMessage** whenever a user action changes a property, as shown in the following example:</span></span>


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



<span data-ttu-id="636db-115">La pagina delle proprietà in questo esempio ha due controlli, una barra di scorrimento e un pulsante **Ripristina impostazioni predefinite** .</span><span class="sxs-lookup"><span data-stu-id="636db-115">The property page in this example has two controls, a slider bar and a **Revert to Default** button.</span></span> <span data-ttu-id="636db-116">Se l'utente scorre la barra del dispositivo di scorrimento, nella pagina delle proprietà viene impostato il valore di saturazione sul filtro.</span><span class="sxs-lookup"><span data-stu-id="636db-116">If the user scrolls the slider bar, the property page sets the saturation value on the filter.</span></span> <span data-ttu-id="636db-117">Se l'utente fa clic sul pulsante, la pagina delle proprietà ripristina il valore di saturazione predefinito del filtro.</span><span class="sxs-lookup"><span data-stu-id="636db-117">If the user clicks the button, the property page restores the filter's default saturation value.</span></span> <span data-ttu-id="636db-118">In ogni caso, m \_ lNewVal include il valore corrente e m \_ LVAL include il valore originale.</span><span class="sxs-lookup"><span data-stu-id="636db-118">In each case, m\_lNewVal holds the current value and m\_lVal holds the original value.</span></span> <span data-ttu-id="636db-119">Il valore di m \_ LVAL non viene aggiornato fino a quando l'utente non esegue il commit della modifica, operazione che viene eseguita quando l'utente fa clic sul pulsante **OK** o **applica** nel frame della proprietà.</span><span class="sxs-lookup"><span data-stu-id="636db-119">The value of m\_lVal is not updated until the user commits the change, which happens when the user clicks the **OK** or **Apply** button on the property frame.</span></span>

<span data-ttu-id="636db-120">[Passaggio 8: Applicare le modifiche alle proprietà](step-8--apply-property-changes.md).</span><span class="sxs-lookup"><span data-stu-id="636db-120">Next: [Step 8. Apply Property Changes](step-8--apply-property-changes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="636db-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="636db-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="636db-122">Creazione di una pagina delle proprietà del filtro</span><span class="sxs-lookup"><span data-stu-id="636db-122">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> </dl>

 

 



