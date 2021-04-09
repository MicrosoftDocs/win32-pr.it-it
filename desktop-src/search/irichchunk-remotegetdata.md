---
description: Recupera la stringa di input e PROPVARIANT che rappresenta un blocco di dati. La chiamata a questo metodo equivale alla chiamata a GetData.
ms.assetid: 78846D1D-923F-4FEA-8BF2-B16BB1B21BB3
title: 'Metodo IRichChunk:: RemoteGetData'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRichChunk.RemoteGetData
api_type:
- COM
api_location: ''
ms.openlocfilehash: 002c85b189a3994b70795c05228ae5331c610284
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128506"
---
# <a name="irichchunkremotegetdata-method"></a><span data-ttu-id="23da8-104">Metodo IRichChunk:: RemoteGetData</span><span class="sxs-lookup"><span data-stu-id="23da8-104">IRichChunk::RemoteGetData method</span></span>

<span data-ttu-id="23da8-105">Recupera la stringa di input e [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) che rappresenta un blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="23da8-105">Retrieves the [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) and input string that represents a chunk of data.</span></span> <span data-ttu-id="23da8-106">La chiamata a questo metodo equivale alla chiamata a [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).</span><span class="sxs-lookup"><span data-stu-id="23da8-106">Calling this method is the same as calling [**GetData**](/windows/desktop/api/StructuredQueryCondition/nf-structuredquerycondition-irichchunk-getdata).</span></span>

## <a name="syntax"></a><span data-ttu-id="23da8-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="23da8-107">Syntax</span></span>


```C++
HRESULT RemoteGetData(
  [out] ULONG       *pFirstPos,
  [out] ULONG       *pLength,
  [out] LPWSTR      *ppsz,
  [out] PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="23da8-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="23da8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23da8-109">*pFirstPos* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23da8-109">*pFirstPos* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23da8-110">Riceve la posizione iniziale in base zero dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="23da8-110">Receives the zero-based starting position of the range.</span></span> <span data-ttu-id="23da8-111">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="23da8-111">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="23da8-112">*pLength* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23da8-112">*pLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23da8-113">Riceve la lunghezza dell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="23da8-113">Receives the length of the range.</span></span> <span data-ttu-id="23da8-114">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="23da8-114">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="23da8-115">*ppsz* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23da8-115">*ppsz* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23da8-116">Riceve il valore stringa Unicode associato oppure **null** se non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="23da8-116">Receives the associated Unicode string value, or **NULL** if not available.</span></span>

</dd> <dt>

<span data-ttu-id="23da8-117">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23da8-117">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23da8-118">Riceve il valore [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) associato oppure **VT \_ vuoto** se non è disponibile.</span><span class="sxs-lookup"><span data-stu-id="23da8-118">Receives the associated [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) value, or **VT\_EMPTY** if not available.</span></span> <span data-ttu-id="23da8-119">Questo parametro può essere **NULL**.</span><span class="sxs-lookup"><span data-stu-id="23da8-119">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23da8-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="23da8-120">Return value</span></span>

<span data-ttu-id="23da8-121">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="23da8-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="23da8-122">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="23da8-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="see-also"></a><span data-ttu-id="23da8-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="23da8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23da8-124">**IRichChunk**</span><span class="sxs-lookup"><span data-stu-id="23da8-124">**IRichChunk**</span></span>](/windows/desktop/api/Structuredquerycondition/nn-structuredquerycondition-irichchunk)
</dt> </dl>

 

 
