---
title: Funzione di callback ReaderScroll
description: Funzione di callback definita dall'applicazione utilizzata quando il puntatore del mouse viene spostato all'interno della parte della finestra della modalità Reader dichiarata come area di scorrimento attiva.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- Controlli Windows per la funzione di callback ReaderScroll
topic_type:
- apiref
api_name:
- ReaderScroll
- PFNREADERSCROLL
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0db5a80b84a30362e3bdbce45fe7485ad0dd6884
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964157"
---
# <a name="readerscroll-callback-function"></a><span data-ttu-id="97c15-104">Funzione di callback ReaderScroll</span><span class="sxs-lookup"><span data-stu-id="97c15-104">ReaderScroll callback function</span></span>

<span data-ttu-id="97c15-105">\[*ReaderScroll* è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="97c15-105">\[*ReaderScroll* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="97c15-106">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="97c15-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="97c15-107">Funzione di callback definita dall'applicazione utilizzata quando il puntatore del mouse viene spostato all'interno della parte della finestra della modalità Reader dichiarata come area di scorrimento attiva.</span><span class="sxs-lookup"><span data-stu-id="97c15-107">An application-defined callback function used when the mouse pointer is moved within the portion of the reader mode window that has been declared as the active scrolling area.</span></span>

## <a name="syntax"></a><span data-ttu-id="97c15-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97c15-108">Syntax</span></span>


```C++
BOOL CALLBACK ReaderScroll(
  _In_ PREADERMODEINFO prmi,
  _In_ int             dx,
  _In_ int             dy
);
```



## <a name="parameters"></a><span data-ttu-id="97c15-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="97c15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97c15-110">*prmi* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97c15-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c15-111">Tipo: **PREADERMODEINFO**</span><span class="sxs-lookup"><span data-stu-id="97c15-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="97c15-112">Puntatore alla struttura [**READERMODEINFO**](readermodeinfo.md) passata alla funzione [**DoReaderMode**](doreadermode.md) .</span><span class="sxs-lookup"><span data-stu-id="97c15-112">A pointer to the [**READERMODEINFO**](readermodeinfo.md) structure that was passed to the [**DoReaderMode**](doreadermode.md) function.</span></span> <span data-ttu-id="97c15-113">Questa struttura definisce la finestra modalità lettore e l'area di scorrimento attiva.</span><span class="sxs-lookup"><span data-stu-id="97c15-113">This structure defines the reader mode window and the active scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="97c15-114">*dx* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97c15-114">*dx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c15-115">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="97c15-115">Type: **int**</span></span>

<span data-ttu-id="97c15-116">Distanza per scorrere orizzontalmente.</span><span class="sxs-lookup"><span data-stu-id="97c15-116">The distance to scroll horizontally.</span></span> <span data-ttu-id="97c15-117">Se il \_ flag RMF VERTICALONLY è impostato nella struttura [**READERMODEINFO**](readermodeinfo.md) , questo valore è sempre 0.</span><span class="sxs-lookup"><span data-stu-id="97c15-117">If the RMF\_VERTICALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> <dt>

<span data-ttu-id="97c15-118">*dy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97c15-118">*dy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97c15-119">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="97c15-119">Type: **int**</span></span>

<span data-ttu-id="97c15-120">Distanza di scorrimento verticale.</span><span class="sxs-lookup"><span data-stu-id="97c15-120">The distance to scroll vertically.</span></span> <span data-ttu-id="97c15-121">Se il \_ flag RMF HORIZONTALONLY è impostato nella struttura [**READERMODEINFO**](readermodeinfo.md) , questo valore è sempre 0.</span><span class="sxs-lookup"><span data-stu-id="97c15-121">If the RMF\_HORIZONTALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97c15-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97c15-122">Return value</span></span>

<span data-ttu-id="97c15-123">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="97c15-123">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="97c15-124">Questa funzione deve sempre restituire **true**.</span><span class="sxs-lookup"><span data-stu-id="97c15-124">This function should always return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="97c15-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="97c15-125">Remarks</span></span>

<span data-ttu-id="97c15-126">Quando l'applicazione riceve la notifica da questa funzione, l'applicazione è responsabile dello scorrimento della finestra modalità lettore nella direzione specificata dai parametri *dx* e *dy* .</span><span class="sxs-lookup"><span data-stu-id="97c15-126">When the application receives notification from this function, the application is responsible for scrolling the reader mode window in the direction specified by the *dx* and *dy* parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="97c15-127">Esempio</span><span class="sxs-lookup"><span data-stu-id="97c15-127">Examples</span></span>

<span data-ttu-id="97c15-128">Nell'esempio seguente viene illustrata un'implementazione di questa funzione utilizzando una funzione personalizzata per eseguire lo scorrimento.</span><span class="sxs-lookup"><span data-stu-id="97c15-128">The following example outlines an implementation of this function using a custom function to accomplish the scrolling.</span></span>


```C++
BOOL CALLBACK
ReaderScrollCallback(PREADERMODEINFO prmi, int dx, int dy)
{
    if (prmi == NULL) 
        return FALSE;

    // Call custom ScrollWindow method to scroll the window
    ScrollWindow(prmi->hwnd, dx, dy);
    
    return TRUE;
}
```



## <a name="requirements"></a><span data-ttu-id="97c15-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97c15-129">Requirements</span></span>



| <span data-ttu-id="97c15-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="97c15-130">Requirement</span></span> | <span data-ttu-id="97c15-131">Valore</span><span class="sxs-lookup"><span data-stu-id="97c15-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="97c15-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97c15-132">Minimum supported client</span></span><br/> | <span data-ttu-id="97c15-133">Windows Vista, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97c15-133">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="97c15-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97c15-134">Minimum supported server</span></span><br/> | <span data-ttu-id="97c15-135">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="97c15-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

