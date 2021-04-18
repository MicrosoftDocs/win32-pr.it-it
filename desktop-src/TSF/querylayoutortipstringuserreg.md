---
title: QueryLayoutOrTipStringUserReg (funzione)
description: Esegue una query sulla stringa specificata che rappresenta il formato di un elenco di layout della tastiera o di un elenco di profili dei servizi di testo del percorso del registro di sistema specificato.
ms.assetid: b7b42fda-5a65-483a-b3f3-85157bb1a667
keywords:
- Framework servizi di testo funzione QueryLayoutOrTipStringUserReg
topic_type:
- apiref
api_name:
- QueryLayoutOrTipStringUserReg
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7f3e4979318b44e8c6be876af5301ad31e544d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302237"
---
# <a name="querylayoutortipstringuserreg-function"></a><span data-ttu-id="6e3c3-104">QueryLayoutOrTipStringUserReg (funzione)</span><span class="sxs-lookup"><span data-stu-id="6e3c3-104">QueryLayoutOrTipStringUserReg function</span></span>

<span data-ttu-id="6e3c3-105">Esegue una query sulla stringa specificata che rappresenta il formato di un elenco di layout della tastiera o di un elenco di profili dei servizi di testo del percorso del registro di sistema specificato.</span><span class="sxs-lookup"><span data-stu-id="6e3c3-105">Queries the specified string which represents the format of a keyboard layout list or text services profile list of the specified registry path.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e3c3-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e3c3-106">Syntax</span></span>


```C++
HRESULT CALLBACK QueryLayoutOrTipStringUserReg(
  _In_ LPCWSTR pszUserReg,
  _In_ LPCWSTR pszSystemReg,
  _In_ LPCWSTR pszSoftwareReg,
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="6e3c3-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="6e3c3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e3c3-108">*pszUserReg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e3c3-108">*pszUserReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e3c3-109">Percorso del registro di sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6e3c3-109">The registry path of the user.</span></span> <span data-ttu-id="6e3c3-110">Se questo parametro è **null**, \_ viene utilizzato l'utente corrente di HKEY \_ .</span><span class="sxs-lookup"><span data-stu-id="6e3c3-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="6e3c3-111">*pszSystemReg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e3c3-111">*pszSystemReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e3c3-112">Percorso del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="6e3c3-112">The registry path of the system.</span></span> <span data-ttu-id="6e3c3-113">Se questo parametro è **null**, \_ \_ viene usato il sistema del computer locale HKEY \\ .</span><span class="sxs-lookup"><span data-stu-id="6e3c3-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="6e3c3-114">*pszSoftwareReg* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e3c3-114">*pszSoftwareReg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e3c3-115">Percorso del registro di sistema del software.</span><span class="sxs-lookup"><span data-stu-id="6e3c3-115">The registry path of the software.</span></span> <span data-ttu-id="6e3c3-116">Se questo parametro è **null**, \_ \_ viene utilizzato il software locale del computer HKEY \\ .</span><span class="sxs-lookup"><span data-stu-id="6e3c3-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="6e3c3-117">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e3c3-117">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e3c3-118">Stringa che rappresenta un elenco di layout della tastiera o un elenco di profili di servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="6e3c3-118">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="6e3c3-119">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6e3c3-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e3c3-120">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="6e3c3-120">This must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e3c3-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6e3c3-121">Return value</span></span>

<span data-ttu-id="6e3c3-122">Questa funzione può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="6e3c3-122">This function can return one of these values.</span></span>



| <span data-ttu-id="6e3c3-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6e3c3-123">Return code</span></span>                                                                                  | <span data-ttu-id="6e3c3-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e3c3-124">Description</span></span>                                                                       |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6e3c3-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6e3c3-125"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="6e3c3-126">Tutti i layout o i profili definiti in **PSZ** sono validi.</span><span class="sxs-lookup"><span data-stu-id="6e3c3-126">All layouts or profiles defined in **psz** are valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="6e3c3-127"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6e3c3-127"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6e3c3-128">Uno o più layout o profili definiti in **PSZ** non sono validi.</span><span class="sxs-lookup"><span data-stu-id="6e3c3-128">One or more of the layouts or profiles defined in **psz** are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6e3c3-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e3c3-129">Remarks</span></span>

<span data-ttu-id="6e3c3-130">Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="6e3c3-130">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="6e3c3-131">L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta.</span><span class="sxs-lookup"><span data-stu-id="6e3c3-131">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="6e3c3-132">Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="6e3c3-132">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="6e3c3-133">Il formato della stringa dell'elenco di layout è:</span><span class="sxs-lookup"><span data-stu-id="6e3c3-133">The string format of the layout list is:</span></span>

<span data-ttu-id="6e3c3-134"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="6e3c3-134"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="6e3c3-135">Il formato stringa dell'elenco profilo servizio di testo è:</span><span class="sxs-lookup"><span data-stu-id="6e3c3-135">The string format of the text service profile list is:</span></span>

<span data-ttu-id="6e3c3-136"><LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="6e3c3-136"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="6e3c3-137">Di seguito è riportato un esempio di un valore per il parametro *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="6e3c3-137">The following is an example of a value for the *psz* parameter:</span></span>

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a><span data-ttu-id="6e3c3-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e3c3-138">Requirements</span></span>



| <span data-ttu-id="6e3c3-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e3c3-139">Requirement</span></span> | <span data-ttu-id="6e3c3-140">Valore</span><span class="sxs-lookup"><span data-stu-id="6e3c3-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6e3c3-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e3c3-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6e3c3-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6e3c3-142">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6e3c3-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e3c3-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6e3c3-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6e3c3-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6e3c3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="6e3c3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e3c3-146"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e3c3-146"><dt>Input.dll</dt></span></span> </dl> |



 

