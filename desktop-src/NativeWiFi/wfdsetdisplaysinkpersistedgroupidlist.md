---
description: Imposta l'elenco di ID di gruppo permanente per tutti i profili resi permanente dall'app.
ms.assetid: EF83F295-CD53-45A4-B209-560B4069CA7C
title: Funzione WFDDisplaySinkSetPersistedGroupIDList (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDSetDisplaySinkPersistedGroupIDList
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423360d7127f331fd1aa2de7f7370daebcc2b417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309444"
---
# <a name="wfddisplaysinksetpersistedgroupidlist-function"></a><span data-ttu-id="5c82d-103">WFDDisplaySinkSetPersistedGroupIDList (funzione)</span><span class="sxs-lookup"><span data-stu-id="5c82d-103">WFDDisplaySinkSetPersistedGroupIDList function</span></span>

<span data-ttu-id="5c82d-104">Imposta l'elenco di ID di gruppo permanente per tutti i profili resi permanente dall'app.</span><span class="sxs-lookup"><span data-stu-id="5c82d-104">Sets the persisted group id list for all the profiles that are persisted by your app.</span></span> <span data-ttu-id="5c82d-105">L'app deve chiamare questo metodo ogni volta che aggiunge o Elimina un profilo dalla relativa archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5c82d-105">Your app should call this method every time it adds or deletes a profile from its storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c82d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c82d-106">Syntax</span></span>


```C++
DWORD WINAPI WFDSetDisplaySinkPersistedGroupIDList(
  _In_ UINT32             cGroupIDList,
  _In_ DOT11_WFD_GROUP_ID *pGroupIDList
);
```



## <a name="parameters"></a><span data-ttu-id="5c82d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c82d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c82d-108">*cGroupIDList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c82d-108">*cGroupIDList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c82d-109">Numero di ID di gruppo a cui punta *pGroupIDList*.</span><span class="sxs-lookup"><span data-stu-id="5c82d-109">The count of group ids being pointed to by *pGroupIDList*.</span></span>

</dd> <dt>

<span data-ttu-id="5c82d-110">*pGroupIDList* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c82d-110">*pGroupIDList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c82d-111">Puntatore a una matrice di ID di gruppo *cGroupIDList* .</span><span class="sxs-lookup"><span data-stu-id="5c82d-111">Pointer to an array of *cGroupIDList* group ids.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c82d-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c82d-112">Return value</span></span>

<span data-ttu-id="5c82d-113">Se la funzione ha esito positivo, il valore restituito è ERROR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="5c82d-113">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c82d-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c82d-114">Remarks</span></span>

<span data-ttu-id="5c82d-115">Questo metodo deve essere sempre chiamato con l'intero elenco e non con un subset.</span><span class="sxs-lookup"><span data-stu-id="5c82d-115">This method is always expected to be called with the entire list, and not a subset.</span></span> <span data-ttu-id="5c82d-116">Quando l'archivio del profilo è vuoto, è possibile chiamare questo metodo con 0 profili.</span><span class="sxs-lookup"><span data-stu-id="5c82d-116">It is OK to call this method with 0 profiles when the profile store is empty.</span></span>

<span data-ttu-id="5c82d-117">Un nuovo richiamo per un ID gruppo che non fa parte dell'elenco fornito avrà esito negativo con "errore; Gruppo P2P sconosciuto "(stato 8).</span><span class="sxs-lookup"><span data-stu-id="5c82d-117">A re-invoke for a group id that is not part of the provided list will fail with "Fail; unknown P2P Group"(status 8).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c82d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c82d-118">Requirements</span></span>



| <span data-ttu-id="5c82d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c82d-119">Requirement</span></span> | <span data-ttu-id="5c82d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="5c82d-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c82d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c82d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5c82d-122">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="5c82d-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5c82d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c82d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5c82d-124">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="5c82d-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5c82d-125">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="5c82d-125">End of client support</span></span><br/>    | <span data-ttu-id="5c82d-126">Windows 10</span><span class="sxs-lookup"><span data-stu-id="5c82d-126">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="5c82d-127">Fine del supporto server</span><span class="sxs-lookup"><span data-stu-id="5c82d-127">End of server support</span></span><br/>    | <span data-ttu-id="5c82d-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="5c82d-128">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="5c82d-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c82d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c82d-130"><dt>Wfdsink. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c82d-130"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="5c82d-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c82d-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="5c82d-132"><dt>Wifidisplay. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c82d-132"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="5c82d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5c82d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c82d-134"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c82d-134"><dt>Wifidisplay.dll</dt></span></span> </dl> |



 

 




