---
title: InstallLayoutOrTip (funzione)
description: Abilita i layout di tastiera o i servizi di testo specificati.
ms.assetid: 6542ad85-02fb-4a57-b665-ff367ba4e99c
keywords:
- Framework servizi di testo funzione InstallLayoutOrTip
topic_type:
- apiref
api_name:
- InstallLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fd3825903f4c92de93709385b03f9e9cba5db84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301688"
---
# <a name="installlayoutortip-function"></a><span data-ttu-id="4ad6f-104">InstallLayoutOrTip (funzione)</span><span class="sxs-lookup"><span data-stu-id="4ad6f-104">InstallLayoutOrTip function</span></span>

<span data-ttu-id="4ad6f-105">Abilita i layout di tastiera o i servizi di testo specificati.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-105">Enables the specified keyboard layouts or text services.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ad6f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ad6f-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTip(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="4ad6f-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="4ad6f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4ad6f-108">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ad6f-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ad6f-109">Stringa che rappresenta l'elenco di layout della tastiera o del profilo dei servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-109">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="4ad6f-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4ad6f-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4ad6f-111">Oggetto bit che specifica i flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="4ad6f-111">A bitfield that specifies the following flags:</span></span>

> [!Note]  
> <span data-ttu-id="4ad6f-112">Gli identificatori seguenti non sono definiti in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-112">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="4ad6f-113">È necessario utilizzare il valore esadecimale o \# definire gli identificatori.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-113">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="4ad6f-114">Ad esempio, per usare **la \_ disinstallazione di Ilot** , è necessario includere `#define ILOT_UNINSTALL 0x00000001` nel codice.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-114">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="4ad6f-115">Valore</span><span class="sxs-lookup"><span data-stu-id="4ad6f-115">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="4ad6f-116">Significato</span><span class="sxs-lookup"><span data-stu-id="4ad6f-116">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="4ad6f-117"><dt>**Ilot \_ Disinstalla**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="4ad6f-117"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="4ad6f-118">Uguale a **Ilot \_ disabilitato**.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-118">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="4ad6f-119"><dt>**Ilot \_**</dt> <dt>0x00000002</dt> DEFPROFILE</span><span class="sxs-lookup"><span data-stu-id="4ad6f-119"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="4ad6f-120">Imposta il layout o il suggerimento specificato come elemento predefinito.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-120">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_DEFUSER4"></span><span id="ilot_defuser4"></span><dl> <span data-ttu-id="4ad6f-121"><dt>**Ilot \_**</dt> <dt>0x00000004</dt> DEFUSER4</span><span class="sxs-lookup"><span data-stu-id="4ad6f-121"><dt>**ILOT\_DEFUSER4**</dt> <dt>0x00000004</dt></span></span> </dl>                                              | <span data-ttu-id="4ad6f-122">Modifica l'impostazione di. Predefinita.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-122">Changes the setting of .Default.</span></span><br/>                                |
| <span id="ILOT_SYSLOCALE"></span><span id="ilot_syslocale"></span><dl> <span data-ttu-id="4ad6f-123"><dt>**Ilot \_**</dt> <dt>0x00000008</dt> SYSLOCALE</span><span class="sxs-lookup"><span data-stu-id="4ad6f-123"><dt>**ILOT\_SYSLOCALE**</dt> <dt>0x00000008</dt></span></span> </dl>                                           | <span data-ttu-id="4ad6f-124">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-124">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOLOCALETOENUMERATE"></span><span id="ilot_nolocaletoenumerate"></span><dl> <span data-ttu-id="4ad6f-125"><dt>**Ilot \_**</dt> <dt>0x00000010</dt> NOLOCALETOENUMERATE</span><span class="sxs-lookup"><span data-stu-id="4ad6f-125"><dt>**ILOT\_NOLOCALETOENUMERATE**</dt> <dt>0x00000010</dt></span></span> </dl>             | <span data-ttu-id="4ad6f-126">Non utilizzato.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-126">Unused.</span></span><br/>                                                         |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="4ad6f-127"><dt>**Ilot \_**</dt> <dt>0x00000020</dt> NOAPPLYTOCURRENTSESSION</span><span class="sxs-lookup"><span data-stu-id="4ad6f-127"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="4ad6f-128">L'impostazione viene salvata ma non viene applicata alla sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-128">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="4ad6f-129"><dt>**Ilot \_**</dt> <dt>0x00000040</dt> CLEANINSTALL</span><span class="sxs-lookup"><span data-stu-id="4ad6f-129"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="4ad6f-130">Disabilita tutti i layout di tastiera e i servizi di testo correnti.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-130">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="4ad6f-131"><dt>**Ilot \_ 0x00000080 DISABILITAto**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="4ad6f-131"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="4ad6f-132">Disabilita il layout di tastiera e il servizio di testo specificati.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-132">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4ad6f-133">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4ad6f-133">Return value</span></span>



| <span data-ttu-id="4ad6f-134">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4ad6f-134">Return code</span></span>                                                                          | <span data-ttu-id="4ad6f-135">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ad6f-135">Description</span></span>                               |
|--------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="4ad6f-136"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="4ad6f-136"><dt>**TRUE**</dt></span></span> </dl>  | <span data-ttu-id="4ad6f-137">La funzione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-137">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="4ad6f-138"><dt>**FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="4ad6f-138"><dt>**FALSE**</dt></span></span> </dl> | <span data-ttu-id="4ad6f-139">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-139">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4ad6f-140">Commenti</span><span class="sxs-lookup"><span data-stu-id="4ad6f-140">Remarks</span></span>

<span data-ttu-id="4ad6f-141">Il formato della stringa dell'elenco di layout è:</span><span class="sxs-lookup"><span data-stu-id="4ad6f-141">The string format of the layout list is:</span></span>

<span data-ttu-id="4ad6f-142"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="4ad6f-142"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="4ad6f-143">Il formato stringa dell'elenco profilo servizio di testo è:</span><span class="sxs-lookup"><span data-stu-id="4ad6f-143">The string format of the text service profile list is:</span></span>

<span data-ttu-id="4ad6f-144"><LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="4ad6f-144"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="4ad6f-145">Di seguito è riportato un esempio di un valore per il parametro *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="4ad6f-145">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="4ad6f-146">Esempio</span><span class="sxs-lookup"><span data-stu-id="4ad6f-146">Examples</span></span>

<span data-ttu-id="4ad6f-147">Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="4ad6f-147">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="4ad6f-148">L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta.</span><span class="sxs-lookup"><span data-stu-id="4ad6f-148">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="4ad6f-149">Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="4ad6f-149">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (WINAPI *PTF_ INSTALLLAYOUTORTIP)(LPCWSTR psz, DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIP pfnInstallLayoutOrTip;
    
    pfnInstallLayoutOrTip = (PTF_ INSTALLLAYOUTORTIP)GetProcAddress(hInputDLL, "InstallLayoutOrTip");

    if(pfnInstallLayoutOrTip)
    {
        bRet = (*pfnInstallLayoutOrTip)(psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="4ad6f-150">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ad6f-150">Requirements</span></span>



| <span data-ttu-id="4ad6f-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ad6f-151">Requirement</span></span> | <span data-ttu-id="4ad6f-152">Valore</span><span class="sxs-lookup"><span data-stu-id="4ad6f-152">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="4ad6f-153">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ad6f-153">Minimum supported client</span></span><br/> | <span data-ttu-id="4ad6f-154">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4ad6f-154">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4ad6f-155">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ad6f-155">Minimum supported server</span></span><br/> | <span data-ttu-id="4ad6f-156">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4ad6f-156">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="4ad6f-157">DLL</span><span class="sxs-lookup"><span data-stu-id="4ad6f-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ad6f-158"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ad6f-158"><dt>Input.dll</dt></span></span> </dl> |



 

