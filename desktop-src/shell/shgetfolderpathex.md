---
UID: ''
title: SHGetFolderPathEx (funzione)
description: Recupera il percorso di una cartella nota identificata da KNOWNFOLDERID.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: SHGetFolderPath
ms.topic: reference
req.header: Shlobj.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Shell32.lib
req.dll: API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Storage-Exports-Internal-L1-1-0.dll
api_name:
- SHGetFolderPathEx
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 0dfc3342f3eca5622c25d2df7319cd2323f516ff
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2020
ms.locfileid: "104976575"
---
# <a name="shgetfolderpathex-function"></a><span data-ttu-id="1c199-103">SHGetFolderPathEx (funzione)</span><span class="sxs-lookup"><span data-stu-id="1c199-103">SHGetFolderPathEx function</span></span>

## <a name="description"></a><span data-ttu-id="1c199-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c199-104">Description</span></span>

<span data-ttu-id="1c199-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="1c199-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span>
<span data-ttu-id="1c199-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="1c199-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1c199-107">Recupera il percorso completo di una cartella nota identificata dal [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid)della cartella.</span><span class="sxs-lookup"><span data-stu-id="1c199-107">Retrieves the full path of a known folder identified by the folder's [KNOWNFOLDERID](/windows/desktop/shell/knownfolderid).</span></span>
<span data-ttu-id="1c199-108">Questo consente di estendere [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) consentendo di impostare la dimensione iniziale del buffer di stringa.</span><span class="sxs-lookup"><span data-stu-id="1c199-108">This extends [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) by allowing you to set the initial size of the string buffer.</span></span>

```cpp
HRESULT WINAPI SHGetFolderPathEx(
  _In_     REFKNOWNFOLDERID rfid,
  _In_     DWORD            dwFlags,
  _In_opt_ HANDLE           hToken,
  _Out_    LPWSTR           pszPath,
  _In_     UINT             cchPath
);
```

## <a name="parameters"></a><span data-ttu-id="1c199-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1c199-109">Parameters</span></span>

### <a name="rfid-in"></a><span data-ttu-id="1c199-110">RFID [in]</span><span class="sxs-lookup"><span data-stu-id="1c199-110">rfid [in]</span></span>

<span data-ttu-id="1c199-111">Riferimento a **KNOWNFOLDERID** che identifica la cartella.</span><span class="sxs-lookup"><span data-stu-id="1c199-111">A reference to the **KNOWNFOLDERID** that identifies the folder.</span></span>

### <a name="dwflags-in"></a><span data-ttu-id="1c199-112">dwFlags [in]</span><span class="sxs-lookup"><span data-stu-id="1c199-112">dwFlags [in]</span></span>

<span data-ttu-id="1c199-113">Flag che specificano opzioni di recupero speciali.</span><span class="sxs-lookup"><span data-stu-id="1c199-113">Flags that specify special retrieval options.</span></span>
<span data-ttu-id="1c199-114">Questo valore può essere 0. in caso contrario, uno o più valori [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) .</span><span class="sxs-lookup"><span data-stu-id="1c199-114">This value can be 0; otherwise, one or more of the [KNOWN_FOLDER_FLAG](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag) values.</span></span>

### <a name="htoken-in-optional"></a><span data-ttu-id="1c199-115">hToken [in, optional]</span><span class="sxs-lookup"><span data-stu-id="1c199-115">hToken [in, optional]</span></span>

<span data-ttu-id="1c199-116">Un [token di accesso](/windows/desktop/SecAuthZ/access-tokens) che rappresenta un utente specifico.</span><span class="sxs-lookup"><span data-stu-id="1c199-116">An [access token](/windows/desktop/SecAuthZ/access-tokens) that represents a particular user.</span></span>
<span data-ttu-id="1c199-117">Se questo parametro è **null**, ovvero l'utilizzo più comune, la funzione richiede la cartella nota per l'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="1c199-117">If this parameter is **NULL**, which is the most common usage, the function requests the known folder for the current user.</span></span>

<span data-ttu-id="1c199-118">Richiedere la cartella di un utente specifico passando il *hToken* dell'utente.</span><span class="sxs-lookup"><span data-stu-id="1c199-118">Request a specific user's folder by passing the *hToken* of that user.</span></span>
<span data-ttu-id="1c199-119">Questa operazione viene in genere eseguita nel contesto di un servizio con privilegi sufficienti per recuperare il token di un determinato utente.</span><span class="sxs-lookup"><span data-stu-id="1c199-119">This is typically done in the context of a service that has sufficient privileges to retrieve the token of a given user.</span></span>
<span data-ttu-id="1c199-120">Il token deve essere aperto con diritti [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) e [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) .</span><span class="sxs-lookup"><span data-stu-id="1c199-120">That token must be opened with [TOKEN_QUERY](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) and [TOKEN_IMPERSONATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects) rights.</span></span>
<span data-ttu-id="1c199-121">In alcuni casi, è necessario includere anche [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).</span><span class="sxs-lookup"><span data-stu-id="1c199-121">In some cases, you also need to include [TOKEN_DUPLICATE](/windows/desktop/SecAuthZ/access-rights-for-access-token-objects).</span></span>
<span data-ttu-id="1c199-122">Oltre a passare il *hToken* dell'utente, è necessario montare l'hive del registro di sistema dell'utente specifico.</span><span class="sxs-lookup"><span data-stu-id="1c199-122">In addition to passing the user's *hToken*, the registry hive of that specific user must be mounted.</span></span>
<span data-ttu-id="1c199-123">Per ulteriori informazioni sui problemi di controllo degli accessi, vedere [controllo di accesso](/windows/desktop/SecAuthZ/access-control) .</span><span class="sxs-lookup"><span data-stu-id="1c199-123">See [Access Control](/windows/desktop/SecAuthZ/access-control) for further discussion of access control issues.</span></span>

<span data-ttu-id="1c199-124">Se si assegna il parametro *hToken* , il valore-1 indica l'utente predefinito.</span><span class="sxs-lookup"><span data-stu-id="1c199-124">Assigning the *hToken* parameter a value of -1 indicates the Default User.</span></span>
<span data-ttu-id="1c199-125">Questo consente ai client di [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) di trovare i percorsi delle cartelle, ad esempio la cartella **Desktop** , per l'utente predefinito.</span><span class="sxs-lookup"><span data-stu-id="1c199-125">This allows clients of [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) to find folder locations (such as the **Desktop** folder) for the Default User.</span></span>
<span data-ttu-id="1c199-126">Il profilo utente predefinito viene duplicato quando viene creato un nuovo account utente e include cartelle speciali, ad esempio **documenti** e **Desktop**.</span><span class="sxs-lookup"><span data-stu-id="1c199-126">The Default User user profile is duplicated when any new user account is created, and includes special folders such as **Documents** and **Desktop**.</span></span>
<span data-ttu-id="1c199-127">Tutti gli elementi aggiunti alla cartella utente predefinita vengono visualizzati anche in qualsiasi nuovo account utente.</span><span class="sxs-lookup"><span data-stu-id="1c199-127">Any items added to the Default User folder also appear in any new user account.</span></span>
<span data-ttu-id="1c199-128">Si noti che per l'accesso alle cartelle utente predefinite sono necessari i privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="1c199-128">Note that access to the Default User folders requires administrator privileges.</span></span>

### <a name="pszpath-out"></a><span data-ttu-id="1c199-129">pszPath [out]</span><span class="sxs-lookup"><span data-stu-id="1c199-129">pszPath [out]</span></span>

<span data-ttu-id="1c199-130">Stringa Unicode con terminazione null.</span><span class="sxs-lookup"><span data-stu-id="1c199-130">A null-terminated, Unicode string.</span></span>
<span data-ttu-id="1c199-131">Il buffer deve essere di dimensioni cchPath.</span><span class="sxs-lookup"><span data-stu-id="1c199-131">This buffer must be of size cchPath.</span></span>
<span data-ttu-id="1c199-132">Quando **SHGetFolderPathEx** viene restituito correttamente, questo parametro contiene il percorso della cartella nota.</span><span class="sxs-lookup"><span data-stu-id="1c199-132">When **SHGetFolderPathEx** returns successfully, this parameter contains the path for the known folder.</span></span>

### <a name="cchpath-in"></a><span data-ttu-id="1c199-133">cchPath [in]</span><span class="sxs-lookup"><span data-stu-id="1c199-133">cchPath [in]</span></span>

<span data-ttu-id="1c199-134">Dimensioni del buffer *ppszPath* , in caratteri.</span><span class="sxs-lookup"><span data-stu-id="1c199-134">The size of the *ppszPath* buffer, in characters.</span></span>

## <a name="returns"></a><span data-ttu-id="1c199-135">Restituisce</span><span class="sxs-lookup"><span data-stu-id="1c199-135">Returns</span></span>

<span data-ttu-id="1c199-136">Restituisce **S_OK** in caso di esito positivo o un valore di errore.</span><span class="sxs-lookup"><span data-stu-id="1c199-136">Returns **S_OK** if successful, or an error value otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c199-137">Commenti</span><span class="sxs-lookup"><span data-stu-id="1c199-137">Remarks</span></span>

<span data-ttu-id="1c199-138">Poiché [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) è un wrapper per [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), questa funzione (**SHGetFolderPathEx**) funge anche da estensione per **SHGetFolderPath**.</span><span class="sxs-lookup"><span data-stu-id="1c199-138">Since [SHGetFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) is a wrapper for [SHGetKnownFolderPath](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath), this function (**SHGetFolderPathEx**) also serves as an extension to **SHGetFolderPath**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c199-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1c199-139">See also</span></span>

[<span data-ttu-id="1c199-140">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="1c199-140">KNOWNFOLDERID</span></span>](/windows/desktop/shell/knownfolderid)

[<span data-ttu-id="1c199-141">KNOWN_FOLDER_FLAG</span><span class="sxs-lookup"><span data-stu-id="1c199-141">KNOWN_FOLDER_FLAG</span></span>](/windows/desktop/api/shlobj_core/ne-shlobj_core-known_folder_flag)

[<span data-ttu-id="1c199-142">SHGetFolderPath</span><span class="sxs-lookup"><span data-stu-id="1c199-142">SHGetFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha)

[<span data-ttu-id="1c199-143">SHGetKnownFolderIDList</span><span class="sxs-lookup"><span data-stu-id="1c199-143">SHGetKnownFolderIDList</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderidlist)

[<span data-ttu-id="1c199-144">SHGetKnownFolderPath</span><span class="sxs-lookup"><span data-stu-id="1c199-144">SHGetKnownFolderPath</span></span>](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath)
