---
description: La \_ \_ struttura di data T PRINTTICKET MXDC contiene \_ un ticket di stampa del documento XPS, che contiene le impostazioni della stampante e del processo di stampa, da passare al file di output Microsoft XPS Document Converter (MXDC) senza alcuna elaborazione.
ms.assetid: d30ba8bb-f429-49d5-963c-b770c3086e97
title: Struttura MXDC_PRINTTICKET_DATA_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_PRINTTICKET_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 94308527437316dda75fc5a50a6a7829e9315c3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881605"
---
# <a name="mxdc_printticket_data_t-structure"></a><span data-ttu-id="31368-103">\_ \_ Struttura T di dati PRINTTICKET MXDC \_</span><span class="sxs-lookup"><span data-stu-id="31368-103">MXDC\_PRINTTICKET\_DATA\_T structure</span></span>

<span data-ttu-id="31368-104">La struttura di **\_ \_ data \_ T PRINTTICKET MXDC** contiene un ticket di stampa del documento XPS, che contiene le impostazioni della stampante e del processo di stampa, da passare al file di output Microsoft XPS Document Converter (MXDC) senza alcuna elaborazione.</span><span class="sxs-lookup"><span data-stu-id="31368-104">The **MXDC\_PRINTTICKET\_DATA\_T** structure holds an XPS document print ticket, which contains printer and print job settings, to pass to the Microsoft XPS Document Converter (MXDC) output file without any processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="31368-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31368-105">Syntax</span></span>


```C++
typedef struct tagMxdcPrintTicketData {
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_PRINTTICKET_DATA_T, *P_MXDC_PRINTTICKET_DATA_T;
```



## <a name="members"></a><span data-ttu-id="31368-106">Members</span><span class="sxs-lookup"><span data-stu-id="31368-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="31368-107">**dwDataSize**</span><span class="sxs-lookup"><span data-stu-id="31368-107">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="31368-108">Dimensioni in byte del ticket di stampa.</span><span class="sxs-lookup"><span data-stu-id="31368-108">The size of the print ticket in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="31368-109">**bData**</span><span class="sxs-lookup"><span data-stu-id="31368-109">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="31368-110">Il ticket di stampa del documento XPS.</span><span class="sxs-lookup"><span data-stu-id="31368-110">The XPS document print ticket.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="31368-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="31368-111">Remarks</span></span>

<span data-ttu-id="31368-112">Questa struttura viene aggiunta a una struttura [**MXDC \_ di \_ intestazione \_ di escape T**](mxdcescapeheader.md) con il membro **OpCode** impostato su **MXDCOP \_ PrintTicket \_ fixed \_ Page**, **MXDCOP \_ PrintTicket \_ fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq** per creare una struttura [**MXDC \_ PrintTicket di \_ escape \_ t**](mxdcprintticketescape.md) .</span><span class="sxs-lookup"><span data-stu-id="31368-112">This structure is appended to an [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that has the **opCode** member set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, **MXDCOP\_PRINTTICKET\_FIXED\_DOC**, or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ** to make an [**MXDC\_PRINTTICKET\_ESCAPE\_T**](mxdcprintticketescape.md) structure.</span></span> <span data-ttu-id="31368-113">La **struttura \_ \_ \_ T di escape PRINTTICKET MXDC** viene quindi passata al parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando viene chiamata con l'escape di [**escape \_ MXDC**](mxdc-escape.md) .</span><span class="sxs-lookup"><span data-stu-id="31368-113">The **MXDC\_PRINTTICKET\_ESCAPE\_T** structure is then passed to the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="31368-114">L'effetto è quello di scrivere il ticket di stampa nel file di documento XPS.</span><span class="sxs-lookup"><span data-stu-id="31368-114">The effect is to write the print ticket to the XPS document file.</span></span>

<span data-ttu-id="31368-115">Se il **codice operativo** è impostato **su MXDCOP \_ PRINTTICKET \_ fixed \_ Page**, la chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere eseguita tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span><span class="sxs-lookup"><span data-stu-id="31368-115">If the **opCode** is set to **MXDCOP\_PRINTTICKET\_FIXED\_PAGE**, the call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must occur between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage).</span></span> <span data-ttu-id="31368-116">Se il **codice operativo** è impostato **su \_ MXDCOP \_ PrintTicket fixed \_ doc** o **MXDCOP \_ PrintTicket \_ fixed \_ doc \_ Seq**, la chiamata a **ExtEscape** deve essere eseguita tra una chiamata a [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) e una chiamata a [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span><span class="sxs-lookup"><span data-stu-id="31368-116">If the **opCode** set to either **MXDCOP\_PRINTTICKET\_FIXED\_DOC** or **MXDCOP\_PRINTTICKET\_FIXED\_DOC\_SEQ**, the call to **ExtEscape** must occur between a call to [**StartDoc**](/windows/desktop/api/Wingdi/nf-wingdi-startdoca) and a call to [**EndDoc**](/windows/desktop/api/Wingdi/nf-wingdi-enddoc).</span></span>

## <a name="requirements"></a><span data-ttu-id="31368-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31368-117">Requirements</span></span>



| <span data-ttu-id="31368-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="31368-118">Requirement</span></span> | <span data-ttu-id="31368-119">Valore</span><span class="sxs-lookup"><span data-stu-id="31368-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="31368-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31368-120">Minimum supported client</span></span><br/> | <span data-ttu-id="31368-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="31368-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="31368-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31368-122">Minimum supported server</span></span><br/> | <span data-ttu-id="31368-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="31368-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="31368-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="31368-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="31368-125"><dt>MXDC. h</dt></span><span class="sxs-lookup"><span data-stu-id="31368-125"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31368-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="31368-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31368-127">Stampa</span><span class="sxs-lookup"><span data-stu-id="31368-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="31368-128">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="31368-128">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="31368-129">[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31368-129">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="31368-130">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="31368-130">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="31368-131">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="31368-131">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

