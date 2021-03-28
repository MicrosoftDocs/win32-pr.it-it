---
description: Inviato dall'implementazione del menu di scelta rapida predefinito durante la creazione, specificando il comando di menu predefinito e consentendo di eseguire una scelta alternativa. Usato da LPFNDFMCALLBACK.
title: Messaggio DFM_GETDEFSTATICID (Shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9e4ad96e-7c90-456e-8668-21b347f2915c
api_name:
- DFM_GETDEFSTATICID
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3fb1635b624b4c39e91ad8c31645c9aad598c7fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401619"
---
# <a name="dfm_getdefstaticid-message"></a><span data-ttu-id="789a5-104">\_Messaggio DFM GETDEFSTATICID</span><span class="sxs-lookup"><span data-stu-id="789a5-104">DFM\_GETDEFSTATICID message</span></span>

<span data-ttu-id="789a5-105">Inviato dall'implementazione del menu di scelta rapida predefinito durante la creazione, specificando il comando di menu predefinito e consentendo di eseguire una scelta alternativa.</span><span class="sxs-lookup"><span data-stu-id="789a5-105">Sent by the default context menu implementation during creation, specifying the default menu command and allowing an alternate choice to be made.</span></span> <span data-ttu-id="789a5-106">Usato da [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).</span><span class="sxs-lookup"><span data-stu-id="789a5-106">Used by [**LPFNDFMCALLBACK**](/windows/win32/api/shlobj_core/nc-shlobj_core-lpfndfmcallback).</span></span>


```C++
DFM_GETDEFSTATICID
    lParam = (LPARAM)(int*) defaultID;          
            
```



## <a name="parameters"></a><span data-ttu-id="789a5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="789a5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="789a5-108">*defaultID* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="789a5-108">*defaultID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="789a5-109">Puntatore all'ID del comando di menu selezionato.</span><span class="sxs-lookup"><span data-stu-id="789a5-109">A pointer to the ID of the selected menu command.</span></span> <span data-ttu-id="789a5-110">Viene riconosciuto il seguente flag.</span><span class="sxs-lookup"><span data-stu-id="789a5-110">The following flag is recognized.</span></span>

<dt>

<span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>

<span data-ttu-id="789a5-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**\_Proprietà cmd \_ DFM**</span><span class="sxs-lookup"><span data-stu-id="789a5-111"><span id="DFM_CMD_PROPERTIES"></span><span id="dfm_cmd_properties"></span>**DFM\_CMD\_PROPERTIES**</span></span>


</dt> <dd>

<span data-ttu-id="789a5-112">Mostra l'interfaccia utente delle **Proprietà** per l'elemento su cui è stato richiamato il menu.</span><span class="sxs-lookup"><span data-stu-id="789a5-112">Show the **Properties** UI for the item the menu was invoked on.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="789a5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="789a5-113">Remarks</span></span>

<span data-ttu-id="789a5-114">Per eseguire l'override della scelta del comando predefinita, il gestore deve, al momento della ricezione del messaggio, impostare il valore a cui punta *defaultID* sull'ID del comando di sostituzione e restituire S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="789a5-114">To override the default command choice, your handler should, upon receipt of this message, set the value pointed to by *defaultID* to the ID of the replacement command and return S\_OK.</span></span> <span data-ttu-id="789a5-115">Restituisce un codice di errore in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="789a5-115">Return a failure code otherwise.</span></span>

<span data-ttu-id="789a5-116">Questo messaggio viene inviato alla funzione di callback o all'oggetto callback a seconda del modo in cui viene costruito l'oggetto menu di scelta rapida predefinito.</span><span class="sxs-lookup"><span data-stu-id="789a5-116">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="789a5-117">Sono disponibili due API per la relativa costruzione, [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span><span class="sxs-lookup"><span data-stu-id="789a5-117">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="789a5-118">[**DFM \_ INVOKECOMMANDEX**](dfm-invokecommandex.md) è una versione estesa di questo messaggio e fornisce ulteriori informazioni al callback.</span><span class="sxs-lookup"><span data-stu-id="789a5-118">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="789a5-119">Usare **DFM \_ INVOKECOMMANDEX** se nell'implementazione sono necessarie informazioni aggiuntive fornite da tale interfaccia.</span><span class="sxs-lookup"><span data-stu-id="789a5-119">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="789a5-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="789a5-120">Requirements</span></span>



| <span data-ttu-id="789a5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="789a5-121">Requirement</span></span> | <span data-ttu-id="789a5-122">Valore</span><span class="sxs-lookup"><span data-stu-id="789a5-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="789a5-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="789a5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="789a5-124">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="789a5-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="789a5-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="789a5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="789a5-126">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="789a5-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="789a5-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="789a5-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="789a5-128"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="789a5-128"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
