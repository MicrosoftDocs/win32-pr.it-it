---
title: EnumLayoutOrTipForSetup (funzione)
description: Enumera i layout di tastiera e i servizi di testo installati dell'interfaccia utente o della OOBE del programma di installazione.
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- Framework servizi di testo funzione EnumLayoutOrTipForSetup
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301346"
---
# <a name="enumlayoutortipforsetup-function"></a><span data-ttu-id="31a98-104">EnumLayoutOrTipForSetup (funzione)</span><span class="sxs-lookup"><span data-stu-id="31a98-104">EnumLayoutOrTipForSetup function</span></span>

<span data-ttu-id="31a98-105">Enumera i layout di tastiera e i servizi di testo installati dell'interfaccia utente o della OOBE del programma di installazione.</span><span class="sxs-lookup"><span data-stu-id="31a98-105">Enumerates the installed keyboard layouts and text services of the setup UI or OOBE.</span></span>

## <a name="syntax"></a><span data-ttu-id="31a98-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="31a98-106">Syntax</span></span>


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="31a98-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="31a98-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31a98-108">*LangID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31a98-108">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31a98-109">ID lingua dell'elemento da enumerare.</span><span class="sxs-lookup"><span data-stu-id="31a98-109">The language id of the item to be enumerated.</span></span>

</dd> <dt>

<span data-ttu-id="31a98-110">*pLayoutOrTip* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="31a98-110">*pLayoutOrTip* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31a98-111">Puntatore al buffer che riceve la matrice di strutture LAYOUTORTIP.</span><span class="sxs-lookup"><span data-stu-id="31a98-111">Pointer to the buffer that receives the array of LAYOUTORTIP structures.</span></span> <span data-ttu-id="31a98-112">Può essere **null** per ottenere il numero di elementi.</span><span class="sxs-lookup"><span data-stu-id="31a98-112">This can be **NULL** to get the number of items.</span></span>

</dd> <dt>

<span data-ttu-id="31a98-113">*uBufLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31a98-113">*uBufLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31a98-114">Lunghezza del buffer a cui punta *pLayoutOrTip*.</span><span class="sxs-lookup"><span data-stu-id="31a98-114">The length of the buffer pointed to by *pLayoutOrTip*.</span></span> <span data-ttu-id="31a98-115">Viene ignorato se *pLayoutOrTip* è **null**.</span><span class="sxs-lookup"><span data-stu-id="31a98-115">This is ignored if *pLayoutOrTip* is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="31a98-116">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="31a98-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31a98-117">Non usato.</span><span class="sxs-lookup"><span data-stu-id="31a98-117">Not used.</span></span> <span data-ttu-id="31a98-118">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="31a98-118">This must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31a98-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="31a98-119">Return value</span></span>

<span data-ttu-id="31a98-120">Se *pLayoutOrTip* è **null**, il numero di elementi della tastiera registrati nel sistema; in caso contrario, il numero di elementi della tastiera che vengono copiati in *pLayoutOrTip*.</span><span class="sxs-lookup"><span data-stu-id="31a98-120">If *pLayoutOrTip* is **NULL**, the number of keyboard items that are registered in System; otherwise, the number of keyboard items that are copied into *pLayoutOrTip*.</span></span>

## <a name="remarks"></a><span data-ttu-id="31a98-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="31a98-121">Remarks</span></span>

<span data-ttu-id="31a98-122">Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="31a98-122">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="31a98-123">L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta.</span><span class="sxs-lookup"><span data-stu-id="31a98-123">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="31a98-124">Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="31a98-124">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="31a98-125">La definizione di LAYOUTORTIP è:</span><span class="sxs-lookup"><span data-stu-id="31a98-125">The definition of LAYOUTORTIP is:</span></span>

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a><span data-ttu-id="31a98-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="31a98-126">Requirements</span></span>



| <span data-ttu-id="31a98-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="31a98-127">Requirement</span></span> | <span data-ttu-id="31a98-128">Valore</span><span class="sxs-lookup"><span data-stu-id="31a98-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="31a98-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31a98-129">Minimum supported client</span></span><br/> | <span data-ttu-id="31a98-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="31a98-130">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="31a98-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="31a98-131">Minimum supported server</span></span><br/> | <span data-ttu-id="31a98-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="31a98-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="31a98-133">DLL</span><span class="sxs-lookup"><span data-stu-id="31a98-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31a98-134"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31a98-134"><dt>Input.dll</dt></span></span> </dl> |



 

