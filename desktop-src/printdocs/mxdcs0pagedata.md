---
description: La \_ struttura MXDC S0PAGE \_ data \_ T include una pagina di documento XPS da passare al file di output di Microsoft XPS Document Converter (MXDC) senza alcuna elaborazione.
ms.assetid: 3dc8e0b9-cf63-4345-93d2-3b60dac42546
title: Struttura MXDC_S0PAGE_DATA_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_S0PAGE_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 2da9df454b8741f2203072fd25856118407ef5c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757742"
---
# <a name="mxdc_s0page_data_t-structure"></a><span data-ttu-id="113e1-103">MXDC \_ S0PAGE \_ data \_ T Structure</span><span class="sxs-lookup"><span data-stu-id="113e1-103">MXDC\_S0PAGE\_DATA\_T structure</span></span>

<span data-ttu-id="113e1-104">La struttura **MXDC \_ S0PAGE \_ data \_ T** include una pagina di documento XPS da passare al file di output di Microsoft XPS Document Converter (MXDC) senza alcuna elaborazione.</span><span class="sxs-lookup"><span data-stu-id="113e1-104">The **MXDC\_S0PAGE\_DATA\_T** structure holds an XPS document page to be passed to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="113e1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="113e1-105">Syntax</span></span>


```C++
typedef struct tagMxdcS0PageData {
  ULONG dwSize;
  BYTE  bData[1];
} MXDC_S0PAGE_DATA_T, *P_MXDC_S0PAGE_DATA_T;
```



## <a name="members"></a><span data-ttu-id="113e1-106">Members</span><span class="sxs-lookup"><span data-stu-id="113e1-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="113e1-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="113e1-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="113e1-108">Dimensioni del buffer di output, **bdata**.</span><span class="sxs-lookup"><span data-stu-id="113e1-108">The size of the output buffer, **bData**.</span></span>

</dd> <dt>

<span data-ttu-id="113e1-109">**bData**</span><span class="sxs-lookup"><span data-stu-id="113e1-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="113e1-110">Pagina del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="113e1-110">The XPS document page.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="113e1-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="113e1-111">Remarks</span></span>

<span data-ttu-id="113e1-112">Questa struttura viene aggiunta a una struttura [**MXDC \_ dell' \_ intestazione \_ di escape t**](mxdcescapeheader.md) (il cui **codice operativo** è impostato su MXDCOP \_ set \_ S0PAGE) per creare una struttura [**MXDC \_ S0PAGE \_ PassThrough \_ escape \_ t**](mxdcs0pagepassthroughescape.md) .</span><span class="sxs-lookup"><span data-stu-id="113e1-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (which has its **opCode** set to MXDCOP\_SET\_S0PAGE) to make an [**MXDC\_S0PAGE\_PASSTHROUGH\_ESCAPE\_T**](mxdcs0pagepassthroughescape.md) structure.</span></span> <span data-ttu-id="113e1-113">Tale struttura viene quindi passata al parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando viene chiamata con l' [**\_ escape MXDC**](mxdc-escape.md) come escape.</span><span class="sxs-lookup"><span data-stu-id="113e1-113">That structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with [**MXDC\_ESCAPE**](mxdc-escape.md) as the escape.</span></span> <span data-ttu-id="113e1-114">Il risultato è che il MXDC passa la pagina all'output senza elaborarla.</span><span class="sxs-lookup"><span data-stu-id="113e1-114">The result is that the MXDC passes the page through to the output without processing it.</span></span>

<span data-ttu-id="113e1-115">La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere compresa tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="113e1-115">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span>

<span data-ttu-id="113e1-116">L'applicazione chiamante è responsabile della convalida del codice XML della pagina del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="113e1-116">The calling application is responsible for validating the XML of the XPS document page.</span></span>

<span data-ttu-id="113e1-117">Il consumo di flussi è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ impostare la \_ \_ risorsa S0PAGE** come **OpCode** per ogni risorsa nella pagina prima di chiamarla con **MXDCOP \_ set \_ S0PAGE**.</span><span class="sxs-lookup"><span data-stu-id="113e1-117">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with **MXDCOP\_SET\_S0PAGE\_RESOURCE** as **opCode** for each resource on the page before you call it with **MXDCOP\_SET\_S0PAGE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="113e1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="113e1-118">Requirements</span></span>



| <span data-ttu-id="113e1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="113e1-119">Requirement</span></span> | <span data-ttu-id="113e1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="113e1-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="113e1-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="113e1-121">Minimum supported client</span></span><br/> | <span data-ttu-id="113e1-122">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="113e1-122">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="113e1-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="113e1-123">Minimum supported server</span></span><br/> | <span data-ttu-id="113e1-124">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="113e1-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="113e1-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="113e1-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="113e1-126"><dt>MXDC. h</dt></span><span class="sxs-lookup"><span data-stu-id="113e1-126"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="113e1-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="113e1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="113e1-128">Stampa</span><span class="sxs-lookup"><span data-stu-id="113e1-128">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="113e1-129">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="113e1-129">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="113e1-130">[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="113e1-130">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="113e1-131">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="113e1-131">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="113e1-132">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="113e1-132">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

