---
UID: ''
title: UnicodeToBytes (funzione)
description: Converte i caratteri Unicode in GB18030 byte.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: WideCharToMultiByte, MultiByteToWideChar
ms.topic: reference
req.header: Gb18030.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: c_g18030.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- c_g18030.dll
api_name:
- UnicodeToBytes
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 66ed21768c3acef7f2aa2128df057da8552b2ad2
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2020
ms.locfileid: "103719951"
---
# <a name="unicodetobytes-function"></a><span data-ttu-id="c090f-103">UnicodeToBytes (funzione)</span><span class="sxs-lookup"><span data-stu-id="c090f-103">UnicodeToBytes function</span></span>

## <a name="description"></a><span data-ttu-id="c090f-104">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c090f-104">Description</span></span>

<span data-ttu-id="c090f-105">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="c090f-105">Deprecated.</span></span> <span data-ttu-id="c090f-106">Converte i caratteri Unicode in GB18030 byte.</span><span class="sxs-lookup"><span data-stu-id="c090f-106">Converts Unicode characters to GB18030 bytes.</span></span>

<span data-ttu-id="c090f-107">**Nota**  Quando si convertono i caratteri Unicode in GB18030 byte, un'applicazione da eseguire in Windows Vista e versioni successive deve usare la funzione [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) .</span><span class="sxs-lookup"><span data-stu-id="c090f-107">**Note**  When converting Unicode characters to GB18030 bytes, an application to run on Windows Vista and later should use the [WideCharToMultiByte](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte) function.</span></span>

```cpp
DWORD UnicodeToBytes(
  _In_ LPWSTR lpWideCharStr,
  _In_ UINT   cchWideChar,
  _In_ LPSTR  lpMultiByteStr,
  _In_ UINT   cchMultiByte
);
```

## <a name="parameters"></a><span data-ttu-id="c090f-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c090f-108">Parameters</span></span>

### <a name="lpwidecharstr-in"></a><span data-ttu-id="c090f-109">lpWideCharStr [in]</span><span class="sxs-lookup"><span data-stu-id="c090f-109">lpWideCharStr [in]</span></span>

<span data-ttu-id="c090f-110">Puntatore alla stringa Unicode da convertire.</span><span class="sxs-lookup"><span data-stu-id="c090f-110">Pointer to the Unicode string to convert.</span></span>

### <a name="cchwidechar-in"></a><span data-ttu-id="c090f-111">cchWideChar [in]</span><span class="sxs-lookup"><span data-stu-id="c090f-111">cchWideChar [in]</span></span>

<span data-ttu-id="c090f-112">Numero di caratteri della stringa Unicode da convertire.</span><span class="sxs-lookup"><span data-stu-id="c090f-112">Character count of the Unicode string to convert.</span></span>

### <a name="lpmultibytestr-in"></a><span data-ttu-id="c090f-113">lpMultiByteStr [in]</span><span class="sxs-lookup"><span data-stu-id="c090f-113">lpMultiByteStr [in]</span></span>

<span data-ttu-id="c090f-114">Puntatore al buffer multibyte di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c090f-114">Pointer to the target multibyte buffer.</span></span>
<span data-ttu-id="c090f-115">Se *lpMultiByteStr* è 0, viene restituito il numero di byte del risultato GB18030 e non viene eseguita alcuna conversione.</span><span class="sxs-lookup"><span data-stu-id="c090f-115">If *lpMultiByteStr* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

### <a name="cchmultibyte-in"></a><span data-ttu-id="c090f-116">cchMultiByte [in]</span><span class="sxs-lookup"><span data-stu-id="c090f-116">cchMultiByte [in]</span></span>

<span data-ttu-id="c090f-117">Numero di byte del buffer multibyte di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c090f-117">Byte count of the target multibyte buffer.</span></span>
<span data-ttu-id="c090f-118">Se *cchMultiByte* è 0, viene restituito il numero di byte del risultato GB18030 e non viene eseguita alcuna conversione.</span><span class="sxs-lookup"><span data-stu-id="c090f-118">If *cchMultiByte* is 0, the byte count of the GB18030 result is returned, and no conversion is done.</span></span>

## <a name="returns"></a><span data-ttu-id="c090f-119">Restituisce</span><span class="sxs-lookup"><span data-stu-id="c090f-119">Returns</span></span>

<span data-ttu-id="c090f-120">Restituisce il numero di byte dei caratteri multibyte generati, in caso di esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c090f-120">Returns the byte count of the multibyte characters that are generated, if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c090f-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="c090f-121">Remarks</span></span>

## <a name="see-also"></a><span data-ttu-id="c090f-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c090f-122">See also</span></span>

[<span data-ttu-id="c090f-123">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="c090f-123">WideCharToMultiByte</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)

[<span data-ttu-id="c090f-124">MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="c090f-124">MultiByteToWideChar</span></span>](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
