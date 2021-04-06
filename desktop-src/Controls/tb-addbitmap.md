---
title: Messaggio TB_ADDBITMAP (COMmctrl. h)
description: Aggiunge una o più immagini all'elenco di immagini dei pulsanti disponibili per una barra degli strumenti.
ms.assetid: 9040ab84-a5f3-4e4b-bc90-590b2ceeaa5a
keywords:
- Controlli di Windows Message TB_ADDBITMAP
topic_type:
- apiref
api_name:
- TB_ADDBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d83cba4b4dec9b490a3e8f41db9cc7721dd23b08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743970"
---
# <a name="tb_addbitmap-message"></a><span data-ttu-id="5b806-104">TB \_ ADDBITMAP messaggio</span><span class="sxs-lookup"><span data-stu-id="5b806-104">TB\_ADDBITMAP message</span></span>

<span data-ttu-id="5b806-105">Aggiunge una o più immagini all'elenco di immagini dei pulsanti disponibili per una barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="5b806-105">Adds one or more images to the list of button images available for a toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="5b806-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5b806-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b806-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5b806-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b806-108">Numero di immagini di pulsanti nella bitmap.</span><span class="sxs-lookup"><span data-stu-id="5b806-108">Number of button images in the bitmap.</span></span> <span data-ttu-id="5b806-109">Se *lParam* specifica una bitmap definita dal sistema, questo parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="5b806-109">If *lParam* specifies a system-defined bitmap, this parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="5b806-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5b806-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5b806-111">Puntatore a una struttura [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) che contiene l'identificatore di una risorsa bitmap e l'handle per l'istanza del modulo con il file eseguibile che contiene la risorsa bitmap.</span><span class="sxs-lookup"><span data-stu-id="5b806-111">Pointer to a [**TBADDBITMAP**](/windows/win32/api/commctrl/ns-commctrl-tbaddbitmap) structure that contains the identifier of a bitmap resource and the handle to the module instance with the executable file that contains the bitmap resource.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b806-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5b806-112">Return value</span></span>

<span data-ttu-id="5b806-113">Restituisce l'indice della prima nuova immagine, se ha esito positivo, oppure-1 in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="5b806-113">Returns the index of the first new image if successful, or -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b806-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5b806-114">Remarks</span></span>

<span data-ttu-id="5b806-115">Se la barra degli strumenti è stata creata utilizzando la funzione [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , è necessario inviare il messaggio [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) alla barra degli strumenti prima di inviare **TB \_ ADDBITMAP**.</span><span class="sxs-lookup"><span data-stu-id="5b806-115">If the toolbar was created using the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function, you must send the [**TB\_BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) message to the toolbar before sending **TB\_ADDBITMAP**.</span></span>

## <a name="examples"></a><span data-ttu-id="5b806-116">Esempio</span><span class="sxs-lookup"><span data-stu-id="5b806-116">Examples</span></span>

<span data-ttu-id="5b806-117">Nell'esempio seguente viene creata una bitmap da una risorsa (IDB \_ bitmap1), viene eseguito il mapping del colore di sfondo (nero in questo caso) al colore della superficie del pulsante di sistema e viene aggiunto alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="5b806-117">The following example creates a bitmap from a resource (IDB\_BITMAP1), maps the background color (black in this case) to the system button face color, and adds it to the toolbar.</span></span>


```C++
DWORD backgroundColor = GetSysColor(COLOR_BTNFACE);
COLORMAP colorMap;
colorMap.from = RGB(0, 0, 0);
colorMap.to = backgroundColor;
HBITMAP hbm = CreateMappedBitmap(g_hInst, IDB_BITMAP1, 0, &colorMap, 1);
TBADDBITMAP tb;
tb.hInst = NULL;
tb.nID = (UINT_PTR)hbm;

// hWndToolbar is the window handle of the toolbar.
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was 
// created by using CreateWindowEx.
int index = SendMessage (hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tb);
```



## <a name="requirements"></a><span data-ttu-id="5b806-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5b806-118">Requirements</span></span>



| <span data-ttu-id="5b806-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b806-119">Requirement</span></span> | <span data-ttu-id="5b806-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5b806-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b806-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b806-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5b806-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5b806-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5b806-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5b806-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5b806-124">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="5b806-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5b806-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5b806-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b806-126"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b806-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

