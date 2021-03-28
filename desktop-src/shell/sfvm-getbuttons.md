---
description: "Consente all'oggetto callback di specificare i pulsanti da aggiungere alla barra degli strumenti. Usato da IShellFolderViewCB:: MessageSFVCB."
ms.assetid: 0c0dbf61-9da9-4bcc-bad9-92c3f78db78f
title: Messaggio SFVM_GETBUTTONS (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ad4ced86909c37ec77bf0470b46a40954f5b61c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103883425"
---
# <a name="sfvm_getbuttons-message"></a><span data-ttu-id="26581-104">\_Messaggio GETbuttons SFVM</span><span class="sxs-lookup"><span data-stu-id="26581-104">SFVM\_GETBUTTONS message</span></span>

<span data-ttu-id="26581-105">Consente all'oggetto callback di specificare i pulsanti da aggiungere alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="26581-105">Allows the callback object to specify the buttons to be added to the toolbar.</span></span> <span data-ttu-id="26581-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="26581-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONS 

    wParam = (WPARAM)(DWORD) idCmdFirst,cbtnMax;

    lParam = (LPARAM)(LPTBBUTTON) pbtn;

            
```



## <a name="parameters"></a><span data-ttu-id="26581-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="26581-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26581-108">*idCmdFirst \_ cbtnMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="26581-108">*idCmdFirst\_cbtnMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26581-109">Contiene i valori a 2 16 bit compressi nel parametro con la macro [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) .</span><span class="sxs-lookup"><span data-stu-id="26581-109">Contains two 16-bit values packed into the parameter with the [**MAKEWPARAM**](/windows/win32/api/winuser/nf-winuser-makewparam) macro.</span></span> <span data-ttu-id="26581-110">La parola di ordine inferiore contiene l'ID del comando iniziale.</span><span class="sxs-lookup"><span data-stu-id="26581-110">The low-order word contains the initial command ID.</span></span> <span data-ttu-id="26581-111">La parola di ordine superiore contiene il numero di pulsanti da aggiungere, come specificato nel messaggio [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) precedente.</span><span class="sxs-lookup"><span data-stu-id="26581-111">The high-order word contains the number of buttons to be added, as specified in the preceding [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span>

</dd> <dt>

<span data-ttu-id="26581-112">*pBtn* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="26581-112">*pbtn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26581-113">Indirizzo di una matrice di strutture [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) , una per ogni pulsante da aggiungere alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="26581-113">The address of an array of [**TBBUTTON**](/windows/win32/api/commctrl/ns-commctrl-tbbutton) structures, one for each button to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="26581-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="26581-114">Remarks</span></span>

<span data-ttu-id="26581-115">Questo messaggio è preceduto da un messaggio [**SFVM \_ GETBUTTONINFO**](sfvm-getbuttoninfo.md) .</span><span class="sxs-lookup"><span data-stu-id="26581-115">This message is preceded by a [**SFVM\_GETBUTTONINFO**](sfvm-getbuttoninfo.md) message.</span></span> <span data-ttu-id="26581-116">L'oggetto callback deve gestire il messaggio per specificare il numero di pulsanti e la posizione in cui devono essere posizionati sulla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="26581-116">The callback object must handle that message to specify the number of buttons and where they are to be placed on the toolbar.</span></span> <span data-ttu-id="26581-117">A seconda del modo in cui l'oggetto callback risponde al messaggio **SFVM \_ GETBUTTONINFO** , i pulsanti specificati dal parametro *pBtn* verranno accodati o anteposti ai pulsanti standard dell'oggetto visualizzazione cartella di sistema o sostituiranno il set standard.</span><span class="sxs-lookup"><span data-stu-id="26581-117">Depending on how the callback object responds to the **SFVM\_GETBUTTONINFO** message, the buttons specified by *pbtn* parameter will be appended or prepended to the system folder view object's standard buttons, or replace the standard set.</span></span>

## <a name="requirements"></a><span data-ttu-id="26581-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26581-118">Requirements</span></span>



| <span data-ttu-id="26581-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="26581-119">Requirement</span></span> | <span data-ttu-id="26581-120">Valore</span><span class="sxs-lookup"><span data-stu-id="26581-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="26581-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26581-121">Minimum supported client</span></span><br/> | <span data-ttu-id="26581-122">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26581-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="26581-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26581-123">Minimum supported server</span></span><br/> | <span data-ttu-id="26581-124">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26581-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="26581-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="26581-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="26581-126"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="26581-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
