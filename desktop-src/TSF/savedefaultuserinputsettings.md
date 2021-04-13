---
title: SaveDefaultUserInputSettings (funzione)
description: Applica il layout di tastiera utente e l'impostazione del servizio testo all'hive utente predefinito.
ms.assetid: ab3ec13f-fc5b-4c4d-ba11-679f97624651
keywords:
- Framework servizi di testo funzione SaveDefaultUserInputSettings
topic_type:
- apiref
api_name:
- SaveDefaultUserInputSettings
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66eb789a88f1a1a0c25fa26b95b3dda758f1ea1d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400412"
---
# <a name="savedefaultuserinputsettings-function"></a><span data-ttu-id="9bc88-104">SaveDefaultUserInputSettings (funzione)</span><span class="sxs-lookup"><span data-stu-id="9bc88-104">SaveDefaultUserInputSettings function</span></span>

<span data-ttu-id="9bc88-105">Applica il layout di tastiera utente e l'impostazione del servizio testo all'hive utente predefinito.</span><span class="sxs-lookup"><span data-stu-id="9bc88-105">Applies the user keyboard layout and text service setting to the default user hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bc88-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9bc88-106">Syntax</span></span>


```C++
BOOL CALLBACK SaveDefaultUserInputSettings(
  _In_ HWND hwndParent,
  _In_ HKEY hSourceRegKey
);
```



## <a name="parameters"></a><span data-ttu-id="9bc88-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="9bc88-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bc88-108">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9bc88-108">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bc88-109">Finestra padre per la finestra di dialogo di avviso.</span><span class="sxs-lookup"><span data-stu-id="9bc88-109">The parent window for the warning dialog box.</span></span> <span data-ttu-id="9bc88-110">La finestra di dialogo di avviso non è sempre visualizzata e viene visualizzata in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="9bc88-110">The warning dialog box is not always shown and appears appropriately.</span></span> <span data-ttu-id="9bc88-111">Se questo parametro è NULL, la finestra di dialogo di avviso non verrà visualizzata.</span><span class="sxs-lookup"><span data-stu-id="9bc88-111">If this parameter is NULL, the warning dialog box will not be shown.</span></span>

</dd> <dt>

<span data-ttu-id="9bc88-112">*hSourceRegKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9bc88-112">*hSourceRegKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9bc88-113">Chiave del registro di sistema radice dell'impostazione utente da copiare.</span><span class="sxs-lookup"><span data-stu-id="9bc88-113">The root registry key of the user setting to be copied.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bc88-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9bc88-114">Return value</span></span>



| <span data-ttu-id="9bc88-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="9bc88-115">Return code</span></span>                                                                          | <span data-ttu-id="9bc88-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9bc88-116">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="9bc88-117"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="9bc88-117"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="9bc88-118">La funzione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="9bc88-118">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="9bc88-119"><dt>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="9bc88-119"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="9bc88-120">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="9bc88-120">An unspecified error occurred.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="9bc88-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="9bc88-121">Examples</span></span>

<span data-ttu-id="9bc88-122">Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="9bc88-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="9bc88-123">Nell'esempio seguente viene illustrato come ottenere un puntatore a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="9bc88-123">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="9bc88-124">L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta.</span><span class="sxs-lookup"><span data-stu-id="9bc88-124">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="9bc88-125">Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="9bc88-125">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SAVEDEFAULTUSERINPUTSETTINGS)(HWND hwndParent, HKEY hSourceRegKey);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SAVEDEFAULTUSERINPUTSETTINGS pfnSaveDefaultUserInputSettings;
    
    pfnSaveDefaultUserInputSettings = (PTF_ SAVEDEFAULTUSERINPUTSETTINGS)GetProcAddress(hInputDLL, "SaveDefaultUserInputSettings ");

    if(pfnSaveDefaultUserInputSettings)
    {
        bRet = (*pfnSaveDefaultUserInputSettings)( hwndParent, hSourceRegKey);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="9bc88-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9bc88-126">Requirements</span></span>



| <span data-ttu-id="9bc88-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9bc88-127">Requirement</span></span> | <span data-ttu-id="9bc88-128">Valore</span><span class="sxs-lookup"><span data-stu-id="9bc88-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9bc88-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bc88-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9bc88-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9bc88-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9bc88-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9bc88-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9bc88-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9bc88-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9bc88-133">DLL</span><span class="sxs-lookup"><span data-stu-id="9bc88-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bc88-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bc88-134"><dt>Input.dll</dt></span></span> </dl> |



 

