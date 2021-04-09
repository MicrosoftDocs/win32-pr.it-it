---
title: Messaggio di MCIWNDM_OPEN (VFW. h)
description: Il \_ messaggio aperto MCIWNDM apre un dispositivo MCI e lo associa a una finestra di MCIWnd.
ms.assetid: ad1dfe0f-015b-45a9-ab88-cc0bdf0aa057
keywords:
- MCIWNDM_OPEN messaggi multimediali di Windows
topic_type:
- apiref
api_name:
- MCIWNDM_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2f232ea9076a1e0ff8c105d8c5cf94104e455c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119542"
---
# <a name="mciwndm_open-message"></a><span data-ttu-id="3c1c6-104">MCIWNDM \_ messaggio aperto</span><span class="sxs-lookup"><span data-stu-id="3c1c6-104">MCIWNDM\_OPEN message</span></span>

<span data-ttu-id="3c1c6-105">Il **messaggio \_ aperto MCIWNDM** apre un dispositivo MCI e lo associa a una finestra di MCIWnd.</span><span class="sxs-lookup"><span data-stu-id="3c1c6-105">The **MCIWNDM\_OPEN** message opens an MCI device and associates it with an MCIWnd window.</span></span> <span data-ttu-id="3c1c6-106">Per i dispositivi MCI che usano file di dati, questa macro può anche aprire un file di dati specificato, denominare un nuovo file da creare o visualizzare una finestra di dialogo per consentire all'utente di selezionare un file da aprire.</span><span class="sxs-lookup"><span data-stu-id="3c1c6-106">For MCI devices that use data files, this macro can also open a specified data file, name a new file to be created, or display a dialog box to let the user select a file to open.</span></span> <span data-ttu-id="3c1c6-107">È possibile inviare questo messaggio in modo esplicito o utilizzando la macro [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) .</span><span class="sxs-lookup"><span data-stu-id="3c1c6-107">You can send this message explicitly or by using the [**MCIWndOpen**](/windows/desktop/api/Vfw/nf-vfw-mciwndopen) macro.</span></span>


```C++
MCIWNDM_OPEN 
wParam = (WPARAM) (UINT) wFlags; 
lParam = (LPARAM) (LPVOID) szFile; 
```



## <a name="parameters"></a><span data-ttu-id="3c1c6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c1c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c1c6-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span><span class="sxs-lookup"><span data-stu-id="3c1c6-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="3c1c6-110">Flag associati al dispositivo o al file da aprire.</span><span class="sxs-lookup"><span data-stu-id="3c1c6-110">Flags associated with the device or file to open.</span></span> <span data-ttu-id="3c1c6-111">Il \_ nuovo flag MCIWNDOPENF specifica che è necessario creare un nuovo file con il nome specificato in **szFile**.</span><span class="sxs-lookup"><span data-stu-id="3c1c6-111">The MCIWNDOPENF\_NEW flag specifies a new file is to be created with the name specified in **szFile**.</span></span>

</dd> <dt>

<span data-ttu-id="3c1c6-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*</span><span class="sxs-lookup"><span data-stu-id="3c1c6-112"><span id="szFile"></span><span id="szfile"></span><span id="SZFILE"></span>*szFile*</span></span>
</dt> <dd>

<span data-ttu-id="3c1c6-113">Puntatore a una stringa con terminazione null che identifica il nome file o il nome del dispositivo MCI da aprire.</span><span class="sxs-lookup"><span data-stu-id="3c1c6-113">Pointer to a null-terminated string identifying the filename or MCI device name to open.</span></span> <span data-ttu-id="3c1c6-114">Specificare 1 per questo parametro per visualizzare la finestra di dialogo Apri.</span><span class="sxs-lookup"><span data-stu-id="3c1c6-114">Specify  1 for this parameter to display the Open dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c1c6-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c1c6-115">Return Value</span></span>

<span data-ttu-id="3c1c6-116">Restituisce zero in caso di esito positivo o un errore.</span><span class="sxs-lookup"><span data-stu-id="3c1c6-116">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c1c6-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c1c6-117">Requirements</span></span>



| <span data-ttu-id="3c1c6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c1c6-118">Requirement</span></span> | <span data-ttu-id="3c1c6-119">Valore</span><span class="sxs-lookup"><span data-stu-id="3c1c6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3c1c6-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c1c6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3c1c6-121">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c1c6-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3c1c6-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c1c6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3c1c6-123">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3c1c6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3c1c6-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c1c6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c1c6-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c1c6-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c1c6-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c1c6-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c1c6-127">**MCIWndOpen**</span><span class="sxs-lookup"><span data-stu-id="3c1c6-127">**MCIWndOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndopen)
</dt> </dl>

 

 





