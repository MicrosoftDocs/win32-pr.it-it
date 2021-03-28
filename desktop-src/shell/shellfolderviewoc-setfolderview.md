---
description: Invia gli eventi dell'oggetto ShellFolderView specificato al gestore eventi ShellFolderViewOC corrispondente.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: Metodo ShellFolderViewOC. SetFolderView (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980423"
---
# <a name="shellfolderviewocsetfolderview-method"></a><span data-ttu-id="b1c8a-103">ShellFolderViewOC. SetFolderView, metodo</span><span class="sxs-lookup"><span data-stu-id="b1c8a-103">ShellFolderViewOC.SetFolderView method</span></span>

<span data-ttu-id="b1c8a-104">Invia gli eventi dell'oggetto [**ShellFolderView**](shellfolderview.md) specificato al gestore eventi [**ShellFolderViewOC**](shellfolderviewoc-object.md) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b1c8a-104">Forwards the events of the specified [**ShellFolderView**](shellfolderview.md) object to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1c8a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b1c8a-105">Syntax</span></span>


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a><span data-ttu-id="b1c8a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b1c8a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1c8a-107">*oShellFolderView* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b1c8a-107">*oShellFolderView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1c8a-108">Tipo: \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) \** _</span><span class="sxs-lookup"><span data-stu-id="b1c8a-108">Type: \**[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\** _</span></span>

<span data-ttu-id="b1c8a-109">Oggetto [_ *ShellFolderView* \*](shellfolderview.md) .</span><span class="sxs-lookup"><span data-stu-id="b1c8a-109">A [_ *ShellFolderView*\*](shellfolderview.md) object.</span></span> <span data-ttu-id="b1c8a-110">Gli eventi [**EnumDone**](shellfolderviewoc-enumdone.md) e [**SelectionChanged**](shellfolderview-selectionchanged.md) verranno trasmessi al gestore eventi [**ShellFolderViewOC**](shellfolderviewoc-object.md) corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b1c8a-110">Its [**EnumDone**](shellfolderviewoc-enumdone.md) and [**SelectionChanged**](shellfolderview-selectionchanged.md) events will be forwarded to the corresponding [**ShellFolderViewOC**](shellfolderviewoc-object.md) event handler.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b1c8a-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1c8a-111">Requirements</span></span>



| <span data-ttu-id="b1c8a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1c8a-112">Requirement</span></span> | <span data-ttu-id="b1c8a-113">Valore</span><span class="sxs-lookup"><span data-stu-id="b1c8a-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1c8a-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1c8a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="b1c8a-115">Windows 2000 Professional, \[ solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b1c8a-115">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1c8a-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1c8a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="b1c8a-117">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b1c8a-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="b1c8a-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1c8a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1c8a-119"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1c8a-119"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="b1c8a-120">IDL</span><span class="sxs-lookup"><span data-stu-id="b1c8a-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1c8a-121"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1c8a-121"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="b1c8a-122">DLL</span><span class="sxs-lookup"><span data-stu-id="b1c8a-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1c8a-123"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="b1c8a-123"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



 

 
