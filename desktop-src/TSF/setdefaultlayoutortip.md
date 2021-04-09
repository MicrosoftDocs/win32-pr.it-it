---
title: SetDefaultLayoutOrTip (funzione)
description: Imposta il layout di tastiera o un servizio di testo specificato come elemento di input predefinito dell'utente corrente.
ms.assetid: e602065c-776b-47ba-b050-4325197e03de
keywords:
- Framework servizi di testo funzione SetDefaultLayoutOrTip
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbdb2f2174c4a6d5ec37d5880d4a8b6feef236be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119299"
---
# <a name="setdefaultlayoutortip-function"></a><span data-ttu-id="0b38d-104">SetDefaultLayoutOrTip (funzione)</span><span class="sxs-lookup"><span data-stu-id="0b38d-104">SetDefaultLayoutOrTip function</span></span>

<span data-ttu-id="0b38d-105">Imposta il layout di tastiera o un servizio di testo specificato come elemento di input predefinito dell'utente corrente.</span><span class="sxs-lookup"><span data-stu-id="0b38d-105">Sets the specified keyboard layout or a text service as the default input item of the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b38d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0b38d-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTip(
  _In_ LPCWSTR           psz,
  _In_ LPCWSTR psz DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0b38d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0b38d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b38d-108">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b38d-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b38d-109">Stringa che rappresenta un elenco di layout della tastiera o un elenco di profili di servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="0b38d-109">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="0b38d-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0b38d-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0b38d-111">Oggetto bit che specifica i flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="0b38d-111">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="0b38d-112">Gli identificatori seguenti non sono definiti in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="0b38d-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="0b38d-113">È necessario utilizzare il valore esadecimale o \# definire gli identificatori.</span><span class="sxs-lookup"><span data-stu-id="0b38d-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="0b38d-114">Ad esempio, per usare SDLOT \_ NOAPPLYTOCURRENTSESSION, è necessario includere \# define SDLOT \_ NOAPPLYTOCURRENTSESSION 0x00000001 nel codice.</span><span class="sxs-lookup"><span data-stu-id="0b38d-114">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="0b38d-115">Valore</span><span class="sxs-lookup"><span data-stu-id="0b38d-115">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="0b38d-116">Significato</span><span class="sxs-lookup"><span data-stu-id="0b38d-116">Meaning</span></span>                                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="0b38d-117"><dt>**SDLOT \_**</dt> <dt>0x00000001</dt> NOAPPLYTOCURRENTSESSION</span><span class="sxs-lookup"><span data-stu-id="0b38d-117"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="0b38d-118">Archivia l'impostazione nel registro di sistema, ma la dose non aggiorna l'impostazione della tastiera di runtime della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="0b38d-118">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="0b38d-119">Se il percorso del registro di sistema alternativo è impostato in [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), questo flag deve essere impostato.</span><span class="sxs-lookup"><span data-stu-id="0b38d-119">If the alternative registry path is set in [**SetDefaultLayoutOrTipUserReg**](/windows/desktop/TSF/setdefaultlayoutortipuserreg), this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="0b38d-120"><dt>**SDLOT \_**</dt> <dt>0x00000002</dt> APPLYTOCURRENTTHREAD</span><span class="sxs-lookup"><span data-stu-id="0b38d-120"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="0b38d-121">Applica immediatamente l'impostazione nel thread corrente.</span><span class="sxs-lookup"><span data-stu-id="0b38d-121">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b38d-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0b38d-122">Return value</span></span>



| <span data-ttu-id="0b38d-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0b38d-123">Return code</span></span>                                                                          | <span data-ttu-id="0b38d-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b38d-124">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="0b38d-125"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="0b38d-125"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="0b38d-126">La funzione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="0b38d-126">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="0b38d-127"><dt>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="0b38d-127"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="0b38d-128">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="0b38d-128">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0b38d-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="0b38d-129">Remarks</span></span>

<span data-ttu-id="0b38d-130">Il formato della stringa dell'elenco di layout è:</span><span class="sxs-lookup"><span data-stu-id="0b38d-130">The string format of the layout list is:</span></span>

<span data-ttu-id="0b38d-131"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="0b38d-131"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="0b38d-132">Il formato stringa dell'elenco profilo servizio di testo è:</span><span class="sxs-lookup"><span data-stu-id="0b38d-132">The string format of the text service profile list is:</span></span>

<span data-ttu-id="0b38d-133"><LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="0b38d-133"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="0b38d-134">Di seguito è riportato un esempio di un valore per il parametro *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="0b38d-134">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="0b38d-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="0b38d-135">Examples</span></span>

<span data-ttu-id="0b38d-136">Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="0b38d-136">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="0b38d-137">Nell'esempio seguente viene illustrato come ottenere un puntatore a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="0b38d-137">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="0b38d-138">L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta.</span><span class="sxs-lookup"><span data-stu-id="0b38d-138">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="0b38d-139">Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="0b38d-139">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ SETDEFAULTLAYOUTORTIP)(LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIP pfnSetDefaultLayoutOrTip;
    
    pfnSetDefaultLayoutOrTip = (PTF_ SETDEFAULTLAYOUTORTIP)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTip");

    if(pfnSetDefaultLayoutOrTip)
    {
        bRet = (*pfnSetDefaultLayoutOrTip)(psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="0b38d-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0b38d-140">Requirements</span></span>



| <span data-ttu-id="0b38d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b38d-141">Requirement</span></span> | <span data-ttu-id="0b38d-142">Valore</span><span class="sxs-lookup"><span data-stu-id="0b38d-142">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0b38d-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b38d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="0b38d-144">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0b38d-144">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0b38d-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0b38d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="0b38d-146">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0b38d-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0b38d-147">DLL</span><span class="sxs-lookup"><span data-stu-id="0b38d-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b38d-148"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b38d-148"><dt>Input.dll</dt></span></span> </dl> |



 

