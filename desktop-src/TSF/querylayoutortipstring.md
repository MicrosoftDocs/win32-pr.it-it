---
title: QueryLayoutOrTipString (funzione)
description: Esegue una query sulla stringa specificata che rappresenta il formato di un elenco di layout della tastiera o di un elenco di profili di servizi di testo.
ms.assetid: 92fd89b7-8b96-4709-8ee2-9814a908b4e4
keywords:
- Framework servizi di testo funzione QueryLayoutOrTipString
topic_type:
- apiref
api_name:
- QueryLayoutOrTipString
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11f4cead682a50897a74c60eeadf886e8b47456b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302238"
---
# <a name="querylayoutortipstring-function"></a><span data-ttu-id="0f88e-104">QueryLayoutOrTipString (funzione)</span><span class="sxs-lookup"><span data-stu-id="0f88e-104">QueryLayoutOrTipString function</span></span>

<span data-ttu-id="0f88e-105">Esegue una query sulla stringa specificata che rappresenta il formato di un elenco di layout della tastiera o di un elenco di profili di servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="0f88e-105">Queries the specified string which represents the format of a keyboard layout list or text services profile list.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f88e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f88e-106">Syntax</span></span>


```C++
HRESULT CALLBACK QueryLayoutOrTipString(
  _In_ LPCWSTR psz,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="0f88e-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f88e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f88e-108">*PSZ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f88e-108">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f88e-109">Stringa che rappresenta un elenco di layout della tastiera o un elenco di profili di servizi di testo.</span><span class="sxs-lookup"><span data-stu-id="0f88e-109">A string that represents a keyboard layout list or a text services profile list.</span></span>

</dd> <dt>

<span data-ttu-id="0f88e-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f88e-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f88e-111">Deve essere 0.</span><span class="sxs-lookup"><span data-stu-id="0f88e-111">This must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f88e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f88e-112">Return value</span></span>

<span data-ttu-id="0f88e-113">Questa funzione può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="0f88e-113">This function can return one of these values.</span></span>



| <span data-ttu-id="0f88e-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="0f88e-114">Return code</span></span>                                                                                  | <span data-ttu-id="0f88e-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f88e-115">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0f88e-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0f88e-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0f88e-117">Tutti i layout o i profili definiti in *PSZ* sono validi.</span><span class="sxs-lookup"><span data-stu-id="0f88e-117">All layouts or profiles defined in *psz* are valid.</span></span><br/>                  |
| <dl> <span data-ttu-id="0f88e-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0f88e-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0f88e-119">Uno o più layout o profili definiti in *PSZ* non sono validi.</span><span class="sxs-lookup"><span data-stu-id="0f88e-119">One or more of the layouts or profiles defined in *psz* are invalid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0f88e-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f88e-120">Remarks</span></span>

<span data-ttu-id="0f88e-121">Non è disponibile alcuna libreria di importazione che definisce questa funzione, quindi è necessario ottenere un puntatore a questa funzione utilizzando [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span><span class="sxs-lookup"><span data-stu-id="0f88e-121">There is no import library available that defines this function, so it is necessary to obtain a pointer to this function using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress).</span></span>

> [!Note]  
> <span data-ttu-id="0f88e-122">L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può compromettere la sicurezza dell'applicazione caricando la dll non corretta.</span><span class="sxs-lookup"><span data-stu-id="0f88e-122">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can compromise the security of your application by loading the wrong DLL.</span></span> <span data-ttu-id="0f88e-123">Per informazioni su come caricare correttamente le dll con diverse versioni di Microsoft Windows, vedere l' [ordine di ricerca della libreria a collegamento dinamico](/windows/desktop/Dlls/dynamic-link-library-search-order) .</span><span class="sxs-lookup"><span data-stu-id="0f88e-123">Refer to [Dynamic-Link Library Search Order](/windows/desktop/Dlls/dynamic-link-library-search-order) for information on how to correctly load DLLs with different versions of Microsoft Windows.</span></span>

 

<span data-ttu-id="0f88e-124">Il formato della stringa dell'elenco di layout è:</span><span class="sxs-lookup"><span data-stu-id="0f88e-124">The string format of the layout list is:</span></span>

<span data-ttu-id="0f88e-125"><LangID 1>: <KLID 1>; \[ ...<LangID N>:<KLID N></span><span class="sxs-lookup"><span data-stu-id="0f88e-125"><LangID 1>:<KLID 1>;\[...<LangID N>:<KLID N></span></span>

<span data-ttu-id="0f88e-126">Il formato stringa dell'elenco profilo servizio di testo è:</span><span class="sxs-lookup"><span data-stu-id="0f88e-126">The string format of the text service profile list is:</span></span>

<span data-ttu-id="0f88e-127"><LangID 1>: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx} {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span><span class="sxs-lookup"><span data-stu-id="0f88e-127"><LangID 1>:{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}{xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx};</span></span>

<span data-ttu-id="0f88e-128">Di seguito è riportato un esempio di un valore per il parametro *PSZ* :</span><span class="sxs-lookup"><span data-stu-id="0f88e-128">The following is an example of a value for the *psz* parameter:</span></span>

``` syntax
"0x0407:0x00000407"
"0x0407:0x00000407;0x040C:0x0000040C"
"0x0407:0x00000407;0x0412:{A028AE76-01B1-46C2-99C4-ACD9858AE02F}{B5FE1F02-D5F2-4445-9C03-C568F23C99A1};0x040C:0x0000040C"
```

## <a name="requirements"></a><span data-ttu-id="0f88e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f88e-129">Requirements</span></span>



| <span data-ttu-id="0f88e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f88e-130">Requirement</span></span> | <span data-ttu-id="0f88e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="0f88e-131">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0f88e-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f88e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="0f88e-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0f88e-133">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0f88e-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f88e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="0f88e-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0f88e-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0f88e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="0f88e-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f88e-137"><dt>Input.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f88e-137"><dt>Input.dll</dt></span></span> </dl> |



 

