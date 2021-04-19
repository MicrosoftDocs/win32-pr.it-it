---
description: Inserisce una parola alternativa e la relativa posizione nell'oggetto IWordSink.
ms.assetid: 5C8A9B30-F9B5-42E9-ADAC-A11230F0C2FA
title: Metodo IWordSink::P utAltWord (search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 21fd9eb9ac5a1bf0f52d6574595dc495432d7ec9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306096"
---
# <a name="iwordsinkputaltword-method"></a><span data-ttu-id="2f53d-103">IWordSink::P metodo utAltWord</span><span class="sxs-lookup"><span data-stu-id="2f53d-103">IWordSink::PutAltWord method</span></span>

<span data-ttu-id="2f53d-104">Inserisce una parola alternativa e la relativa posizione nell'oggetto [**IWordSink**](iwordsink.md) .</span><span class="sxs-lookup"><span data-stu-id="2f53d-104">Puts an alternative word and its position in the [**IWordSink**](iwordsink.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f53d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f53d-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in]       ULONG cwc,
  [in] const WCHAR *pwcInBuf,
  [in]       ULONG cwcSrcLen,
  [in]       ULONG cwcSrcPos
);
```



## <a name="parameters"></a><span data-ttu-id="2f53d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f53d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f53d-107">*CWC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f53d-107">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f53d-108">Numero di caratteri in *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="2f53d-108">The number of characters in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="2f53d-109">*pwcInBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f53d-109">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f53d-110">Puntatore a un buffer che contiene una forma alternativa di una parola dal testo di origine.</span><span class="sxs-lookup"><span data-stu-id="2f53d-110">A pointer to a buffer that contains an alternative form of a word from the source text.</span></span> <span data-ttu-id="2f53d-111">Questo parametro non viene modificato da **PutAltWord**.</span><span class="sxs-lookup"><span data-stu-id="2f53d-111">This parameter is not modified by **PutAltWord**.</span></span> <span data-ttu-id="2f53d-112">È possibile passare il parametro *pTextSource* da [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) , in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="2f53d-112">You can pass the *pTextSource* parameter from [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext) as appropriate.</span></span>

</dd> <dt>

<span data-ttu-id="2f53d-113">*cwcSrcLen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f53d-113">*cwcSrcLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f53d-114">Il numero di caratteri nel buffer di testo di origine (indicato dal parametro *pTextSource* in [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) che corrispondono alla parola contenuta in *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="2f53d-114">The number of characters in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)) that correspond to the word contained in *pwcInBuf*.</span></span>

</dd> <dt>

<span data-ttu-id="2f53d-115">*cwcSrcPos* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f53d-115">*cwcSrcPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f53d-116">Posizione iniziale della parola in *pwcInBuf* nel buffer del testo di origine (indicata dal parametro *pTextSource* per [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="2f53d-116">The starting position of the word in *pwcInBuf* in the source text buffer (indicated by the *pTextSource* parameter to [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f53d-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f53d-117">Return value</span></span>

<span data-ttu-id="2f53d-118">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="2f53d-118">This method can return one of these values.</span></span>



| <span data-ttu-id="2f53d-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="2f53d-119">Return code</span></span>                                                                                              | <span data-ttu-id="2f53d-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2f53d-120">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2f53d-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2f53d-121"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="2f53d-122">L'operazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="2f53d-122">The operation was completed successfully.</span></span> <span data-ttu-id="2f53d-123">Indica inoltre che non resta altro testo da elaborare.</span><span class="sxs-lookup"><span data-stu-id="2f53d-123">Also indicates that no more text remains to be processed.</span></span><br/>                                            |
| <dl> <span data-ttu-id="2f53d-124"><dt>**Lingua \_ di \_ \_ parola grande**</dt></span><span class="sxs-lookup"><span data-stu-id="2f53d-124"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="2f53d-125">Il valore di *CWC* è maggiore del valore di *UlMaxTokenSize* specificato in [**IWordBreaker:: init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span><span class="sxs-lookup"><span data-stu-id="2f53d-125">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IWordBreaker::Init**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f53d-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="2f53d-126">Remarks</span></span>

<span data-ttu-id="2f53d-127">**PutAltWord** inserisce una forma alternativa di una parola in [**IWordSink**](iwordsink.md).</span><span class="sxs-lookup"><span data-stu-id="2f53d-127">**PutAltWord** puts an alternative form of a word in the [**IWordSink**](iwordsink.md).</span></span> <span data-ttu-id="2f53d-128">La parola viene posizionata nella stessa posizione della parola originale nell'origine testo (*pTextSource* in [**IWordBreaker:: BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span><span class="sxs-lookup"><span data-stu-id="2f53d-128">The word is put in the same position as the original word in the text source (*pTextSource* in [**IWordBreaker::BreakText**](/windows/win32/api/indexsrv/nf-indexsrv-iwordbreaker-breaktext)).</span></span> <span data-ttu-id="2f53d-129">Per impostazione predefinita, **PutAltWord** termina le parole con un tipo di interruzione **WORDREP \_ break \_ EOW** dal tipo enumerato [**WORDREP \_ \_ tipo di interruzione**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="2f53d-129">By default, **PutAltWord** terminates words with a **WORDREP\_BREAK\_EOW** break type from the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f53d-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f53d-130">Requirements</span></span>



| <span data-ttu-id="2f53d-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f53d-131">Requirement</span></span> | <span data-ttu-id="2f53d-132">Valore</span><span class="sxs-lookup"><span data-stu-id="2f53d-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2f53d-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f53d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2f53d-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f53d-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2f53d-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2f53d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2f53d-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2f53d-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2f53d-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f53d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f53d-138"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f53d-138"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f53d-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f53d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f53d-140">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="2f53d-140">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
