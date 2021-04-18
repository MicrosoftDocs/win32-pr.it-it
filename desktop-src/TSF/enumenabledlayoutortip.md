---
title: EnumEnabledLayoutOrTip (funzione)
description: Enumera tutti i layout di tastiera abilitati o i servizi di testo dell'impostazione utente specificata.
ms.assetid: b3c57e88-e04b-411b-9eba-83258da16773
keywords:
- Framework servizi di testo funzione EnumEnabledLayoutOrTip
topic_type:
- apiref
api_name:
- EnumEnabledLayoutOrTip
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b192896dd95d5ab8f306158e33a8d248793bfc10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301570"
---
# <a name="enumenabledlayoutortip-function"></a><span data-ttu-id="76195-104">EnumEnabledLayoutOrTip (funzione)</span><span class="sxs-lookup"><span data-stu-id="76195-104">EnumEnabledLayoutOrTip function</span></span>

<span data-ttu-id="76195-105">Enumera tutti i layout di tastiera abilitati o i servizi di testo dell'impostazione utente specificata.</span><span class="sxs-lookup"><span data-stu-id="76195-105">Enumerates all enabled keyboard layouts or text services of the specified user setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="76195-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="76195-106">Syntax</span></span>


```C++
UINT EnumEnabledLayoutOrTip(
  _In_opt_ LPCWSTR            pszUserReg,
  _In_opt_ LPCWSTR            pszSystemReg,
  _In_opt_ LPCWSTR            pszSoftwareReg,
  _Out_    LAYOUTORTIPPROFILE *pLayoutOrTipProfile,
  _In_     UINT               uBufLength
);
```



## <a name="parameters"></a><span data-ttu-id="76195-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="76195-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76195-108">*pszUserReg* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="76195-108">*pszUserReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76195-109">Percorso del registro di sistema dell'utente.</span><span class="sxs-lookup"><span data-stu-id="76195-109">The registry path of the user.</span></span> <span data-ttu-id="76195-110">Se questo parametro è **null**, \_ viene utilizzato l'utente corrente di HKEY \_ .</span><span class="sxs-lookup"><span data-stu-id="76195-110">If this parameter is **NULL**, HKEY\_CURRENT\_USER is used.</span></span>

</dd> <dt>

<span data-ttu-id="76195-111">*pszSystemReg* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="76195-111">*pszSystemReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76195-112">Percorso del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="76195-112">The registry path of the system.</span></span> <span data-ttu-id="76195-113">Se questo parametro è **null**, \_ \_ viene usato il sistema del computer locale HKEY \\ .</span><span class="sxs-lookup"><span data-stu-id="76195-113">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\System is used.</span></span>

</dd> <dt>

<span data-ttu-id="76195-114">*pszSoftwareReg* \[ in, facoltativo\]</span><span class="sxs-lookup"><span data-stu-id="76195-114">*pszSoftwareReg* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="76195-115">Percorso del registro di sistema del software.</span><span class="sxs-lookup"><span data-stu-id="76195-115">The registry path of the software.</span></span> <span data-ttu-id="76195-116">Se questo parametro è **null**, \_ \_ viene utilizzato il software locale del computer HKEY \\ .</span><span class="sxs-lookup"><span data-stu-id="76195-116">If this parameter is **NULL**, HKEY\_LOCAL\_MACHINE\\Software is used.</span></span>

</dd> <dt>

<span data-ttu-id="76195-117">*pLayoutOrTipProfile* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="76195-117">*pLayoutOrTipProfile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76195-118">Puntatore al buffer che riceve la matrice LAYOUTORTIPPROFILE.</span><span class="sxs-lookup"><span data-stu-id="76195-118">Pointer to the buffer that receives the LAYOUTORTIPPROFILE array.</span></span>

</dd> <dt>

<span data-ttu-id="76195-119">*uBufLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="76195-119">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76195-120">Lunghezza del buffer a cui punta *pLayoutOrTipProfile*.</span><span class="sxs-lookup"><span data-stu-id="76195-120">The length of the buffer pointed to by *pLayoutOrTipProfile*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76195-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="76195-121">Return value</span></span>

<span data-ttu-id="76195-122">Se *pLayoutOrTipProfile* è **null**, il numero di elementi della tastiera abilitati nell'impostazione utente; in caso contrario, il numero di elementi della tastiera che vengono copiati in *pLayoutOrTipProfile*.</span><span class="sxs-lookup"><span data-stu-id="76195-122">If *pLayoutOrTipProfile* is **NULL**, the number of keyboard items that are enabled in the user setting; otherwise, the number of keyboard items that are copied into *pLayoutOrTipProfile*.</span></span>

<span data-ttu-id="76195-123">Per i linguaggi IME (Input Method Editor), vengono restituiti tutti gli IME, anche quando è abilitato un solo IME.</span><span class="sxs-lookup"><span data-stu-id="76195-123">For Input Method Editor (IME) languages, all IMEs are returned, even when only one IME is enabled.</span></span> <span data-ttu-id="76195-124">Se, ad esempio, per un utente è abilitato il nuovo IME rapido, la funzione **EnumEnabledLayoutOrTip** restituisce tutti i 5 IME cht.</span><span class="sxs-lookup"><span data-stu-id="76195-124">For example, if a user has the CHT New Quick IME enabled, the **EnumEnabledLayoutOrTip** function returns all 5 CHT IMEs.</span></span>

## <a name="remarks"></a><span data-ttu-id="76195-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="76195-125">Remarks</span></span>

<span data-ttu-id="76195-126">Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="76195-126">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="76195-127">L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta.</span><span class="sxs-lookup"><span data-stu-id="76195-127">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="76195-128">Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="76195-128">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="76195-129">La definizione di LAYOUTORTIPPROFILE è:</span><span class="sxs-lookup"><span data-stu-id="76195-129">The definition of LAYOUTORTIPPROFILE is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIPPROFILE {
    DWORD  dwProfileType;       // InputProcessor or HKL 
#define LOTP_INPUTPROCESSOR 1
#define LOTP_KEYBOARDLAYOUT 2
    LANGID langid;              // language id 
    CLSID  clsid;               // CLSID of tip 
    GUID   guidProfile;         // profile description 
    GUID   catid;               // category of tip 
    DWORD  dwSubstituteLayout;  // substitute hkl 
    DWORD  dwFlags;             // Flags 
    WCHAR  szId[MAX_PATH];      // KLID or TIP profile for string 
} LAYOUTORTIPPROFILE;
```

## <a name="requirements"></a><span data-ttu-id="76195-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="76195-130">Requirements</span></span>



| <span data-ttu-id="76195-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="76195-131">Requirement</span></span> | <span data-ttu-id="76195-132">Valore</span><span class="sxs-lookup"><span data-stu-id="76195-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76195-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76195-133">Minimum supported client</span></span><br/> | <span data-ttu-id="76195-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="76195-134">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="76195-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="76195-135">Minimum supported server</span></span><br/> | <span data-ttu-id="76195-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="76195-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="76195-137">DLL</span><span class="sxs-lookup"><span data-stu-id="76195-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="76195-138"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76195-138"><dt>Input.dll</dt></span></span> </dl> |



 

