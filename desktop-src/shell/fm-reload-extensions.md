---
description: Inviato da un'estensione di file Manager (o un'altra applicazione) per fare in modo che file Manager ricarichi tutte le DLL di estensione elencate nella \[ \] sezione addons del file Winfile.ini.
ms.assetid: 5103a986-5f45-4deb-aaae-c6e87cb60051
title: Messaggio FM_RELOAD_EXTENSIONS (Wfext. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FM_RELOAD_EXTENSIONS
api_type:
- HeaderDef
api_location:
- Wfext.h
ms.openlocfilehash: 9e82ec9ec638cb70cc7b571ed9e5e76d604cd4da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979714"
---
# <a name="fm_reload_extensions-message"></a><span data-ttu-id="7a18e-103">\_Messaggio estensioni di RIcaricamento FM \_</span><span class="sxs-lookup"><span data-stu-id="7a18e-103">FM\_RELOAD\_EXTENSIONS message</span></span>

<span data-ttu-id="7a18e-104">Inviato da un'estensione di file Manager (o un'altra applicazione) per fare in modo che file Manager ricarichi tutte le DLL di estensione elencate nella \[ \] sezione addons del file Winfile.ini.</span><span class="sxs-lookup"><span data-stu-id="7a18e-104">Sent by a File Manager extension (or another application) to cause File Manager to reload all extension DLLs listed in the \[AddOns\] section of the Winfile.ini file.</span></span>

## <a name="parameters"></a><span data-ttu-id="7a18e-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a18e-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a18e-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7a18e-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a18e-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7a18e-107">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7a18e-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7a18e-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7a18e-109">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7a18e-109">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a18e-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7a18e-110">Return value</span></span>

<span data-ttu-id="7a18e-111">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="7a18e-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a18e-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a18e-112">Remarks</span></span>

<span data-ttu-id="7a18e-113">Altre applicazioni possono utilizzare la funzione [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) per inviare questo messaggio a gestione file.</span><span class="sxs-lookup"><span data-stu-id="7a18e-113">Other applications can use the [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) function to send this message to File Manager.</span></span> <span data-ttu-id="7a18e-114">Per ottenere l'handle di finestra del file Manager appropriato, un'applicazione può specificare "WFS \_ frame" come parametro *lpszClassName* in una chiamata alla funzione [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) .</span><span class="sxs-lookup"><span data-stu-id="7a18e-114">To obtain the appropriate File Manager window handle, an application can specify "WFS\_Frame" as the *lpszClassName* parameter in a call to the [**FindWindow**](/windows/win32/api/winuser/nf-winuser-findwindowa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a18e-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a18e-115">Requirements</span></span>



| <span data-ttu-id="7a18e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a18e-116">Requirement</span></span> | <span data-ttu-id="7a18e-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7a18e-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7a18e-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a18e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7a18e-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7a18e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="7a18e-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a18e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7a18e-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7a18e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7a18e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7a18e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a18e-123"><dt>Wfext. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a18e-123"><dt>Wfext.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a18e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a18e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a18e-125">**FMExtensionProc**</span><span class="sxs-lookup"><span data-stu-id="7a18e-125">**FMExtensionProc**</span></span>](fmextensionproc.md)
</dt> </dl>

 

 
