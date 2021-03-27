---
description: "Consente all'oggetto callback di aggiungere pulsanti alla barra degli strumenti. Usato da IShellFolderViewCB:: MessageSFVCB."
title: Messaggio SFVM_GETBUTTONINFO (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980226"
---
# <a name="sfvm_getbuttoninfo-message"></a><span data-ttu-id="f0ac0-104">\_Messaggio SFVM GETBUTTONINFO</span><span class="sxs-lookup"><span data-stu-id="f0ac0-104">SFVM\_GETBUTTONINFO message</span></span>

<span data-ttu-id="f0ac0-105">Consente all'oggetto callback di aggiungere pulsanti alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f0ac0-105">Allows the callback object to add buttons to the toolbar.</span></span> <span data-ttu-id="f0ac0-106">Usato da [**IShellFolderViewCB:: MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="f0ac0-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a><span data-ttu-id="f0ac0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f0ac0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0ac0-108">*ptbinfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f0ac0-108">*ptbinfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0ac0-109">Indirizzo di una struttura [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) che specifica il numero di pulsanti e il modo in cui devono essere aggiunti alla barra degli strumenti.</span><span class="sxs-lookup"><span data-stu-id="f0ac0-109">The address of a [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) structure that specifies the number of buttons and how they are to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f0ac0-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0ac0-110">Remarks</span></span>

<span data-ttu-id="f0ac0-111">I pulsanti possono essere accodati o anteposti ai pulsanti dell'oggetto visualizzazione cartella di sistema standard o visualizzati al posto dei pulsanti standard.</span><span class="sxs-lookup"><span data-stu-id="f0ac0-111">Buttons can be appended or prepended to the standard system folder view object buttons, or be displayed in place of the standard buttons.</span></span> <span data-ttu-id="f0ac0-112">Questo messaggio è seguito da un [**messaggio \_ getButtons SFVM**](sfvm-getbuttons.md) che recupera le informazioni relative alle specifiche dei pulsanti.</span><span class="sxs-lookup"><span data-stu-id="f0ac0-112">This message is followed by a [**SFVM\_GETBUTTONS**](sfvm-getbuttons.md) message that retrieves the information concerning the button specifics.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0ac0-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f0ac0-113">Requirements</span></span>



| <span data-ttu-id="f0ac0-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0ac0-114">Requirement</span></span> | <span data-ttu-id="f0ac0-115">Valore</span><span class="sxs-lookup"><span data-stu-id="f0ac0-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ac0-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0ac0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f0ac0-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f0ac0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f0ac0-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f0ac0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f0ac0-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f0ac0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f0ac0-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f0ac0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f0ac0-121"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0ac0-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
