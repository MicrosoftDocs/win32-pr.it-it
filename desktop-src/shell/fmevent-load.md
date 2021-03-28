---
description: Inviato a una DLL di estensione quando la DLL viene caricata da file Manager.
ms.assetid: 9d673ab8-c468-4b46-b96e-1adfaa9f85fb
title: Messaggio FMEVENT_LOAD (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FMEVENT_LOAD
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: de7a950e3f17c9b2cee2b66a047d289ca29b6b56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979706"
---
# <a name="fmevent_load-message"></a><span data-ttu-id="974a4-103">\_Messaggio di caricamento FMEVENT</span><span class="sxs-lookup"><span data-stu-id="974a4-103">FMEVENT\_LOAD message</span></span>

<span data-ttu-id="974a4-104">Inviato a una DLL di estensione quando la DLL viene caricata da file Manager.</span><span class="sxs-lookup"><span data-stu-id="974a4-104">Sent to an extension DLL when File Manager is loading the DLL.</span></span>

## <a name="parameters"></a><span data-ttu-id="974a4-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="974a4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="974a4-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="974a4-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="974a4-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="974a4-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="974a4-108">*lpfmsld*</span><span class="sxs-lookup"><span data-stu-id="974a4-108">*lpfmsld*</span></span> 
</dt> <dd>

<span data-ttu-id="974a4-109">Indirizzo di una struttura [**di \_ caricamento FMS**](fms-load.md) che specifica il valore delta della voce di menu.</span><span class="sxs-lookup"><span data-stu-id="974a4-109">The address of an [**FMS\_LOAD**](fms-load.md) structure that specifies the menu item delta value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="974a4-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="974a4-110">Return value</span></span>

<span data-ttu-id="974a4-111">Una DLL di estensione deve restituire **true** per continuare a caricare la dll.</span><span class="sxs-lookup"><span data-stu-id="974a4-111">An extension DLL must return **TRUE** to continue loading the DLL.</span></span> <span data-ttu-id="974a4-112">Se la DLL restituisce **false**, gestione file chiama la funzione [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) e termina qualsiasi comunicazione con la dll di estensione.</span><span class="sxs-lookup"><span data-stu-id="974a4-112">If the DLL returns **FALSE**, File Manager calls the [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) function and ends any communication with the extension DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="974a4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="974a4-113">Remarks</span></span>

<span data-ttu-id="974a4-114">Un'applicazione deve riempire i membri **dwSize**, **szMenuName** e **HMenu** nella struttura di [**\_ caricamento FMS**](fms-load.md) .</span><span class="sxs-lookup"><span data-stu-id="974a4-114">An application should fill the **dwSize**, **szMenuName**, and **hMenu** members in the [**FMS\_LOAD**](fms-load.md) structure.</span></span> <span data-ttu-id="974a4-115">Deve inoltre salvare il valore del membro **wMenuDelta** e usarlo per identificare le voci di menu quando si modifica il menu.</span><span class="sxs-lookup"><span data-stu-id="974a4-115">It should also save the value of the **wMenuDelta** member and use it to identify menu items when modifying the menu.</span></span>

## <a name="requirements"></a><span data-ttu-id="974a4-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="974a4-116">Requirements</span></span>



| <span data-ttu-id="974a4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="974a4-117">Requirement</span></span> | <span data-ttu-id="974a4-118">Valore</span><span class="sxs-lookup"><span data-stu-id="974a4-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="974a4-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="974a4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="974a4-120">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="974a4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="974a4-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="974a4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="974a4-122">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="974a4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="974a4-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="974a4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="974a4-124"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="974a4-124"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="974a4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="974a4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="974a4-126">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="974a4-126">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 
