---
description: Inserisce una parola e la relativa posizione nell'oggetto IWordSink.
ms.assetid: 3D645BF6-895E-46E2-92A3-3E301CD228D8
title: Metodo IWordSink::P utWord (search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 5f622e09c2b82bc8de986dafcc83247617caec75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306095"
---
# <a name="iwordsinkputword-method"></a><span data-ttu-id="4fd35-103">IWordSink::P metodo utWord</span><span class="sxs-lookup"><span data-stu-id="4fd35-103">IWordSink::PutWord method</span></span>

<span data-ttu-id="4fd35-104">Inserisce una parola e la relativa posizione nell'oggetto [**IWordSink**](iwordsink.md) .</span><span class="sxs-lookup"><span data-stu-id="4fd35-104">Puts a word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fd35-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4fd35-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="4fd35-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4fd35-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fd35-107">*CWC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fd35-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fd35-108">Numero di caratteri in *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="4fd35-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="4fd35-109">*pwcInBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fd35-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fd35-110">Puntatore a un buffer che contiene una forma alternativa di una parola dal testo di origine.</span><span class="sxs-lookup"><span data-stu-id="4fd35-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="4fd35-111">Questo parametro non viene modificato da **PutWord**.</span><span class="sxs-lookup"><span data-stu-id="4fd35-111">This parameter is not modified by **PutWord**.</span></span> <span data-ttu-id="4fd35-112">È possibile passare il parametro *pTextSource* da [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) , in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="4fd35-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="4fd35-113">*cwcSrcLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fd35-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fd35-114">Il numero di caratteri nel buffer di testo di origine (indicato dal parametro *pTextSource* in [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) che corrispondono alla parola contenuta in *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="4fd35-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="4fd35-115">*cwcSrcPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fd35-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fd35-116">Posizione iniziale della parola in *pwcInBuf* nel buffer del testo di origine (indicata dal parametro *pTextSource* per [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="4fd35-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fd35-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4fd35-117">Return value</span></span>

<span data-ttu-id="4fd35-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="4fd35-118">This method can return one of these values.</span></span>



| <span data-ttu-id="4fd35-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4fd35-119">Return code</span></span>                                                                                              | <span data-ttu-id="4fd35-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fd35-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="4fd35-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4fd35-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="4fd35-122">L'operazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="4fd35-122">The operation was completed successfully.</span></span> <span data-ttu-id="4fd35-123">Indica inoltre che non è disponibile altro testo per riempire il buffer.</span><span class="sxs-lookup"><span data-stu-id="4fd35-123">Also indicates that no more text is available to refill the buffer.</span></span><br/>                                  |
| <dl> <span data-ttu-id="4fd35-124"><dt>**Lingua \_ di \_ \_ parola grande**</dt></span><span class="sxs-lookup"><span data-stu-id="4fd35-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="4fd35-125">Il valore di *CWC* è maggiore del valore di *UlMaxTokenSize* specificato in [**IWordBreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span><span class="sxs-lookup"><span data-stu-id="4fd35-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="4fd35-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="4fd35-126">Remarks</span></span>

<span data-ttu-id="4fd35-127">È consigliabile che il metodo **IWordSink::P utword** contenga sempre la parola originale come disponibile in *pTextSource*.</span><span class="sxs-lookup"><span data-stu-id="4fd35-127">We recommend that the **IWordSink::PutWord** method always contain the original word as found in *pTextSource*.</span></span> <span data-ttu-id="4fd35-128">Le forme alternative della parola vengono passate a WordSink usando [**IWordSink::P utaltword**](iwordsink-putaltword.md).</span><span class="sxs-lookup"><span data-stu-id="4fd35-128">Alternative forms of the word are passed to WordSink by using [**IWordSink::PutAltWord**](iwordsink-putaltword.md).</span></span> <span data-ttu-id="4fd35-129">Si consiglia inoltre di fare in modo che le parole in *pwcInBuf* corrispondano quanto più possibile al testo di origine.</span><span class="sxs-lookup"><span data-stu-id="4fd35-129">We also recommend that the words in *pwcInBuf* match the source text as closely as possible.</span></span> <span data-ttu-id="4fd35-130">Ad esempio, se possibile, mantenere le lettere maiuscole e gli accenti.</span><span class="sxs-lookup"><span data-stu-id="4fd35-130">For example, retain capitalization and accents where possible.</span></span>

<span data-ttu-id="4fd35-131">Questa chiamata deve essere eseguita per ogni parola recuperata da *pTextSource* , ad eccezione di quelle per cui è stata effettuata la chiamata a [**IWordSink::P utaltword**](iwordsink-putaltword.md) .</span><span class="sxs-lookup"><span data-stu-id="4fd35-131">This call must be made for every word retrieved from *pTextSource* except those for which the [**IWordSink::PutAltWord**](iwordsink-putaltword.md) call was made.</span></span> <span data-ttu-id="4fd35-132">La parola viene terminata con un carattere EOW quando viene salvata in WordSink.</span><span class="sxs-lookup"><span data-stu-id="4fd35-132">The word is terminated with an EOW character when it is saved to the WordSink.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fd35-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4fd35-133">Requirements</span></span>



| <span data-ttu-id="4fd35-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fd35-134">Requirement</span></span> | <span data-ttu-id="4fd35-135">Valore</span><span class="sxs-lookup"><span data-stu-id="4fd35-135">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd35-136">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fd35-136">Minimum supported client</span></span><br/> | <span data-ttu-id="4fd35-137">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4fd35-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4fd35-138">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4fd35-138">Minimum supported server</span></span><br/> | <span data-ttu-id="4fd35-139">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4fd35-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4fd35-140">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4fd35-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fd35-141"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fd35-141"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fd35-142">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4fd35-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fd35-143">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="4fd35-143">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
