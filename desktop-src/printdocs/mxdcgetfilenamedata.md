---
description: La \_ struttura MXDC Get \_ filename \_ data \_ T include il percorso completo e il nome file di un file di output di Microsoft XPS Document Converter (MXDC).
ms.assetid: 070bce2e-5055-47e8-9412-2094a636635f
title: Struttura MXDC_GET_FILENAME_DATA_T (MXDC. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MXDC_GET_FILENAME_DATA_T
api_type:
- HeaderDef
api_location:
- mxdc.h
ms.openlocfilehash: dd29696ae21924f245e508469acfbb88c78b034b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881606"
---
# <a name="mxdc_get_filename_data_t-structure"></a><span data-ttu-id="7f8b6-103">MXDC \_ ottenere \_ la \_ struttura dei dati filename \_</span><span class="sxs-lookup"><span data-stu-id="7f8b6-103">MXDC\_GET\_FILENAME\_DATA\_T structure</span></span>

<span data-ttu-id="7f8b6-104">La struttura **MXDC \_ get \_ filename \_ data \_ T** include il percorso completo e il nome file di un file di output di Microsoft XPS Document Converter (MXDC).</span><span class="sxs-lookup"><span data-stu-id="7f8b6-104">The **MXDC\_GET\_FILENAME\_DATA\_T** structure holds the full path and file name of a Microsoft XPS Document Converter (MXDC) output file.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f8b6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f8b6-105">Syntax</span></span>


```C++
typedef struct _tagMxdcGetFileNameData {
  ULONG   cbOutput;
  wchar_t wszData[1];
} MXDC_GET_FILENAME_DATA_T, *P_MXDC_GET_FILENAME_DATA_T;
```



## <a name="members"></a><span data-ttu-id="7f8b6-106">Members</span><span class="sxs-lookup"><span data-stu-id="7f8b6-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="7f8b6-107">**cbOutput**</span><span class="sxs-lookup"><span data-stu-id="7f8b6-107">**cbOutput**</span></span>
</dt> <dd>

<span data-ttu-id="7f8b6-108">Dimensioni del buffer di output, **wszData**.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-108">The size of the output buffer, **wszData**.</span></span>

</dd> <dt>

<span data-ttu-id="7f8b6-109">**wszData**</span><span class="sxs-lookup"><span data-stu-id="7f8b6-109">**wszData**</span></span>
</dt> <dd>

<span data-ttu-id="7f8b6-110">Percorso completo e nome file del file di output.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-110">The fully qualified path and file name of the output file.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7f8b6-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f8b6-111">Remarks</span></span>

<span data-ttu-id="7f8b6-112">Questa struttura viene restituita da [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) quando viene chiamata con l'escape di escape [**MXDC \_**](mxdc-escape.md) e la struttura dell' [**intestazione di \_ escape \_ \_ MXDC**](mxdcescapeheader.md) che viene passata nel parametro *lpszInData* è impostata sul **codice operativo** **MXDCOP \_ get \_ filename**.</span><span class="sxs-lookup"><span data-stu-id="7f8b6-112">This structure is returned by [**ExtEscape**](/windows/desktop/api/Wingdi/nf-wingdi-extescape) when it is called with the [**MXDC\_ESCAPE**](mxdc-escape.md) escape and the [**MXDC\_ESCAPE\_HEADER\_T**](mxdcescapeheader.md) structure that is passed in the *lpszInData* parameter has its **opCode** set to **MXDCOP\_GET\_FILENAME**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f8b6-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f8b6-113">Requirements</span></span>



| <span data-ttu-id="7f8b6-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f8b6-114">Requirement</span></span> | <span data-ttu-id="7f8b6-115">Valore</span><span class="sxs-lookup"><span data-stu-id="7f8b6-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="7f8b6-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f8b6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="7f8b6-117">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7f8b6-117">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7f8b6-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7f8b6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="7f8b6-119">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7f8b6-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="7f8b6-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7f8b6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="7f8b6-121"><dt>MXDC. h</dt></span><span class="sxs-lookup"><span data-stu-id="7f8b6-121"><dt>Mxdc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f8b6-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7f8b6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f8b6-123">Stampa</span><span class="sxs-lookup"><span data-stu-id="7f8b6-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="7f8b6-124">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="7f8b6-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

<span data-ttu-id="7f8b6-125">[Funzioni di escape della stampante GDI](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7f8b6-125">[GDI Printer Escape Functions](/previous-versions/windows/desktop/legacy/dd162843(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7f8b6-126">**ExtEscape**</span><span class="sxs-lookup"><span data-stu-id="7f8b6-126">**ExtEscape**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-extescape)
</dt> <dt>

[<span data-ttu-id="7f8b6-127">**\_escape MXDC**</span><span class="sxs-lookup"><span data-stu-id="7f8b6-127">**MXDC\_ESCAPE**</span></span>](mxdc-escape.md)
</dt> </dl>

 

