---
description: Inviato a una procedura DLL di estensione di File Manager quando File Manager vuole una stringa della Guida per un menu o una voce di comando della barra degli strumenti.
title: FMEVENT_HELPSTRING messaggio (Wfext.h)
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
ms.openlocfilehash: 6fe187330e27f7e246c9bbd68005f68f346bbc90
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841282"
---
# <a name="fmevent_helpstring-message"></a><span data-ttu-id="96058-103">Messaggio \_ HELPSTRING FMEVENT</span><span class="sxs-lookup"><span data-stu-id="96058-103">FMEVENT\_HELPSTRING message</span></span>

<span data-ttu-id="96058-104">Inviato a una procedura DLL di estensione di File Manager quando File Manager vuole una stringa della Guida per un menu o una voce di comando della barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="96058-104">Sent to a File Manager extension DLL procedure when File Manager wants a Help string for a menu or toolbar command item.</span></span>

## <a name="parameters"></a><span data-ttu-id="96058-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="96058-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96058-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="96058-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="96058-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="96058-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="96058-108">*lpfmshs*</span><span class="sxs-lookup"><span data-stu-id="96058-108">*lpfmshs*</span></span> 
</dt> <dd>

<span data-ttu-id="96058-109">Indirizzo di una struttura [**\_ HELPSTRING FMS**](fms-helpstring.md) che comunica i dati della stringa della Guida dell'elemento del comando.</span><span class="sxs-lookup"><span data-stu-id="96058-109">The address of an [**FMS\_HELPSTRING**](fms-helpstring.md) structure that communicates command item Help string data.</span></span> <span data-ttu-id="96058-110">La **struttura FMS \_ HELPSTRING** identifica l'elemento di comando per il quale è ricercata una stringa della Guida, insieme a un handle al relativo menu.</span><span class="sxs-lookup"><span data-stu-id="96058-110">The **FMS\_HELPSTRING** structure identifies the command item for which a Help string is wanted, along with a handle to its menu.</span></span> <span data-ttu-id="96058-111">Un'applicazione scrive quindi la stringa della Guida appropriata nel membro **szHelp** della struttura **\_ HELPSTRING FMS.**</span><span class="sxs-lookup"><span data-stu-id="96058-111">An application then writes the appropriate Help string to the **FMS\_HELPSTRING** structure's **szHelp** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96058-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96058-112">Return value</span></span>

<span data-ttu-id="96058-113">Una routine DLL di estensione deve restituire zero se elabora questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="96058-113">An extension DLL procedure should return zero if it processes this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="96058-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96058-114">Requirements</span></span>



| <span data-ttu-id="96058-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="96058-115">Requirement</span></span> | <span data-ttu-id="96058-116">Valore</span><span class="sxs-lookup"><span data-stu-id="96058-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96058-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96058-117">Minimum supported client</span></span><br/> | <span data-ttu-id="96058-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="96058-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="96058-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="96058-119">Minimum supported server</span></span><br/> | <span data-ttu-id="96058-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="96058-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="96058-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96058-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="96058-122"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="96058-122"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96058-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96058-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96058-124">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="96058-124">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> <dt>

[<span data-ttu-id="96058-125">**FMEVENT \_ HELPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="96058-125">**FMEVENT\_HELPMENUITEM**</span></span>](fmevent-helpmenuitem.md)
</dt> </dl>

 

 




