---
description: La struttura MXDC di \_ \_ escape PrintTicket \_ t è una \_ struttura di intestazione di escape MXDC \_ \_ t concatenata a una struttura di \_ \_ data t PrintTicket MXDC \_ .
ms.assetid: 79b4f830-3e3f-4c6f-9e61-98e8bf6e2824
title: Struttura MXDC_PRINTTICKET_ESCAPE_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_ESCAPE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 158ee2038c83b74077d00e6922b2c7050b76bc62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318360"
---
# <a name="mxdc_printticket_escape_t-structure"></a><span data-ttu-id="87832-103">\_ \_ Struttura T di escape PRINTTICKET MXDC \_</span><span class="sxs-lookup"><span data-stu-id="87832-103">MXDC\_PRINTTICKET\_ESCAPE\_T structure</span></span>

<span data-ttu-id="87832-104">La struttura **MXDC di \_ \_ escape PrintTicket \_ t** è una struttura di [**intestazione di escape MXDC \_ \_ \_ t**](mxdcescapeheader.md) concatenata a una struttura di [**\_ \_ data \_ t PrintTicket MXDC**](mxdcprintticketpassthrough.md) .</span><span class="sxs-lookup"><span data-stu-id="87832-104">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure concatenated with a [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="87832-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="87832-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketEscape {
  MXDC_ESCAPE_HEADER_T    mxdcEscape;
  MXDC_PRINTTICKET_DATA_T printTicketData;
} MXDC_PRINTTICKET_ESCAPE_T, *P_MXDC_PRINTTICKET_ESCAPE_T;
```



## <a name="members"></a><span data-ttu-id="87832-106">Members</span><span class="sxs-lookup"><span data-stu-id="87832-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="87832-107">**mxdcEscape**</span><span class="sxs-lookup"><span data-stu-id="87832-107">**mxdcEscape**</span></span>
</dt> <dd>

<span data-ttu-id="87832-108">Una struttura [**MXDC dell' \_ intestazione di escape \_ \_ T**](mxdcescapeheader.md) con il membro **OpCode** impostato \_ sulla \_ pagina fissa MXDCOP PrintTicket \_ , MXDCOP \_ PrintTicket \_ fixed \_ doc o MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq.</span><span class="sxs-lookup"><span data-stu-id="87832-108">A [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure with its **opCode** member set to MXDCOP\_PRINTTICKET\_FIXED\_PAGE, MXDCOP\_PRINTTICKET\_FIXED\_DOC, or MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ.</span></span>

</dd> <dt>

<span data-ttu-id="87832-109">**printTicketData**</span><span class="sxs-lookup"><span data-stu-id="87832-109">**printTicketData**</span></span>
</dt> <dd>

<span data-ttu-id="87832-110">Struttura [**di \_ \_ data \_ T PRINTTICKET MXDC**](mxdcprintticketpassthrough.md) contenente il ticket di stampa.</span><span class="sxs-lookup"><span data-stu-id="87832-110">A [**MXDC\_PRINTTICKET\_DATA\_T**](mxdcprintticketpassthrough.md) structure containing the print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="87832-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="87832-111">Remarks</span></span>

<span data-ttu-id="87832-112">Questa struttura viene passata nel parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando tale funzione viene chiamata con il escape di [**\_ escape MXDC**](mxdc-escape.md) e il membro **OpCode** della struttura dell' [**\_ \_ intestazione \_ di escape MXDC**](mxdcescapeheader.md) è **MXDCOP \_ \_ \_ pagina fissa** dell'oggetto, **MXDCOP \_ PrintTicket \_ fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**.</span><span class="sxs-lookup"><span data-stu-id="87832-112">This structure is passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when that function is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the **opCode** member of the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure is **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**.</span></span> <span data-ttu-id="87832-113">Il risultato è la scrittura del ticket di stampa nel file di documento XPS.</span><span class="sxs-lookup"><span data-stu-id="87832-113">The result is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="87832-114">Allocare memoria per l'escape come illustrato di seguito, impostare i campi in base alle esigenze e quindi chiamare [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span><span class="sxs-lookup"><span data-stu-id="87832-114">Allocate memory for the escape as shown below, set the fields as needed, and then call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape).</span></span>


```C++
// Compute size of buffer required adding the
//  size of the escape structure to the size
//  of the resource data buffer.
SIZE_T iTotalDataSize = sizeof(MXDC_PRINTTICKET_ESCAPE_T) + 
                        iS0PageDataSize - 1;

// Allocate the memory buffer.
P_MXDC_PRINTTICKET_ESCAPE_T pS0PageEscapeData = 
                        (P_MXDC_PRINTTICKET_ESCAPE_T)HeapAlloc(
                            GetProcessHeap(),
                            0,
                            iTotalDataSize);
```



<span data-ttu-id="87832-115">Se il **codice operativo** è impostato **su MXDCOP \_ PRINTTICKET \_ fixed \_ Page**, la chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere eseguita tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="87832-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="87832-116">Se il **codice operativo** è impostato **su \_ MXDCOP \_ PrintTicket fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**, la chiamata a **ExtEscape** deve essere eseguita tra una chiamata a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e una chiamata a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="87832-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="87832-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87832-117">Requirements</span></span>



| <span data-ttu-id="87832-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="87832-118">Requirement</span></span> | <span data-ttu-id="87832-119">Valore</span><span class="sxs-lookup"><span data-stu-id="87832-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="87832-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87832-120">Minimum supported client</span></span><br/> | <span data-ttu-id="87832-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="87832-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="87832-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="87832-122">Minimum supported server</span></span><br/> | <span data-ttu-id="87832-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="87832-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="87832-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="87832-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="87832-125"><dt>MXDC. h</dt></span><span class="sxs-lookup"><span data-stu-id="87832-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87832-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87832-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87832-127">Stampa</span><span class="sxs-lookup"><span data-stu-id="87832-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="87832-128">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="87832-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="87832-129">[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="87832-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="87832-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="87832-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="87832-131">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="87832-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

