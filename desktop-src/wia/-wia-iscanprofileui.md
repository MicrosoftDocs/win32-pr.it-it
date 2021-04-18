---
description: L'interfaccia IScanProfileUI consente alle applicazioni di visualizzare una finestra di dialogo in modo che gli utenti possano creare, modificare ed eliminare i profili di analisi.
ms.assetid: d0c7edcc-00d8-49b2-a0f7-fe4bbba90bfb
title: Interfaccia IScanProfileUI (Scanprofileui. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileUI
api_type:
- COM
api_location:
- Scanprofileui.h
ms.openlocfilehash: c8791461db76c72de81216aef188886f63fde4f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308248"
---
# <a name="iscanprofileui-interface"></a><span data-ttu-id="c0bc0-103">Interfaccia IScanProfileUI</span><span class="sxs-lookup"><span data-stu-id="c0bc0-103">IScanProfileUI interface</span></span>

<span data-ttu-id="c0bc0-104">L'interfaccia **IScanProfileUI** consente alle applicazioni di visualizzare una finestra di dialogo in modo che gli utenti possano creare, modificare ed eliminare i profili di analisi.</span><span class="sxs-lookup"><span data-stu-id="c0bc0-104">The **IScanProfileUI** interface enables applications to display a dialog box so that users can create, modify, and delete scan profiles.</span></span>

## <a name="members"></a><span data-ttu-id="c0bc0-105">Membri</span><span class="sxs-lookup"><span data-stu-id="c0bc0-105">Members</span></span>

<span data-ttu-id="c0bc0-106">L'interfaccia **IScanProfileUI** eredita dall'interfaccia [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="c0bc0-106">The **IScanProfileUI** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="c0bc0-107">**IScanProfileUI** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="c0bc0-107">**IScanProfileUI** also has these types of members:</span></span>

-   [<span data-ttu-id="c0bc0-108">Metodi</span><span class="sxs-lookup"><span data-stu-id="c0bc0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c0bc0-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="c0bc0-109">Methods</span></span>

<span data-ttu-id="c0bc0-110">L'interfaccia **IScanProfileUI** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="c0bc0-110">The **IScanProfileUI** interface has these methods.</span></span>



| <span data-ttu-id="c0bc0-111">Metodo</span><span class="sxs-lookup"><span data-stu-id="c0bc0-111">Method</span></span>                                                             | <span data-ttu-id="c0bc0-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c0bc0-112">Description</span></span>                                                                                      |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c0bc0-113">**ScanProfileDialog**</span><span class="sxs-lookup"><span data-stu-id="c0bc0-113">**ScanProfileDialog**</span></span>](-wia-iscanprofileui-scanprofiledialog.md) | <span data-ttu-id="c0bc0-114">Visualizza una finestra di dialogo che consente agli utenti di creare, modificare ed eliminare i profili di analisi.</span><span class="sxs-lookup"><span data-stu-id="c0bc0-114">Displays a dialog box that enables users to create, modify, and delete scan profiles.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0bc0-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c0bc0-115">Remarks</span></span>

<span data-ttu-id="c0bc0-116">La finestra di dialogo è modale. l'utente non può passare alla finestra padre fino alla chiusura della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="c0bc0-116">The dialog box is modal; the user cannot switch to the parent window until the dialog box closes.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0bc0-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c0bc0-117">Requirements</span></span>



| <span data-ttu-id="c0bc0-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0bc0-118">Requirement</span></span> | <span data-ttu-id="c0bc0-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c0bc0-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0bc0-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0bc0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c0bc0-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c0bc0-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="c0bc0-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c0bc0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c0bc0-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c0bc0-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c0bc0-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c0bc0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0bc0-125"><dt>Scanprofileui. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0bc0-125"><dt>Scanprofileui.h</dt></span></span> </dl>  |
| <span data-ttu-id="c0bc0-126">IDL</span><span class="sxs-lookup"><span data-stu-id="c0bc0-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c0bc0-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c0bc0-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0bc0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c0bc0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0bc0-129">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="c0bc0-129">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="c0bc0-130">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="c0bc0-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 
