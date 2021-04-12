---
title: SetDefaultLayoutOrTipUserReg (funzione)
description: Imposta il layout di tastiera o un servizio di testo specificato come elemento di input predefinito del registro di sistema dell'utente.
ms.assetid: 23ac67bb-b9dc-4f88-8fa0-a1d0534cbb84
keywords:
- Framework servizi di testo funzione SetDefaultLayoutOrTipUserReg
topic_type:
- apiref
api_name:
- SetDefaultLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48333b42b673cb6284e4b97001fa5ee88e0b3867
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119123"
---
# <a name="setdefaultlayoutortipuserreg-function"></a><span data-ttu-id="e0b0d-104">SetDefaultLayoutOrTipUserReg (funzione)</span><span class="sxs-lookup"><span data-stu-id="e0b0d-104">SetDefaultLayoutOrTipUserReg function</span></span>

<span data-ttu-id="e0b0d-105">Imposta il layout di tastiera o un servizio di testo specificato come elemento di input predefinito del registro di sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-105">Sets the specified keyboard layout or a text service as a default input item of the user registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0b0d-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0b0d-106">Syntax</span></span>


```C++
BOOL CALLBACK SetDefaultLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="e0b0d-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0b0d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0b0d-108">*pszUserReg* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e0b0d-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b0d-109">Percorso del registro di sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-109">The registry path of the user.</span></span> <span data-ttu-id="e0b0d-110">Se questo parametro è **null**, \_ viene utilizzato l'utente corrente di HKEY \_ .</span><span class="sxs-lookup"><span data-stu-id="e0b0d-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="e0b0d-111">*pszSystemReg* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e0b0d-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b0d-112">Percorso del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-112">The registry path of the system.</span></span> <span data-ttu-id="e0b0d-113">Se questo parametro è **null**, \_ \_ viene usato il sistema del computer locale HKEY \\ .</span><span class="sxs-lookup"><span data-stu-id="e0b0d-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="e0b0d-114">*pszSoftwareReg* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="e0b0d-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b0d-115">Percorso del registro di sistema del software.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-115">The registry path of the software.</span></span> <span data-ttu-id="e0b0d-116">Se questo parametro è **null**, \_ \_ viene utilizzato il software locale del computer HKEY \\ .</span><span class="sxs-lookup"><span data-stu-id="e0b0d-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="e0b0d-117">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0b0d-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b0d-118">Stringa che rappresenta l'elenco di layout della tastiera o del profilo dei servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="e0b0d-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e0b0d-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e0b0d-120">Oggetto bit che specifica i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="e0b0d-120">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="e0b0d-121">Gli identificatori seguenti non sono definiti in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="e0b0d-122">È necessario utilizzare il valore esadecimale o \# definire gli identificatori.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="e0b0d-123">Ad esempio, per usare SDLOT \_ NOAPPLYTOCURRENTSESSION, è necessario includere \# define SDLOT \_ NOAPPLYTOCURRENTSESSION 0x00000001 nel codice.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-123">For example, to use SDLOT\_NOAPPLYTOCURRENTSESSION you must include \#define SDLOT\_NOAPPLYTOCURRENTSESSION 0x00000001 in your code.</span></span>

 



| <span data-ttu-id="e0b0d-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e0b0d-124">Value</span></span>                                                                                                                                                                                                                                                                         | <span data-ttu-id="e0b0d-125">Significato</span><span class="sxs-lookup"><span data-stu-id="e0b0d-125">Meaning</span></span>                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SDLOT_NOAPPLYTOCURRENTSESSION"></span><span id="sdlot_noapplytocurrentsession"></span><dl> <span data-ttu-id="e0b0d-126"><dt>**SDLOT \_**</dt> <dt>0x00000001</dt> NOAPPLYTOCURRENTSESSION</span><span class="sxs-lookup"><span data-stu-id="e0b0d-126"><dt>**SDLOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="e0b0d-127">Archivia l'impostazione nel registro di sistema, ma la dose non aggiorna l'impostazione della tastiera di runtime della sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-127">Stores the setting in the registry but dose not update the runtime keyboard setting of the current session.</span></span> <span data-ttu-id="e0b0d-128">Se il percorso del registro di sistema alternativo è impostato in **SetDefaultLayoutOrTipUserReg**, questo flag deve essere impostato.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-128">If the alternative registry path is set in **SetDefaultLayoutOrTipUserReg**, this flag should be set.</span></span><br/> |
| <span id="SDLOT_APPLYTOCURRENTTHREAD"></span><span id="sdlot_applytocurrentthread"></span><dl> <span data-ttu-id="e0b0d-129"><dt>**SDLOT \_**</dt> <dt>0x00000002</dt> APPLYTOCURRENTTHREAD</span><span class="sxs-lookup"><span data-stu-id="e0b0d-129"><dt>**SDLOT\_APPLYTOCURRENTTHREAD**</dt> <dt>0x00000002</dt></span></span> </dl>          | <span data-ttu-id="e0b0d-130">Applica immediatamente l'impostazione nel thread corrente.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-130">Applies the setting immediately on the current thread.</span></span><br/>                                                                                                                                                            |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0b0d-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0b0d-131">Return value</span></span>



| <span data-ttu-id="e0b0d-132">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e0b0d-132">Return code</span></span>                                                                          | <span data-ttu-id="e0b0d-133">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e0b0d-133">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="e0b0d-134"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b0d-134"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="e0b0d-135">La funzione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-135">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="e0b0d-136"><dt>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="e0b0d-136"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="e0b0d-137">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-137">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e0b0d-138">Commenti</span><span class="sxs-lookup"><span data-stu-id="e0b0d-138">Remarks</span></span>

<span data-ttu-id="e0b0d-139">Il formato della stringa dell'elenco di layout è:</span><span class="sxs-lookup"><span data-stu-id="e0b0d-139">The string format of the layout list is:</span></span>

<span data-ttu-id="e0b0d-140"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="e0b0d-140"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="e0b0d-141">Il formato stringa dell'elenco profilo servizio di testo è:</span><span class="sxs-lookup"><span data-stu-id="e0b0d-141">The string format of the text service profile list is:</span></span>

<span data-ttu-id="e0b0d-142"><LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="e0b0d-142"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="e0b0d-143">Di seguito è riportato un esempio di un valore per il parametro *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="e0b0d-143">The following is an example of a value for the *psz* parameter:</span></span>


```
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="e0b0d-144">Esempio</span><span class="sxs-lookup"><span data-stu-id="e0b0d-144">Examples</span></span>

<span data-ttu-id="e0b0d-145">Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="e0b0d-145">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="e0b0d-146">Nell'esempio seguente viene illustrato come ottenere un puntatore a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-146">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="e0b0d-147">L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta.</span><span class="sxs-lookup"><span data-stu-id="e0b0d-147">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="e0b0d-148">Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="e0b0d-148">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
    WINAPI *PTF_ SETDEFAULTLAYOUTORTIPUSERREG)( LPCWSTR pszUserReg, 
    LPCWSTR pszSystemReg, 
    LPCWSTR pszSoftwareReg, 
    LPCWSTR psz);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    //Error loading module -- fail as securely as possible 
}
else
{
    PTF_ SETDEFAULTLAYOUTORTIPUSERREG pfnSetDefaultLayoutOrTipUserReg;
    
    pfnSetDefaultLayoutOrTipUserReg = (PTF_ SETDEFAULTLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "SetDefaultLayoutOrTipUserReg");

    if(pfnSetDefaultLayoutOrTipUserReg)
    {
        bRet = (*pfnSetDefaultLayoutOrTipUserReg)( pszUserReg, pszSystemReg, pszSoftwareReg, psz);
    }

    FreeLibrary(hInputDLL);
}
```



## <a name="requirements"></a><span data-ttu-id="e0b0d-149">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0b0d-149">Requirements</span></span>



| <span data-ttu-id="e0b0d-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0b0d-150">Requirement</span></span> | <span data-ttu-id="e0b0d-151">Valore</span><span class="sxs-lookup"><span data-stu-id="e0b0d-151">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e0b0d-152">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0b0d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="e0b0d-153">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e0b0d-153">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="e0b0d-154">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e0b0d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="e0b0d-155">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e0b0d-155">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e0b0d-156">DLL</span><span class="sxs-lookup"><span data-stu-id="e0b0d-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e0b0d-157"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0b0d-157"><dt>Input.dll</dt></span></span> </dl> |



 

