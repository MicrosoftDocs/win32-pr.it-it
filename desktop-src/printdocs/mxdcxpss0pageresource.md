---
description: La \_ struttura della \_ risorsa T S0PAGE di MXDC XPS \_ \_ include informazioni su una risorsa, ad esempio un'immagine o un tipo di carattere, associato a una pagina del documento XPS e da passare al file di output di Microsoft XPS Document Converter (MXDC).
ms.assetid: af0690a6-3047-4e95-b719-2305948c0f5d
title: Struttura MXDC_XPS_S0PAGE_RESOURCE_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_XPS_S0PAGE_RESOURCE_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: 90f8a52ed3bd1bcba4c8f21a086627781bdbbf67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882514"
---
# <a name="mxdc_xps_s0page_resource_t-structure"></a><span data-ttu-id="0c58a-103">\_ \_ \_ Struttura T della risorsa \_ S0PAGE di MXDC XPS</span><span class="sxs-lookup"><span data-stu-id="0c58a-103">MXDC\_XPS\_S0PAGE\_RESOURCE\_T structure</span></span>

<span data-ttu-id="0c58a-104">La struttura della **\_ \_ \_ risorsa \_ T S0PAGE di MXDC XPS** include informazioni su una risorsa, ad esempio un'immagine o un tipo di carattere, associato a una pagina del documento XPS e da passare al file di output di Microsoft XPS Document Converter (MXDC).</span><span class="sxs-lookup"><span data-stu-id="0c58a-104">The **MXDC\_XPS\_S0PAGE\_RESOURCE\_T** structure holds information about a resource, such as an image or font, that is associated with an XPS document page, and is to be passed to the Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c58a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0c58a-105">Syntax</span></span>


```C++
typedef struct tagMxdcXpsS0PageResource {
  DWORD dwSize;
  DWORD dwResourceType;
  BYTE  szUri[MAX_PATH];
  DWORD dwDataSize;
  BYTE  bData[1];
} MXDC_XPS_S0PAGE_RESOURCE_T, *P_MXDC_XPS_S0PAGE_RESOURCE_T;
```



## <a name="members"></a><span data-ttu-id="0c58a-106">Members</span><span class="sxs-lookup"><span data-stu-id="0c58a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0c58a-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="0c58a-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="0c58a-108">Dimensioni totali della struttura e della risorsa a cui fa riferimento.</span><span class="sxs-lookup"><span data-stu-id="0c58a-108">The total size of this structure and the resource to which it points.</span></span>

</dd> <dt>

<span data-ttu-id="0c58a-109">**dwResourceType**</span><span class="sxs-lookup"><span data-stu-id="0c58a-109">**dwResourceType**</span></span>
</dt> <dd>

<span data-ttu-id="0c58a-110">Valore di tipo [**MXDC \_ S0 \_ Page \_ enums**](mxdcs0pageenums.md) che indica il tipo di risorsa, ad esempio l'immagine TIFF o il tipo di carattere TrueType.</span><span class="sxs-lookup"><span data-stu-id="0c58a-110">A value of type [**MXDC\_S0\_PAGE\_ENUMS**](mxdcs0pageenums.md) indicating the type of resource, such as TIFF image or TrueType font.</span></span>

</dd> <dt>

<span data-ttu-id="0c58a-111">**szUri**</span><span class="sxs-lookup"><span data-stu-id="0c58a-111">**szUri**</span></span>
</dt> <dd>

<span data-ttu-id="0c58a-112">URI della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c58a-112">The URI of the resource.</span></span> <span data-ttu-id="0c58a-113">Non può essere superiore a 260 byte.</span><span class="sxs-lookup"><span data-stu-id="0c58a-113">This cannot be more than 260 bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0c58a-114">**dwDataSize**</span><span class="sxs-lookup"><span data-stu-id="0c58a-114">**dwDataSize**</span></span>
</dt> <dd>

<span data-ttu-id="0c58a-115">Dimensioni in byte della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c58a-115">The size of the resource in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="0c58a-116">**bData**</span><span class="sxs-lookup"><span data-stu-id="0c58a-116">**bData**</span></span>
</dt> <dd>

<span data-ttu-id="0c58a-117">I dati della risorsa in una matrice di byte con dimensioni pari a 1 + le dimensioni della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0c58a-117">The data of the resource in an array of bytes with size 1 + the size of the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c58a-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="0c58a-118">Remarks</span></span>

<span data-ttu-id="0c58a-119">Questa struttura viene aggiunta a una struttura [**MXDC \_ dell' \_ intestazione \_ di escape t**](mxdcescapeheader.md) (il cui **codice operativo** è impostato su **MXDCOP \_ set \_ S0PAGERESOURCE**) per creare una struttura di [**\_ \_ \_ escape \_ t della risorsa MXDC S0PAGE**](mxdcs0pageresourceescape.md) .</span><span class="sxs-lookup"><span data-stu-id="0c58a-119">This structure is appended to a [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure (that has its **opCode** set to **MXDCOP\_SET\_S0PAGERESOURCE**) to make an [**MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T**](mxdcs0pageresourceescape.md) structure.</span></span> <span data-ttu-id="0c58a-120">La struttura **di \_ \_ \_ escape \_ T della risorsa S0PAGE MXDC** risultante viene quindi passata nel parametro *lpszInData* della funzione [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) chiamata con l'escape di [**\_ escape MXDC**](mxdc-escape.md) .</span><span class="sxs-lookup"><span data-stu-id="0c58a-120">The resulting **MXDC\_S0PAGE\_RESOURCE\_ESCAPE\_T** structure is then passed in the *lpszInData* parameter of the [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) function that it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape.</span></span> <span data-ttu-id="0c58a-121">L'effetto è l'invio della risorsa a MXDC per la conversione e la scrittura nel file di output.</span><span class="sxs-lookup"><span data-stu-id="0c58a-121">The effect is to send the resource to the MXDC for conversion and to be written to the output file.</span></span>

<span data-ttu-id="0c58a-122">La chiamata a [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) deve essere compresa tra una chiamata a [**Startpage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) e una chiamata a [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); Tuttavia, possono essere presenti più chiamate tra le chiamate a **Startpage** e **EndPage**.</span><span class="sxs-lookup"><span data-stu-id="0c58a-122">The call to [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) must be between a call to [**StartPage**](/windows/desktop/api/Wingdi/nf-wingdi-startpage) and a call to [**EndPage**](/windows/desktop/api/Wingdi/nf-wingdi-endpage); however there can be more than one such calls between the calls to **StartPage** and **EndPage**.</span></span>

<span data-ttu-id="0c58a-123">Il consumo di flussi è più efficiente se si chiama [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) con **MXDCOP \_ set \_ S0PAGE \_ Resource** **OpCode** per ogni risorsa nella pagina prima di chiamare **ExtEscape** con il **codice operativo** MXDCOP **\_ set \_ S0PAGE** .</span><span class="sxs-lookup"><span data-stu-id="0c58a-123">Streaming consumption is more efficient if you call [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) with the **MXDCOP\_SET\_S0PAGE\_RESOURCE** **opCode** for each resource on the page before you call **ExtEscape** with the **MXDCOP\_SET\_S0PAGE** **opCode**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c58a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0c58a-124">Requirements</span></span>



| <span data-ttu-id="0c58a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c58a-125">Requirement</span></span> | <span data-ttu-id="0c58a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0c58a-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0c58a-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c58a-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0c58a-128">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c58a-128">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0c58a-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0c58a-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0c58a-130">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c58a-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0c58a-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0c58a-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c58a-132"><dt>MXDC. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c58a-132"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c58a-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0c58a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c58a-134">Stampa</span><span class="sxs-lookup"><span data-stu-id="0c58a-134">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="0c58a-135">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="0c58a-135">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="0c58a-136">[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0c58a-136">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0c58a-137">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="0c58a-137">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="0c58a-138">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="0c58a-138">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

