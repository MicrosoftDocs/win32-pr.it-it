---
description: La struttura MXDC \_ S0PAGE \_ PassThrough \_ escape \_ t è una \_ \_ \_ struttura di escape t MXDC concatenata a una struttura MXDC \_ S0PAGE \_ data \_ t.
ms.assetid: 949c1ed4-92d5-4c11-a7da-f9d94bafe3f8
title: Struttura MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 7c1a8370d2cfa1ada9fda2d2d99b9fe500b79d31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346486"
---
# <a name="mxdc_s0page_passthrough_escape_t-structure"></a><span data-ttu-id="2adb2-103">\_Struttura MXDC S0PAGE \_ PassThrough \_ escape \_ T</span><span class="sxs-lookup"><span data-stu-id="2adb2-103">MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T structure</span></span>

<span data-ttu-id="2adb2-104">La struttura **MXDC \_ S0PAGE \_ PassThrough \_ escape \_ t** è una struttura di [**\_ escape \_ \_ t MXDC**](mxdcescapeheader.md) concatenata a una struttura [**MXDC \_ S0PAGE \_ data \_ t**](mxdcs0pagedata.md) .</span><span class="sxs-lookup"><span data-stu-id="2adb2-104">The **MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_S0PAGE\_DATA\_T**](mxdcs0pagedata.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="2adb2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2adb2-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PagePassthroughEscape {
  MXDC_ESCAPE_HEADER_T mxdcEscape;
  MXDC_S0PAGE_DATA_T   xpsS0PageData;
} MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T, *P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="2adb2-106">Members</span><span class="sxs-lookup"><span data-stu-id="2adb2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2adb2-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="2adb2-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="2adb2-108">Una struttura [**MXDC dell' \_ intestazione di escape \_ \_ T**](mxdcescapeheader.md) con il relativo membro **OpCode** impostato su **MXDCOP \_ impostare \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="2adb2-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to **MXDCOP\_SET\_S0PAGE**.</span></span>

</dd> <dt>

<span data-ttu-id="2adb2-109">**xpsS0PageData**</span><span class="sxs-lookup"><span data-stu-id="2adb2-109">**xpsS0PageData**</span></span>
</dt> <dd>

<span data-ttu-id="2adb2-110">Struttura [**MxdcS0PageData**](mxdcs0pagedata.md) che rappresenta una pagina XPS-Document.</span><span class="sxs-lookup"><span data-stu-id="2adb2-110">An [**MxdcS0PageData**](mxdcs0pagedata.md) structure that represents an XPS-document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2adb2-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="2adb2-111">Remarks</span></span>

<span data-ttu-id="2adb2-112">Questa struttura viene passata nel parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando viene chiamata con l'escape di [**\_ escape MXDC**](mxdc-escape.md) e il membro **OpCode** della struttura dell' [**intestazione di \_ escape \_ MXDC \_ T**](mxdcescapeheader.md) è **MXDCOP \_ set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="2adb2-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE**.</span></span> <span data-ttu-id="2adb2-113">Il risultato è che il convertitore di documenti XML Microsoft (MXDC) passa la pagina alla stampante senza elaborarla.</span><span class="sxs-lookup"><span data-stu-id="2adb2-113">The result is that the Microsoft XML Document Converter (MXDC) passes the page through to the printer without processing it.</span></span>

<span data-ttu-id="2adb2-114">Allocare memoria per l'escape come illustrato di seguito, impostare i campi in base alle esigenze e quindi chiamare [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="2adb2-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_S0PAGE_PASSTHROUGH_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="2adb2-115">La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere compresa tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="2adb2-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="2adb2-116">L'applicazione chiamante è responsabile della convalida del codice XML della pagina del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="2adb2-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="2adb2-117">Il consumo di flussi è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ impostare la \_ \_ risorsa S0PAGE** come **OpCode** per ogni risorsa nella pagina prima di chiamarla con **MXDCOP \_ set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="2adb2-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2adb2-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2adb2-118">Requirements</span></span>



| <span data-ttu-id="2adb2-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="2adb2-119">Requirement</span></span> | <span data-ttu-id="2adb2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="2adb2-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2adb2-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2adb2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="2adb2-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2adb2-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2adb2-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2adb2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="2adb2-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2adb2-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2adb2-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2adb2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="2adb2-126"><dt>MXDC. h</dt></span><span class="sxs-lookup"><span data-stu-id="2adb2-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2adb2-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2adb2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2adb2-128">Stampa</span><span class="sxs-lookup"><span data-stu-id="2adb2-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2adb2-129">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="2adb2-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="2adb2-130">[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2adb2-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="2adb2-131">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="2adb2-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="2adb2-132">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="2adb2-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

