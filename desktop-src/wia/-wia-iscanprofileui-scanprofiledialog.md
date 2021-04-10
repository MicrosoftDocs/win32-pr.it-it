---
description: Visualizza una finestra di dialogo che consente agli utenti di creare, modificare ed eliminare i profili di analisi.
ms.assetid: 208ec527-f7ad-4d45-b433-6d7d3658ca26
title: 'Metodo IScanProfileUI:: ScanProfileDialog (Scanprofileui. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI.ScanProfileDialog
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: bc8707378f1debc322fea258ceb8aad0c6400ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231555"
---
# <a name="iscanprofileuiscanprofiledialog-method"></a><span data-ttu-id="03c97-103">Metodo IScanProfileUI:: ScanProfileDialog</span><span class="sxs-lookup"><span data-stu-id="03c97-103">IScanProfileUI::ScanProfileDialog method</span></span>

<span data-ttu-id="03c97-104">Visualizza una finestra di dialogo che consente agli utenti di creare, modificare ed eliminare i profili di analisi.</span><span class="sxs-lookup"><span data-stu-id="03c97-104">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span>

## <a name="syntax"></a><span data-ttu-id="03c97-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03c97-105">Syntax</span></span>


```C++
HRESULT ScanProfileDialog(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="03c97-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="03c97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03c97-107">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03c97-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03c97-108">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="03c97-108">Type: **HWND**</span></span>

<span data-ttu-id="03c97-109">Handle della finestra padre proprietario della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="03c97-109">The handle of the parent window that owns the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03c97-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03c97-110">Return value</span></span>

<span data-ttu-id="03c97-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="03c97-111">Type: **HRESULT**</span></span>

<span data-ttu-id="03c97-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="03c97-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="03c97-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="03c97-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="03c97-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="03c97-114">Remarks</span></span>

<span data-ttu-id="03c97-115">La finestra di dialogo è modale. l'utente non può passare alla finestra padre fino alla chiusura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="03c97-115">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

<span data-ttu-id="03c97-116">I valori dell' `<ProfileName>` elemento e dell' `<WiaItem>` elemento possono essere modificati nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="03c97-116">The values of the `<ProfileName>` element and the `<WiaItem>` element can be changed in the dialog box.</span></span> <span data-ttu-id="03c97-117">L' `<Default>` elemento può essere aggiunto o eliminato.</span><span class="sxs-lookup"><span data-stu-id="03c97-117">The `<Default>` element can be added or deleted.</span></span> <span data-ttu-id="03c97-118">Non è possibile apportare altre modifiche al profilo di analisi nella finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="03c97-118">No other changes to the scan profile can be made in the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="03c97-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03c97-119">Requirements</span></span>



| <span data-ttu-id="03c97-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="03c97-120">Requirement</span></span> | <span data-ttu-id="03c97-121">Valore</span><span class="sxs-lookup"><span data-stu-id="03c97-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="03c97-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03c97-122">Minimum supported client</span></span><br/> | <span data-ttu-id="03c97-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="03c97-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="03c97-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="03c97-124">Minimum supported server</span></span><br/> | <span data-ttu-id="03c97-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="03c97-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="03c97-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03c97-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="03c97-127"><dt>Scanprofileui. h</dt></span><span class="sxs-lookup"><span data-stu-id="03c97-127"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="03c97-128">IDL</span><span class="sxs-lookup"><span data-stu-id="03c97-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="03c97-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="03c97-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03c97-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03c97-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03c97-131">**IScanProfileUI**</span><span class="sxs-lookup"><span data-stu-id="03c97-131">**IScanProfileUI**</span></span>](-wia-iscanprofileui.md)
</dt> <dt>

[<span data-ttu-id="03c97-132">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="03c97-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




