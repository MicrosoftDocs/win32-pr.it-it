---
description: La \_ struttura Printer Info \_ 3 specifica le informazioni di sicurezza della stampante.
ms.assetid: 527d635d-2d75-4b56-bab7-e95c9919a8fb
title: Struttura PRINTER_INFO_3 (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTER_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: aad24e56d43f6fadd3da3f627b2399249a7ff8a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315982"
---
# <a name="printer_info_3-structure"></a><span data-ttu-id="f1e77-103">\_Struttura Info stampante \_ 3</span><span class="sxs-lookup"><span data-stu-id="f1e77-103">PRINTER\_INFO\_3 structure</span></span>

<span data-ttu-id="f1e77-104">La struttura **Printer \_ info \_ 3** specifica le informazioni di sicurezza della stampante.</span><span class="sxs-lookup"><span data-stu-id="f1e77-104">The **PRINTER\_INFO\_3** structure specifies printer security information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1e77-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1e77-105">Syntax</span></span>


```C++
typedef struct _PRINTER_INFO_3 {
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
} PRINTER_INFO_3, *PPRINTER_INFO_3;
```



## <a name="members"></a><span data-ttu-id="f1e77-106">Members</span><span class="sxs-lookup"><span data-stu-id="f1e77-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f1e77-107">**pSecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="f1e77-107">**pSecurityDescriptor**</span></span>
</dt> <dd>

<span data-ttu-id="f1e77-108">Puntatore a una struttura di [**\_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) che specifica le informazioni di sicurezza di una stampante.</span><span class="sxs-lookup"><span data-stu-id="f1e77-108">Pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that specifies a printer's security information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f1e77-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1e77-109">Remarks</span></span>

<span data-ttu-id="f1e77-110">La struttura **Printer \_ info \_ 3** consente a un'applicazione di ottenere e impostare il descrittore di sicurezza di una stampante.</span><span class="sxs-lookup"><span data-stu-id="f1e77-110">The **PRINTER\_INFO\_3** structure lets an application get and set a printer's security descriptor.</span></span> <span data-ttu-id="f1e77-111">Il chiamante può eseguire questa operazione anche se non dispone di autorizzazioni specifiche per la stampante, purché disponga dei diritti standard descritti in [**Seprinter**](setprinter.md) e [**GetPrinter**](getprinter.md).</span><span class="sxs-lookup"><span data-stu-id="f1e77-111">The caller may do so even if it lacks specific printer permissions, as long as it has the standard rights described in [**SetPrinter**](setprinter.md) and [**GetPrinter**](getprinter.md).</span></span> <span data-ttu-id="f1e77-112">Pertanto, un'applicazione può negare temporaneamente l'accesso a una stampante, consentendo al proprietario della stampante di accedere all'ACL discrezionale della stampante.</span><span class="sxs-lookup"><span data-stu-id="f1e77-112">Thus, an application may temporarily deny all access to a printer, while allowing the owner of the printer to have access to the printer's discretionary ACL.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1e77-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1e77-113">Requirements</span></span>



| <span data-ttu-id="f1e77-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1e77-114">Requirement</span></span> | <span data-ttu-id="f1e77-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f1e77-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1e77-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1e77-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f1e77-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1e77-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f1e77-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1e77-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f1e77-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f1e77-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="f1e77-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1e77-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1e77-121"><dt>Winspool. h (include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1e77-121"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1e77-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1e77-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1e77-123">Stampa</span><span class="sxs-lookup"><span data-stu-id="f1e77-123">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="f1e77-124">Strutture dell'API spooler di stampa</span><span class="sxs-lookup"><span data-stu-id="f1e77-124">Print Spooler API Structures</span></span>](printing-and-print-spooler-structures.md)
</dt> <dt>

[<span data-ttu-id="f1e77-125">**SetPrinter**</span><span class="sxs-lookup"><span data-stu-id="f1e77-125">**SetPrinter**</span></span>](setprinter.md)
</dt> <dt>

[<span data-ttu-id="f1e77-126">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="f1e77-126">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="f1e77-127">**\_Informazioni stampante \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f1e77-127">**PRINTER\_INFO\_1**</span></span>](printer-info-1.md)
</dt> <dt>

[<span data-ttu-id="f1e77-128">**\_Informazioni stampante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f1e77-128">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> <dt>

[<span data-ttu-id="f1e77-129">**\_Informazioni stampante \_ 4**</span><span class="sxs-lookup"><span data-stu-id="f1e77-129">**PRINTER\_INFO\_4**</span></span>](printer-info-4.md)
</dt> <dt>

[<span data-ttu-id="f1e77-130">**descrittore di sicurezza \_**</span><span class="sxs-lookup"><span data-stu-id="f1e77-130">**SECURITY\_DESCRIPTOR**</span></span>](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

 

