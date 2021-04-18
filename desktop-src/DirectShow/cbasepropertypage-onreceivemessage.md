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
# <a name="cbasepropertypageonreceivemessage-method"></a><span data-ttu-id="d9160-103">CBasePropertyPage. OnReceiveMessage, metodo</span><span class="sxs-lookup"><span data-stu-id="d9160-103">CBasePropertyPage.OnReceiveMessage method</span></span>

<span data-ttu-id="d9160-104">Il `OnReceiveMessage` metodo viene chiamato quando la finestra di dialogo riceve un messaggio.</span><span class="sxs-lookup"><span data-stu-id="d9160-104">The `OnReceiveMessage` method is called when the dialog box receives a message.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9160-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9160-105">Syntax</span></span>


```C++
virtual INT_PTR OnReceiveMessage(
   HWND   hwnd,
   UINT   uMsg,
   WPARAM wParam,
   LPARAM lParam
);
```



## <a name="parameters"></a><span data-ttu-id="d9160-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d9160-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9160-107">*HWND*</span><span class="sxs-lookup"><span data-stu-id="d9160-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d9160-108">Handle per la finestra.</span><span class="sxs-lookup"><span data-stu-id="d9160-108">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="d9160-109">*uMsg*</span><span class="sxs-lookup"><span data-stu-id="d9160-109">*uMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="d9160-110">Message.</span><span class="sxs-lookup"><span data-stu-id="d9160-110">Message.</span></span>

</dd> <dt>

<span data-ttu-id="d9160-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d9160-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9160-112">Primo parametro del messaggio.</span><span class="sxs-lookup"><span data-stu-id="d9160-112">First message parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d9160-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d9160-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d9160-114">Secondo parametro del messaggio.</span><span class="sxs-lookup"><span data-stu-id="d9160-114">Second message parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9160-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d9160-115">Return value</span></span>

<span data-ttu-id="d9160-116">Restituisce un valore booleano.</span><span class="sxs-lookup"><span data-stu-id="d9160-116">Returns a Boolean value.</span></span> <span data-ttu-id="d9160-117">La routine della finestra di dialogo restituisce questo valore. Per ulteriori informazioni, vedere la documentazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="d9160-117">The dialog procedure returns this value; for more information, see the Platform SDK documentation.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9160-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9160-118">Remarks</span></span>

<span data-ttu-id="d9160-119">L'implementazione della classe di base chiama **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="d9160-119">The base-class implementation calls **DefWindowProc**.</span></span> <span data-ttu-id="d9160-120">Eseguire l'override di questo metodo per gestire i messaggi correlati ai controlli della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="d9160-120">Override this method to handle messages that relate to the dialog controls.</span></span> <span data-ttu-id="d9160-121">Se il metodo che esegue l'override non gestisce un messaggio specifico, deve chiamare il metodo della classe base.</span><span class="sxs-lookup"><span data-stu-id="d9160-121">If the overriding method does not handle a particular message, it should call the base-class method.</span></span>

<span data-ttu-id="d9160-122">Se l'utente modifica le proprietà tramite i controlli della finestra di dialogo, impostare il flag [**CBasePropertyPage:: m \_ BDirty**](cbasepropertypage-m-bdirty.md) su **true**.</span><span class="sxs-lookup"><span data-stu-id="d9160-122">If the user changes any properties via the dialog controls, set the [**CBasePropertyPage::m\_bDirty**](cbasepropertypage-m-bdirty.md) flag to **TRUE**.</span></span> <span data-ttu-id="d9160-123">Chiamare quindi il metodo **IPropertyPageSite:: OnStatusChange** sul puntatore [**CBasePropertyPage:: m \_ pPageSite**](cbasepropertypage-m-ppagesite.md) per informare il frame.</span><span class="sxs-lookup"><span data-stu-id="d9160-123">Then call the **IPropertyPageSite::OnStatusChange** method on the [**CBasePropertyPage::m\_pPageSite**](cbasepropertypage-m-ppagesite.md) pointer to inform the frame.</span></span>

## <a name="examples"></a><span data-ttu-id="d9160-124">Esempio</span><span class="sxs-lookup"><span data-stu-id="d9160-124">Examples</span></span>

<span data-ttu-id="d9160-125">Nell'esempio seguente viene risposto a un clic del pulsante aggiornando una variabile membro che si presuppone venga definita nella classe derivata.</span><span class="sxs-lookup"><span data-stu-id="d9160-125">The following example responds to a button click by updating a member variable, which is assumed to be defined in the derived class.</span></span> <span data-ttu-id="d9160-126">Questo esempio mostra anche una funzione helper per impostare lo stato dirty della pagina delle proprietà.</span><span class="sxs-lookup"><span data-stu-id="d9160-126">This example also shows a helper function for setting the property page's dirty status.</span></span>


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



## <a name="requirements"></a><span data-ttu-id="d9160-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9160-127">Requirements</span></span>



| <span data-ttu-id="d9160-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9160-128">Requirement</span></span> | <span data-ttu-id="d9160-129">Valore</span><span class="sxs-lookup"><span data-stu-id="d9160-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9160-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9160-130">Header</span></span><br/>  | <dl> <span data-ttu-id="d9160-131"><dt>Cprop. h (include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9160-131"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="d9160-132">Libreria</span><span class="sxs-lookup"><span data-stu-id="d9160-132">Library</span></span><br/> | <dl> <span data-ttu-id="d9160-133"><dt>Strmbase. lib (compilazioni finali); </dt> <dt>Strmbasd. lib (build di debug)</dt></span><span class="sxs-lookup"><span data-stu-id="d9160-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9160-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9160-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9160-135">**Classe CBasePropertyPage**</span><span class="sxs-lookup"><span data-stu-id="d9160-135">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




