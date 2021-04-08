---
title: InstallLayoutOrTipUserReg (funzione)
description: Abilita i layout di tastiera o i servizi di testo specificati per l'utente specificato.
ms.assetid: f9b7a77e-5e82-41a6-8deb-be13bb96e85f
keywords:
- Framework servizi di testo funzione InstallLayoutOrTipUserReg
topic_type:
- apiref
api_name:
- InstallLayoutOrTipUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0484aeb16990467edd6e9f56a8a0cb6ca27b9ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741626"
---
# <a name="installlayoutortipuserreg-function"></a><span data-ttu-id="462e4-104">InstallLayoutOrTipUserReg (funzione)</span><span class="sxs-lookup"><span data-stu-id="462e4-104">InstallLayoutOrTipUserReg function</span></span>

<span data-ttu-id="462e4-105">Abilita i layout di tastiera o i servizi di testo specificati per l'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="462e4-105">Enables the specified keyboard layouts or text services for the specified user.</span></span>

## <a name="syntax"></a><span data-ttu-id="462e4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="462e4-106">Syntax</span></span>


```C++
BOOL CALLBACK InstallLayoutOrTipUserReg(
  _In_opt_ LPCWSTR pszUserReg,
  _In_opt_ LPCWSTR pszSystemReg,
  _In_opt_ LPCWSTR pszSoftwareReg,
  _In_     LPCWSTR psz,
  _In_     DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="462e4-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="462e4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="462e4-108">*pszUserReg* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="462e4-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="462e4-109">Percorso del registro di sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="462e4-109">The registry path of the user.</span></span> <span data-ttu-id="462e4-110">Se questo parametro è **null**, \_ viene utilizzato l'utente corrente di HKEY \_ .</span><span class="sxs-lookup"><span data-stu-id="462e4-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="462e4-111">*pszSystemReg* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="462e4-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="462e4-112">Percorso del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="462e4-112">The registry path of the system.</span></span> <span data-ttu-id="462e4-113">Se questo parametro è **null**, \_ \_ viene usato il sistema del computer locale HKEY \\ .</span><span class="sxs-lookup"><span data-stu-id="462e4-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="462e4-114">*pszSoftwareReg* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="462e4-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="462e4-115">Percorso del registro di sistema del software.</span><span class="sxs-lookup"><span data-stu-id="462e4-115">The registry path of the software.</span></span> <span data-ttu-id="462e4-116">Se questo parametro è **null**, \_ \_ viene utilizzato il software locale del computer HKEY \\ .</span><span class="sxs-lookup"><span data-stu-id="462e4-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="462e4-117">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="462e4-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="462e4-118">Stringa che rappresenta l'elenco di layout della tastiera o del profilo dei servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="462e4-118">A string that represents the keyboard layout list or text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="462e4-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="462e4-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="462e4-120">Oggetto bit che specifica i flag seguenti.</span><span class="sxs-lookup"><span data-stu-id="462e4-120">A bitfield that specifies the following flags.</span></span>

> [!Note]  
> <span data-ttu-id="462e4-121">Gli identificatori seguenti non sono definiti in un file di intestazione pubblico.</span><span class="sxs-lookup"><span data-stu-id="462e4-121">The following identifiers are not defined in a public header file.</span></span> <span data-ttu-id="462e4-122">È necessario utilizzare il valore esadecimale o \# definire gli identificatori.</span><span class="sxs-lookup"><span data-stu-id="462e4-122">You must either use the hexadecimal value or \#define the identifiers.</span></span> <span data-ttu-id="462e4-123">Ad esempio, per usare **la \_ disinstallazione di Ilot** , è necessario includere `#define ILOT_UNINSTALL 0x00000001` nel codice.</span><span class="sxs-lookup"><span data-stu-id="462e4-123">For example, to use **ILOT\_UNINSTALL** you must include `#define ILOT_UNINSTALL 0x00000001` in your code.</span></span>

 



| <span data-ttu-id="462e4-124">Valore</span><span class="sxs-lookup"><span data-stu-id="462e4-124">Value</span></span>                                                                                                                                                                                                                                                                      | <span data-ttu-id="462e4-125">Significato</span><span class="sxs-lookup"><span data-stu-id="462e4-125">Meaning</span></span>                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="ILOT_UNINSTALL"></span><span id="ilot_uninstall"></span><dl> <span data-ttu-id="462e4-126"><dt>**Ilot \_ Disinstalla**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="462e4-126"><dt>**ILOT\_UNINSTALL**</dt> <dt>0x00000001</dt></span></span> </dl>                                           | <span data-ttu-id="462e4-127">Uguale a **Ilot \_ disabilitato**.</span><span class="sxs-lookup"><span data-stu-id="462e4-127">Same as **ILOT\_DISABLED**.</span></span><br/>                                     |
| <span id="ILOT_DEFPROFILE"></span><span id="ilot_defprofile"></span><dl> <span data-ttu-id="462e4-128"><dt>**Ilot \_**</dt> <dt>0x00000002</dt> DEFPROFILE</span><span class="sxs-lookup"><span data-stu-id="462e4-128"><dt>**ILOT\_DEFPROFILE**</dt> <dt>0x00000002</dt></span></span> </dl>                                        | <span data-ttu-id="462e4-129">Imposta il layout o il suggerimento specificato come elemento predefinito.</span><span class="sxs-lookup"><span data-stu-id="462e4-129">Sets the specified layout or tip as a default item.</span></span><br/>             |
| <span id="ILOT_NOAPPLYTOCURRENTSESSION"></span><span id="ilot_noapplytocurrentsession"></span><dl> <span data-ttu-id="462e4-130"><dt>**Ilot \_**</dt> <dt>0x00000020</dt> NOAPPLYTOCURRENTSESSION</span><span class="sxs-lookup"><span data-stu-id="462e4-130"><dt>**ILOT\_NOAPPLYTOCURRENTSESSION**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="462e4-131">L'impostazione viene salvata ma non viene applicata alla sessione corrente.</span><span class="sxs-lookup"><span data-stu-id="462e4-131">The setting is saved but is not applied to the current session.</span></span><br/> |
| <span id="ILOT_CLEANINSTALL"></span><span id="ilot_cleaninstall"></span><dl> <span data-ttu-id="462e4-132"><dt>**Ilot \_**</dt> <dt>0x00000040</dt> CLEANINSTALL</span><span class="sxs-lookup"><span data-stu-id="462e4-132"><dt>**ILOT\_CLEANINSTALL**</dt> <dt>0x00000040</dt></span></span> </dl>                                  | <span data-ttu-id="462e4-133">Disabilita tutti i layout di tastiera e i servizi di testo correnti.</span><span class="sxs-lookup"><span data-stu-id="462e4-133">Disables all of the current keyboard layouts and text services.</span></span><br/> |
| <span id="ILOT_DISABLED"></span><span id="ilot_disabled"></span><dl> <span data-ttu-id="462e4-134"><dt>**Ilot \_ 0x00000080 DISABILITAto**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="462e4-134"><dt>**ILOT\_DISABLED**</dt> <dt>0x00000080</dt></span></span> </dl>                                              | <span data-ttu-id="462e4-135">Disabilita il layout di tastiera e il servizio di testo specificati.</span><span class="sxs-lookup"><span data-stu-id="462e4-135">Disables the specified keyboard layout and text service.</span></span><br/>        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="462e4-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="462e4-136">Return value</span></span>



| <span data-ttu-id="462e4-137">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="462e4-137">Return code</span></span>                                                                         | <span data-ttu-id="462e4-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="462e4-138">Description</span></span>                               |
|-------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="462e4-139"><dt>**TRUE**</dt></span><span class="sxs-lookup"><span data-stu-id="462e4-139"><dt>**TRUE**</dt></span></span> </dl> | <span data-ttu-id="462e4-140">La funzione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="462e4-140">The function was successful.</span></span><br/>   |
| <dl> <span data-ttu-id="462e4-141"><dt>**FASE**</dt></span><span class="sxs-lookup"><span data-stu-id="462e4-141"><dt>**FASE**</dt></span></span> </dl> | <span data-ttu-id="462e4-142">Si è verificato un errore non specificato.</span><span class="sxs-lookup"><span data-stu-id="462e4-142">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="462e4-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="462e4-143">Remarks</span></span>

<span data-ttu-id="462e4-144">Il formato della stringa dell'elenco di layout è:</span><span class="sxs-lookup"><span data-stu-id="462e4-144">The string format of the layout list is:</span></span>

<span data-ttu-id="462e4-145"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="462e4-145"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="462e4-146">Il formato stringa dell'elenco profilo servizio di testo è:</span><span class="sxs-lookup"><span data-stu-id="462e4-146">The string format of the text service profile list is:</span></span>

<span data-ttu-id="462e4-147"><LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="462e4-147"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="462e4-148">Di seguito è riportato un esempio di un valore per il parametro *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="462e4-148">The following is an example of a value for the *psz* parameter:</span></span>


```C++
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```



## <a name="examples"></a><span data-ttu-id="462e4-149">Esempio</span><span class="sxs-lookup"><span data-stu-id="462e4-149">Examples</span></span>

<span data-ttu-id="462e4-150">Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="462e4-150">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span> <span data-ttu-id="462e4-151">Nell'esempio seguente viene illustrato come ottenere un puntatore a questa funzione.</span><span class="sxs-lookup"><span data-stu-id="462e4-151">The following example demonstrates how to obtain a pointer to this function.</span></span>

> [!Note]  
> <span data-ttu-id="462e4-152">L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta.</span><span class="sxs-lookup"><span data-stu-id="462e4-152">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="462e4-153">Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="462e4-153">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 


```C++
typedef HRESULT (
  WINAPI *PTF_ INSTALLLAYOUTORTIPUSERREG)(LPCWSTR pszUserReg, 
  LPCWSTR pszSystemReg, 
  LPCWSTR pszSoftwareReg, 
  LPCWSTR psz, 
  DWORD dwFlasg);

HMODULE hInputDLL = LoadLibrary(TEXT("input.dll"));
BOOL bRet = FALSE;

if(hInputDLL == NULL)
{
    // Error loading module; fail as securely as possible. 
}
else
{
    PTF_ INSTALLLAYOUTORTIPUSERREG pfnInputLayoutOrTipUserReg;
    
    pfnInputLayoutOrTipUserReg = (PTF_ INSTALLLAYOUTORTIPUSERREG)GetProcAddress(hInputDLL, "InputLayoutOrTipUserReg");

    if(pfnInputLayoutOrTipUserReg)
    {
        bRet = (*pfnInputLayoutOrTipUserReg)(pszUserReg, pszSystemReg, pszSoftwareReg, psz, dwFlags);
    }

    FreeLibrary(hInputDLL);
}

```



## <a name="requirements"></a><span data-ttu-id="462e4-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="462e4-154">Requirements</span></span>



| <span data-ttu-id="462e4-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="462e4-155">Requirement</span></span> | <span data-ttu-id="462e4-156">Valore</span><span class="sxs-lookup"><span data-stu-id="462e4-156">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="462e4-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="462e4-157">Minimum supported client</span></span><br/> | <span data-ttu-id="462e4-158">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="462e4-158">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="462e4-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="462e4-159">Minimum supported server</span></span><br/> | <span data-ttu-id="462e4-160">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="462e4-160">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="462e4-161">DLL</span><span class="sxs-lookup"><span data-stu-id="462e4-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="462e4-162"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="462e4-162"><dt>Input.dll</dt></span></span> </dl> |



 

