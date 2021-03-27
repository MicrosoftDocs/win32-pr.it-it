---
description: Il \_ messaggio WM PALETTEISCHANGING informa le applicazioni che un'applicazione sta per realizzare la relativa tavolozza logica.
ms.assetid: 64ec1042-0ab5-496f-9a88-2f293b412704
title: Messaggio WM_PALETTEISCHANGING (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa2127dc9c682bba1fc4cea4e10b2b96ecc92102
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757877"
---
# <a name="wm_paletteischanging-message"></a><span data-ttu-id="7298a-103">\_Messaggio PALETTEISCHANGING WM</span><span class="sxs-lookup"><span data-stu-id="7298a-103">WM\_PALETTEISCHANGING message</span></span>

<span data-ttu-id="7298a-104">Il messaggio **WM \_ PALETTEISCHANGING** informa le applicazioni che un'applicazione sta per realizzare la relativa tavolozza logica.</span><span class="sxs-lookup"><span data-stu-id="7298a-104">The **WM\_PALETTEISCHANGING** message informs applications that an application is going to realize its logical palette.</span></span>

<span data-ttu-id="7298a-105">Una finestra riceve questo messaggio tramite la funzione [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7298a-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a><span data-ttu-id="7298a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7298a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7298a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7298a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7298a-108">Handle per la finestra che renderà conto della tavolozza logica.</span><span class="sxs-lookup"><span data-stu-id="7298a-108">A handle to the window that is going to realize its logical palette.</span></span>

</dd> <dt>

<span data-ttu-id="7298a-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7298a-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7298a-110">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="7298a-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7298a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7298a-111">Return value</span></span>

<span data-ttu-id="7298a-112">Se un'applicazione elabora il messaggio, deve restituire zero.</span><span class="sxs-lookup"><span data-stu-id="7298a-112">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="7298a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7298a-113">Remarks</span></span>

<span data-ttu-id="7298a-114">L'applicazione che modifica la tavolozza non attende il riconoscimento del messaggio prima di modificare la tavolozza e di inviare il messaggio [**WM \_ PALETTECHANGED**](wm-palettechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="7298a-114">The application changing its palette does not wait for acknowledgment of this message before changing the palette and sending the [**WM\_PALETTECHANGED**](wm-palettechanged.md) message.</span></span> <span data-ttu-id="7298a-115">Di conseguenza, è possibile che la tavolozza sia già stata modificata dal momento in cui un'applicazione riceve il messaggio.</span><span class="sxs-lookup"><span data-stu-id="7298a-115">As a result, the palette may already be changed by the time an application receives this message.</span></span>

<span data-ttu-id="7298a-116">Se l'applicazione ignora o non riesce a elaborare il messaggio e una seconda applicazione ne realizza la tavolozza mentre la prima utilizza gli indici della tavolozza, è possibile che l'utente visualizzi colori imprevisti durante le successive operazioni di disegno.</span><span class="sxs-lookup"><span data-stu-id="7298a-116">If the application either ignores or fails to process this message and a second application realizes its palette while the first is using palette indexes, there is a strong possibility that the user will see unexpected colors during subsequent drawing operations.</span></span>

## <a name="requirements"></a><span data-ttu-id="7298a-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7298a-117">Requirements</span></span>



| <span data-ttu-id="7298a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7298a-118">Requirement</span></span> | <span data-ttu-id="7298a-119">Valore</span><span class="sxs-lookup"><span data-stu-id="7298a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7298a-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7298a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7298a-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7298a-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7298a-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7298a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7298a-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7298a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7298a-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7298a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7298a-125"><dt>Winuser. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7298a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7298a-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7298a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7298a-127">Panoramica sui colori</span><span class="sxs-lookup"><span data-stu-id="7298a-127">Colors Overview</span></span>](colors.md)
</dt> <dt>

[<span data-ttu-id="7298a-128">Messaggi colori</span><span class="sxs-lookup"><span data-stu-id="7298a-128">Color Messages</span></span>](color-messages.md)
</dt> <dt>

[<span data-ttu-id="7298a-129">**\_PALETTECHANGED WM**</span><span class="sxs-lookup"><span data-stu-id="7298a-129">**WM\_PALETTECHANGED**</span></span>](wm-palettechanged.md)
</dt> <dt>

[<span data-ttu-id="7298a-130">**\_QUERYNEWPALETTE WM**</span><span class="sxs-lookup"><span data-stu-id="7298a-130">**WM\_QUERYNEWPALETTE**</span></span>](wm-querynewpalette.md)
</dt> </dl>

 

 
