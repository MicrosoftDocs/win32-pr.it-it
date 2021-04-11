---
title: Funzione di callback TranslateDispatch
description: Utilizzato dal client della funzione DoReaderMode per intercettare e gestire in modo esplicito tutti i messaggi di Windows di destinazione per l'area di scorrimento della finestra modalità lettore. Si tratta di una funzione di callback definita dall'applicazione.
ms.assetid: a50cff4f-ae10-4c3c-a386-9ec7c7d6256f
keywords:
- Controlli Windows per la funzione di callback TranslateDispatch
topic_type:
- apiref
api_name:
- TranslateDispatch
- PFNREADERTRANSLATEDISPATCH
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1230ed1e65f8d739f9a0a05e4788eb919c45c4cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964109"
---
# <a name="translatedispatch-callback-function"></a><span data-ttu-id="d39dc-105">Funzione di callback TranslateDispatch</span><span class="sxs-lookup"><span data-stu-id="d39dc-105">TranslateDispatch callback function</span></span>

<span data-ttu-id="d39dc-106">\[*TranslateDispatch* è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti.</span><span class="sxs-lookup"><span data-stu-id="d39dc-106">\[*TranslateDispatch* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d39dc-107">È possibile che in versioni successive sia stata modificata o non sia più disponibile.\]</span><span class="sxs-lookup"><span data-stu-id="d39dc-107">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="d39dc-108">Utilizzato dal client della funzione [**DoReaderMode**](doreadermode.md) per intercettare e gestire in modo esplicito tutti i messaggi di Windows di destinazione per l'area di scorrimento della finestra modalità lettore.</span><span class="sxs-lookup"><span data-stu-id="d39dc-108">Used by the client of the [**DoReaderMode**](doreadermode.md) function to intercept and explicitly handle any windows messages targeted for the scrolling area of the reader mode window.</span></span> <span data-ttu-id="d39dc-109">Si tratta di una funzione di callback definita dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d39dc-109">This is an application-defined callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="d39dc-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d39dc-110">Syntax</span></span>


```C++
BOOL CALLBACK TranslateDispatch(
  _In_ const MSG *lpmsg
);
```



## <a name="parameters"></a><span data-ttu-id="d39dc-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="d39dc-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d39dc-112">*lpMsg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d39dc-112">*lpmsg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d39dc-113">Tipo: \**const [**msg**](/windows/win32/api/winuser/ns-winuser-msg) \** _</span><span class="sxs-lookup"><span data-stu-id="d39dc-113">Type: \**const [**MSG**](/windows/win32/api/winuser/ns-winuser-msg)\** _</span></span>

<span data-ttu-id="d39dc-114">Puntatore a una struttura [_ *msg* \*](/windows/win32/api/winuser/ns-winuser-msg) che contiene il messaggio intercettato.</span><span class="sxs-lookup"><span data-stu-id="d39dc-114">A pointer to an [_ *MSG*\*](/windows/win32/api/winuser/ns-winuser-msg) structure that contains the intercepted message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d39dc-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d39dc-115">Return value</span></span>

<span data-ttu-id="d39dc-116">Tipo: **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="d39dc-116">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="d39dc-117">**True** se il messaggio è stato gestito da questa funzione; in caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="d39dc-117">**TRUE** if the message was handled by this function; otherwise, **FALSE**.</span></span> <span data-ttu-id="d39dc-118">Se **false**, il messaggio viene gestito dall'implementazione della modalità Reader predefinita.</span><span class="sxs-lookup"><span data-stu-id="d39dc-118">If **FALSE**, the message is handled by the default reader mode implementation.</span></span> <span data-ttu-id="d39dc-119">Tale implementazione gestisce lo spostamento e i pulsanti del mouse, nonché le pressioni dei tasti.</span><span class="sxs-lookup"><span data-stu-id="d39dc-119">That implementation handles mouse movement and buttons as well as key presses.</span></span>

## <a name="examples"></a><span data-ttu-id="d39dc-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="d39dc-120">Examples</span></span>

<span data-ttu-id="d39dc-121">Nell'esempio seguente viene illustrata un'implementazione di questa funzione.</span><span class="sxs-lookup"><span data-stu-id="d39dc-121">The following example outlines an implementation of this function.</span></span>


```C++
BOOL CALLBACK
TranslateDispatchCallback(LPMSG lpmsg)
{
    BOOL fResult = FALSE;

    if (lpmsg->message == WM_KEYDOWN)
    {
        
        // Perform custom keyboard actions here.
        fResult = TRUE;
    }

    return fResult;
}
```



## <a name="requirements"></a><span data-ttu-id="d39dc-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d39dc-122">Requirements</span></span>



| <span data-ttu-id="d39dc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d39dc-123">Requirement</span></span> | <span data-ttu-id="d39dc-124">Valore</span><span class="sxs-lookup"><span data-stu-id="d39dc-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d39dc-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d39dc-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d39dc-126">Windows Vista, \[ solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d39dc-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d39dc-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d39dc-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d39dc-128">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d39dc-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

