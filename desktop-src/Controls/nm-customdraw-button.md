---
title: Codice di notifica di NM_CUSTOMDRAW (Button) (COMmctrl. h)
description: Notifica alla finestra padre di un controllo Button informazioni sulle operazioni di disegni personalizzate sul pulsante. Il controllo Button invia questo codice di notifica sotto forma di messaggio di \_ notifica WM.
ms.assetid: cabe5515-ba64-4c53-8746-7a0559df8989
keywords:
- NM_CUSTOMDRAW (pulsante) codice di notifica controlli Windows
topic_type:
- apiref
api_name:
- NM_CUSTOMDRAW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab3cc4eb73c3a0185131bb6ef2198458888ec89d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479426"
---
# <a name="nm_customdraw-button-notification-code"></a><span data-ttu-id="eede5-105">\_Codice di notifica CUSTOMDRAW (Button) Nm</span><span class="sxs-lookup"><span data-stu-id="eede5-105">NM\_CUSTOMDRAW (button) notification code</span></span>

<span data-ttu-id="eede5-106">Notifica alla finestra padre di un controllo Button informazioni sulle operazioni di disegni personalizzate sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="eede5-106">Notifies the parent window of a button control about custom draw operations on the button.</span></span>

<span data-ttu-id="eede5-107">Il controllo Button invia questo codice di notifica sotto forma di messaggio [**di \_ notifica WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="eede5-107">The button control sends this notification code in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CUSTOMDRAW

    lpNMCustomDraw = (LPNMCUSTOMDRAW) lParam;
```



## <a name="parameters"></a><span data-ttu-id="eede5-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eede5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eede5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eede5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="eede5-110">Puntatore a una struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) che contiene informazioni sull'operazione di disegno.</span><span class="sxs-lookup"><span data-stu-id="eede5-110">A pointer to an [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure that contains information about the drawing operation.</span></span> <span data-ttu-id="eede5-111">Il membro **dwItemSpec** di questa struttura contiene l'indice dell'elemento da disegnare e il membro **lItemlParam** di questa struttura contiene l'elemento *lParam* dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="eede5-111">The **dwItemSpec** member of this structure contains the index of the item being drawn and the **lItemlParam** member of this structure contains the item's *lParam*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eede5-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eede5-112">Return value</span></span>

<span data-ttu-id="eede5-113">Il valore che l'applicazione può restituire dipende dalla fase di disegno corrente.</span><span class="sxs-lookup"><span data-stu-id="eede5-113">The value your application can return depends on the current drawing stage.</span></span> <span data-ttu-id="eede5-114">Il membro **dwDrawStage** della struttura [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) associata include un valore che specifica la fase di disegno.</span><span class="sxs-lookup"><span data-stu-id="eede5-114">The **dwDrawStage** member of the associated [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) structure holds a value that specifies the drawing stage.</span></span> <span data-ttu-id="eede5-115">È necessario restituire uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="eede5-115">You must return one of the following values.</span></span>



| <span data-ttu-id="eede5-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="eede5-116">Return code</span></span>                                                                                          | <span data-ttu-id="eede5-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="eede5-117">Description</span></span>                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="eede5-118"><dt>**\_NOTIFYPOSTERASE CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="eede5-118"><dt>**CDRF\_NOTIFYPOSTERASE**</dt></span></span> </dl> | <span data-ttu-id="eede5-119">Il controllo invierà una notifica al padre dopo la cancellazione di un elemento.</span><span class="sxs-lookup"><span data-stu-id="eede5-119">The control will notify the parent after erasing an item.</span></span> <span data-ttu-id="eede5-120">Questa operazione può essere utilizzata solo se **dwDrawStage** è uguale a CDDS \_ preerase.</span><span class="sxs-lookup"><span data-stu-id="eede5-120">This can be used only if **dwDrawStage** equals CDDS\_PREERASE.</span></span><br/>                                  |
| <dl> <span data-ttu-id="eede5-121"><dt>**\_NOTIFYPOSTPAINT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="eede5-121"><dt>**CDRF\_NOTIFYPOSTPAINT**</dt></span></span> </dl> | <span data-ttu-id="eede5-122">Il controllo invierà una notifica al padre dopo aver disegnato un elemento.</span><span class="sxs-lookup"><span data-stu-id="eede5-122">The control will notify the parent after painting an item.</span></span> <span data-ttu-id="eede5-123">Può essere usato solo se **dwDrawStage** è uguale a CDDS \_ PrePaint.</span><span class="sxs-lookup"><span data-stu-id="eede5-123">This can be used only if **dwDrawStage** equals CDDS\_PREPAINT.</span></span><br/>                                 |
| <dl> <span data-ttu-id="eede5-124"><dt>**\_SKIPDEFAULT CDRF**</dt></span><span class="sxs-lookup"><span data-stu-id="eede5-124"><dt>**CDRF\_SKIPDEFAULT**</dt></span></span> </dl>     | <span data-ttu-id="eede5-125">L'applicazione ha disegnato manualmente l'elemento.</span><span class="sxs-lookup"><span data-stu-id="eede5-125">The application drew the item manually.</span></span> <span data-ttu-id="eede5-126">L'elemento non viene disegnato dal controllo.</span><span class="sxs-lookup"><span data-stu-id="eede5-126">The control will not draw the item.</span></span> <span data-ttu-id="eede5-127">Questa operazione può essere usata quando **dwDrawStage** è uguale a CDDS \_ PREerase o CDDS \_ nonpaint.</span><span class="sxs-lookup"><span data-stu-id="eede5-127">This can be used when **dwDrawStage** equals CDDS\_PREERASE or CDDS\_PREPAINT.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eede5-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="eede5-128">Remarks</span></span>

<span data-ttu-id="eede5-129">Se il controllo Button è contrassegnato come OwnerDraw (BS \_ OwnerDraw), il \_ codice di notifica CUSTOMDRAW nm non viene inviato.</span><span class="sxs-lookup"><span data-stu-id="eede5-129">If the button control is marked ownerdraw (BS\_OWNERDRAW), the NM\_CUSTOMDRAW notification code is not sent.</span></span>

<span data-ttu-id="eede5-130">Per ulteriori informazioni, vedere [utilizzo del progetto personalizzato](custom-draw.md) .</span><span class="sxs-lookup"><span data-stu-id="eede5-130">See [Using Custom Draw](custom-draw.md) for further discussion.</span></span>

> [!Note]  
> <span data-ttu-id="eede5-131">Per usare questo codice di notifica, è necessario fornire un manifesto che specifichi Comclt32.dll versione 6,0.</span><span class="sxs-lookup"><span data-stu-id="eede5-131">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="eede5-132">Per altre informazioni sui manifesti, vedere [Abilitazione degli stili di visualizzazione](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eede5-132">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="eede5-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eede5-133">Requirements</span></span>



| <span data-ttu-id="eede5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="eede5-134">Requirement</span></span> | <span data-ttu-id="eede5-135">Valore</span><span class="sxs-lookup"><span data-stu-id="eede5-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eede5-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eede5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="eede5-137">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="eede5-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="eede5-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="eede5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="eede5-139">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="eede5-139">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="eede5-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eede5-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="eede5-141"><dt>Commctrl. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eede5-141"><dt>Commctrl.h (include Windows.h)</dt></span></span> </dl> |



 

 





