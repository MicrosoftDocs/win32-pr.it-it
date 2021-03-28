---
description: Inviato a una procedura DLL di estensione di file Manager quando il file Manager desidera una stringa della Guida per un elemento di comando del menu o della barra degli strumenti.
title: Messaggio FMEVENT_HELPSTRING (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_HELPSTRING
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: 55fb5bfe-2889-40e5-9798-85f63727e31f
ms.openlocfilehash: ae3be1953d4c8bbf70f8f17fcf34fcfb1ac583f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227449"
---
# <a name="fmevent_helpstring-message"></a><span data-ttu-id="b4c95-103">\_Messaggio FMEVENT HELPSTRING</span><span class="sxs-lookup"><span data-stu-id="b4c95-103">FMEVENT\_HELPSTRING message</span></span>

<span data-ttu-id="b4c95-104">Inviato a una procedura DLL di estensione di file Manager quando il file Manager desidera una stringa della Guida per un elemento di comando del menu o della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="b4c95-104">Sent to a File Manager extension DLL procedure when File Manager wants a Help string for a menu or toolbar command item.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4c95-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="b4c95-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4c95-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b4c95-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b4c95-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="b4c95-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b4c95-108">*lpfmshs*</span><span class="sxs-lookup"><span data-stu-id="b4c95-108">*lpfmshs*</span></span> 
</dt> <dd>

<span data-ttu-id="b4c95-109">Indirizzo di una struttura [**FMS \_ HELPSTRING**](fms-helpstring.md) che comunica i dati della stringa della Guida dell'elemento di comando.</span><span class="sxs-lookup"><span data-stu-id="b4c95-109">The address of an [**FMS\_HELPSTRING**](fms-helpstring.md) structure that communicates command item Help string data.</span></span> <span data-ttu-id="b4c95-110">La struttura **FMS \_ HELPSTRING** identifica l'elemento di comando per il quale si desidera una stringa della guida, insieme a un handle per il menu.</span><span class="sxs-lookup"><span data-stu-id="b4c95-110">The **FMS\_HELPSTRING** structure identifies the command item for which a Help string is wanted, along with a handle to its menu.</span></span> <span data-ttu-id="b4c95-111">Un'applicazione scrive quindi la stringa della guida appropriata nel membro **szHelp** della struttura **FMS \_ HELPSTRING** .</span><span class="sxs-lookup"><span data-stu-id="b4c95-111">An application then writes the appropriate Help string to the **FMS\_HELPSTRING** structure's **szHelp** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4c95-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b4c95-112">Return value</span></span>

<span data-ttu-id="b4c95-113">Una procedura DLL di estensione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="b4c95-113">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4c95-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b4c95-114">Requirements</span></span>



| <span data-ttu-id="b4c95-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4c95-115">Requirement</span></span> | <span data-ttu-id="b4c95-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b4c95-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4c95-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4c95-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b4c95-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b4c95-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="b4c95-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b4c95-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b4c95-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="b4c95-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b4c95-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b4c95-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4c95-122"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4c95-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4c95-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b4c95-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4c95-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="b4c95-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="b4c95-125">**\_HELPMENUITEM FMEVENT**</span><span class="sxs-lookup"><span data-stu-id="b4c95-125">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




