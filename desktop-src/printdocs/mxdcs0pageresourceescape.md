---
description: La struttura MXDC \_ S0PAGE \_ Resource \_ escape \_ t è una \_ \_ \_ struttura di escape t MXDC concatenata a una struttura della \_ \_ \_ risorsa \_ t S0PAGE XPS MXDC.
ms.assetid: e5caa280-f0a5-4a89-b4f1-4f195a537dc6
title: Struttura MXDC_S0PAGE_RESOURCE_ESCAPE_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_RESOURCE_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: ed1d78aad1ede2a318dcde2d3a2d39fd8e666ddc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227464"
---
# <a name="mxdc_s0page_resource_escape_t-structure"></a><span data-ttu-id="b3978-103">MXDC \_ S0PAGE \_ risorsa \_ escape \_ T struttura</span><span class="sxs-lookup"><span data-stu-id="b3978-103">MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T structure</span></span>

<span data-ttu-id="b3978-104">La struttura **MXDC \_ S0PAGE \_ Resource \_ escape \_ t** è una struttura di [**\_ escape \_ \_ t MXDC**](mxdcescapeheader.md) concatenata a una struttura della [**\_ \_ \_ risorsa \_ t S0PAGE XPS MXDC**](mxdcxpss0pageresource.md) .</span><span class="sxs-lookup"><span data-stu-id="b3978-104">The **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with an [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3978-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b3978-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageResourceEscape {
  MXDC_ESCAPE_HEADER_T       mxdcEscape;
  MXDC_XPS_S0PAGE_RESOURCE_T xpsS0PageResourcePassthrough;
} MXDC_S0PAGE_RESOURCE_ESCAPE_T, *P_MXDC_S0PAGE_RESOURCE_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="b3978-106">Members</span><span class="sxs-lookup"><span data-stu-id="b3978-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b3978-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="b3978-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="b3978-108">Una struttura [**MXDC dell' \_ intestazione di escape \_ \_ T**](mxdcescapeheader.md) con il membro **OpCode** impostato su MXDCOP \_ imposta la \_ risorsa S0PAGE \_ .</span><span class="sxs-lookup"><span data-stu-id="b3978-108">An [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_SET\_S0PAGE\_RESOURCE.</span></span>

</dd> <dt>

<span data-ttu-id="b3978-109">**xpsS0PageResourcePassthrough**</span><span class="sxs-lookup"><span data-stu-id="b3978-109">**xpsS0PageResourcePassthrough**</span></span>
</dt> <dd>

<span data-ttu-id="b3978-110">Una struttura della [**\_ \_ \_ risorsa \_ T MXDC XPS S0PAGE**](mxdcxpss0pageresource.md) che rappresenta una risorsa, ad esempio un tipo di carattere o un file di immagine, in una pagina del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="b3978-110">An [**MXDC\_XPS\_S0PAGE\_RESOURCE\_T**](mxdcxpss0pageresource.md) structure representing a resource, such as a font or image file, on an XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b3978-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="b3978-111">Remarks</span></span>

<span data-ttu-id="b3978-112">Questa struttura viene passata nel parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando tale funzione viene chiamata con l'escape di [**\_ escape MXDC**](mxdc-escape.md) e il membro **OpCode** della struttura dell' [**intestazione di \_ escape \_ MXDC \_ T**](mxdcescapeheader.md) è **MXDCOP \_ set \_ S0PAGE \_ Resource**.</span><span class="sxs-lookup"><span data-stu-id="b3978-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape, and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_SET\_S0PAGE\_RESOURCE**.</span></span> <span data-ttu-id="b3978-113">Il risultato è una risorsa di pagina da inviare a MXDC.</span><span class="sxs-lookup"><span data-stu-id="b3978-113">The result is a page resource to send to the MXDC.</span></span>

<span data-ttu-id="b3978-114">Allocare memoria per l'escape come illustrato di seguito, impostare i campi in base alle esigenze e quindi chiamare [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="b3978-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_S0PAGE_RESOURCE_ESCAPE_T) + 
                        iS0PageResourceDataSize - 1;

// Allocate the memory buffer.
P_MXDC_S0PAGE_RESOURCE_ESCAPE_T pS0PageResourceEscapeData = 
                        (P_MXDC_S0PAGE_RESOURCE_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="b3978-115">La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere compresa tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); Tuttavia, può essere presente più di una di queste chiamate tra le chiamate a **Startpage** e **EndPage**.</span><span class="sxs-lookup"><span data-stu-id="b3978-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however, there can be more than one of these calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="b3978-116">Il consumo di flussi è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ set \_ S0PAGE \_ Resource** **OpCode** per ogni risorsa nella pagina prima di chiamare **ExtEscape** con il **codice operativo** MXDCOP **\_ set \_ S0PAGE**.  </span><span class="sxs-lookup"><span data-stu-id="b3978-116">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE**  **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3978-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b3978-117">Requirements</span></span>



| <span data-ttu-id="b3978-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3978-118">Requirement</span></span> | <span data-ttu-id="b3978-119">Valore</span><span class="sxs-lookup"><span data-stu-id="b3978-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b3978-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3978-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b3978-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3978-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b3978-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b3978-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b3978-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3978-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b3978-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b3978-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3978-125"><dt>MXDC. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3978-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3978-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b3978-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3978-127">Stampa</span><span class="sxs-lookup"><span data-stu-id="b3978-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b3978-128">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="b3978-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="b3978-129">[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b3978-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b3978-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="b3978-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="b3978-131">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="b3978-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

