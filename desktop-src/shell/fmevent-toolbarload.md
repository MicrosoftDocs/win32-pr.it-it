---
description: Inviato a una DLL di estensione quando il file Manager carica la barra degli strumenti. Questo messaggio consente a una DLL di estensione di aggiungere un pulsante alla barra degli strumenti di gestione file.
title: Messaggio FMEVENT_TOOLBARLOAD (Wfext. h)
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
ms.openlocfilehash: 5f04b524c8d44d987513b6605f9f827336078d02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227448"
---
# <a name="fmevent_toolbarload-message"></a><span data-ttu-id="7dbec-104">\_Messaggio FMEVENT TOOLBARLOAD</span><span class="sxs-lookup"><span data-stu-id="7dbec-104">FMEVENT\_TOOLBARLOAD message</span></span>

<span data-ttu-id="7dbec-105">Inviato a una DLL di estensione quando il file Manager carica la barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="7dbec-105">Sent to an extension DLL when File Manager is loading its toolbar.</span></span> <span data-ttu-id="7dbec-106">Questo messaggio consente a una DLL di estensione di aggiungere un pulsante alla barra degli strumenti di gestione file.</span><span class="sxs-lookup"><span data-stu-id="7dbec-106">This message allows an extension DLL to add a button to the File Manager toolbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="7dbec-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="7dbec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7dbec-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7dbec-108">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="7dbec-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7dbec-109">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="7dbec-110">*lpfmstbl*</span><span class="sxs-lookup"><span data-stu-id="7dbec-110">*lpfmstbl*</span></span> 
</dt> <dd>

<span data-ttu-id="7dbec-111">Indirizzo di una struttura [**di \_ TOOLBARLOAD FMS**](fms-toolbarload.md) .</span><span class="sxs-lookup"><span data-stu-id="7dbec-111">The address of an [**FMS\_TOOLBARLOAD**](fms-toolbarload.md) structure.</span></span> <span data-ttu-id="7dbec-112">Se la DLL di estensione aggiunge un pulsante alla barra degli strumenti in file Manager, la DLL deve riempire la struttura con informazioni sul pulsante.</span><span class="sxs-lookup"><span data-stu-id="7dbec-112">If the extension DLL adds a button to the toolbar in File Manager, the DLL should fill the structure with information about the button.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7dbec-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7dbec-113">Return value</span></span>

<span data-ttu-id="7dbec-114">Una DLL di estensione deve restituire **true** per aggiungere il pulsante alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="7dbec-114">An extension DLL must return **TRUE** to add the button to the toolbar.</span></span> <span data-ttu-id="7dbec-115">Se la DLL restituisce **false**, il pulsante non viene aggiunto dal file Manager.</span><span class="sxs-lookup"><span data-stu-id="7dbec-115">If the DLL returns **FALSE**, File Manager does not add the button.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dbec-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7dbec-116">Requirements</span></span>



| <span data-ttu-id="7dbec-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dbec-117">Requirement</span></span> | <span data-ttu-id="7dbec-118">Valore</span><span class="sxs-lookup"><span data-stu-id="7dbec-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7dbec-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dbec-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7dbec-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7dbec-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7dbec-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7dbec-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7dbec-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7dbec-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7dbec-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7dbec-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dbec-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dbec-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dbec-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7dbec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dbec-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="7dbec-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 




