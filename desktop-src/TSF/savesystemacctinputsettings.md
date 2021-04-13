---
title: SaveSystemAcctInputSettings (funzione)
description: Applica il layout di tastiera utente e l'impostazione del servizio testo all'hive degli account di sistema.
ms.assetid: 73782637-3784-46d9-ba93-0527a2527412
keywords:
- Framework servizi di testo funzione SaveSystemAcctInputSettings
topic_type:
- apiref
api_name:
- SaveSystemAcctInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e45d590b80a9119d78eac8363a493ecd6c7b70d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400280"
---
# <a name="savesystemacctinputsettings-function"></a><span data-ttu-id="78f62-104">SaveSystemAcctInputSettings (funzione)</span><span class="sxs-lookup"><span data-stu-id="78f62-104">SaveSystemAcctInputSettings function</span></span>

<span data-ttu-id="78f62-105">Applica il layout di tastiera utente e l'impostazione del servizio testo all'hive degli account di sistema.</span><span class="sxs-lookup"><span data-stu-id="78f62-105">Applies the user keyboard layout and text service setting to the system accounts hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="78f62-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="78f62-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveSystemAcctInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="78f62-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="78f62-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78f62-108">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78f62-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78f62-109">Finestra padre per la finestra di dialogo di avviso.</span><span class="sxs-lookup"><span data-stu-id="78f62-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="78f62-110">La finestra di dialogo di avviso non è sempre visualizzata e viene visualizzata in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="78f62-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="78f62-111">Se questo parametro è **null**, la finestra di dialogo di avviso non verrà visualizzata.</span><span class="sxs-lookup"><span data-stu-id="78f62-111">If this parameter is **NULL**, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="78f62-112">*hSourceRegKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="78f62-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78f62-113">Chiave del registro di sistema radice dell'impostazione utente da copiare.</span><span class="sxs-lookup"><span data-stu-id="78f62-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78f62-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="78f62-114">Return value</span></span>



| <span data-ttu-id="78f62-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="78f62-115">Return code</span></span>                                                                          | <span data-ttu-id="78f62-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78f62-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="78f62-117"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="78f62-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="78f62-118">La funzione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="78f62-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="78f62-119"><dt>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="78f62-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="78f62-120">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="78f62-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="78f62-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="78f62-121">Remarks</span></span>

<span data-ttu-id="78f62-122">L'account di sistema hive è HKEY \_ Users \\ . DEFAULT, HKEY \_ Users \\ s-1-5-19 e HKEY \_ Users \\ s-1-5-20.</span><span class="sxs-lookup"><span data-stu-id="78f62-122">The system account hive is HKEY\_USERS\\.DEFAULT, HKEY\_USERS\\S-1-5-19, and HKEY\_USERS\\S-1-5-20.</span></span>

## <a name="examples"></a><span data-ttu-id="78f62-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="78f62-123">Examples</span></span>

<span data-ttu-id="78f62-124">Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="78f62-124">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="78f62-125">Nell'esempio seguente viene illustrato come ottenere un puntatore a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="78f62-125">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="78f62-126">L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta.</span><span class="sxs-lookup"><span data-stu-id="78f62-126">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="78f62-127">Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="78f62-127">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVESYSTEMACCTINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVESYSTEMACCTINPUTSETTINGS pfnSaveSystemAcctInputSettings;
    
    pfnSaveSystemAcctInputSettings = (PTF_ SAVESYSTEMACCTINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveSystemAcctInputSettings ");

    if(pfnSaveSystemAcctInputSettings)
    {
        bRet = (*pfnSaveSystemAcctInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="78f62-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="78f62-128">Requirements</span></span>



| <span data-ttu-id="78f62-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="78f62-129">Requirement</span></span> | <span data-ttu-id="78f62-130">Valore</span><span class="sxs-lookup"><span data-stu-id="78f62-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="78f62-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78f62-131">Minimum supported client</span></span><br/> | <span data-ttu-id="78f62-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="78f62-132">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="78f62-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="78f62-133">Minimum supported server</span></span><br/> | <span data-ttu-id="78f62-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="78f62-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="78f62-135">DLL</span><span class="sxs-lookup"><span data-stu-id="78f62-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78f62-136"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78f62-136"><dt>Input.dll</dt></span></span> </dl> |



 

