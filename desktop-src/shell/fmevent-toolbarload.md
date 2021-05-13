---
description: Inviato a una DLL di estensione quando File Manager carica la relativa barra degli strumenti. Questo messaggio consente a una DLL di estensione di aggiungere un pulsante alla barra degli strumenti di File Manager.
title: FMEVENT_TOOLBARLOAD messaggio (Wfext.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_TOOLBARLOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.assetid: c5daab49-4ed5-439b-b1b7-a87f70c379f0
ms.openlocfilehash: c4195acedbd696679a2deea2f4d6e268717566d1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841272"
---
# <a name="fmevent_toolbarload-message"></a><span data-ttu-id="3ffc9-104">FMEVENT \_ TOOLBARLOAD message</span><span class="sxs-lookup"><span data-stu-id="3ffc9-104">FMEVENT\_TOOLBARLOAD message</span></span>

<span data-ttu-id="3ffc9-105">Inviato a una DLL di estensione quando File Manager carica la relativa barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="3ffc9-105">Sent to an extension DLL when File Manager is loading its toolbar.</span></span> <span data-ttu-id="3ffc9-106">Questo messaggio consente a una DLL di estensione di aggiungere un pulsante alla barra degli strumenti di File Manager.</span><span class="sxs-lookup"><span data-stu-id="3ffc9-106">This message allows an extension DLL to add a button to the File Manager toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3ffc9-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ffc9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ffc9-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3ffc9-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3ffc9-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3ffc9-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3ffc9-110">*lpfmstbl*</span><span class="sxs-lookup"><span data-stu-id="3ffc9-110">*lpfmstbl*</span></span> 
</dt> <dd>

<span data-ttu-id="3ffc9-111">Indirizzo di una [**struttura \_ TOOLBARLOAD fms.**](fms-toolbarload.md)</span><span class="sxs-lookup"><span data-stu-id="3ffc9-111">The address of an [**FMS\_TOOLBARLOAD**](fms-toolbarload.md) structure.</span></span> <span data-ttu-id="3ffc9-112">Se la DLL di estensione aggiunge un pulsante alla barra degli strumenti in File Manager, la DLL deve riempire la struttura con le informazioni sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="3ffc9-112">If the extension DLL adds a button to the toolbar in File Manager, the DLL should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ffc9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ffc9-113">Return value</span></span>

<span data-ttu-id="3ffc9-114">Una DLL di estensione deve restituire **TRUE** per aggiungere il pulsante alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="3ffc9-114">An extension DLL must return **TRUE** to add the button to the toolbar.</span></span> <span data-ttu-id="3ffc9-115">Se la DLL restituisce **FALSE,** File Manager non aggiunge il pulsante.</span><span class="sxs-lookup"><span data-stu-id="3ffc9-115">If the DLL returns **FALSE**, File Manager does not add the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ffc9-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ffc9-116">Requirements</span></span>



| <span data-ttu-id="3ffc9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ffc9-117">Requirement</span></span> | <span data-ttu-id="3ffc9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="3ffc9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ffc9-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ffc9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3ffc9-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3ffc9-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="3ffc9-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3ffc9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3ffc9-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3ffc9-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3ffc9-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ffc9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ffc9-124"><dt>Wfext.h</dt></span><span class="sxs-lookup"><span data-stu-id="3ffc9-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ffc9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ffc9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ffc9-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="3ffc9-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




