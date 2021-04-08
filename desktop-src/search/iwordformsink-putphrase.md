---
description: Inserisce una forma alternativa di una parola nell'oggetto IWordFormSink.
ms.assetid: 4F6A3E88-A17C-4CA3-849D-FF0DC06D5DC3
title: Metodo IWordFormSink::P utAltWord (search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutAltWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 43539bbf67e23bc37ca92f6a961b945ae581e746
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750359"
---
# <a name="iwordformsinkputaltword-method"></a><span data-ttu-id="f4fa8-103">IWordFormSink::P metodo utAltWord</span><span class="sxs-lookup"><span data-stu-id="f4fa8-103">IWordFormSink::PutAltWord method</span></span>

<span data-ttu-id="f4fa8-104">Inserisce una forma alternativa di una parola nell'oggetto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .</span><span class="sxs-lookup"><span data-stu-id="f4fa8-104">Puts an alternative form of a word in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4fa8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f4fa8-105">Syntax</span></span>


```C++
HRESULT PutAltWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="f4fa8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f4fa8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4fa8-107">*pwcInBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4fa8-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4fa8-108">Puntatore a un buffer che contiene una forma alternativa di una parola.</span><span class="sxs-lookup"><span data-stu-id="f4fa8-108">A pointer to a buffer that contains an alternative form of a word.</span></span>

</dd> <dt>

<span data-ttu-id="f4fa8-109">*CWC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f4fa8-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4fa8-110">Numero di caratteri in *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="f4fa8-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4fa8-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f4fa8-111">Return value</span></span>

<span data-ttu-id="f4fa8-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="f4fa8-112">This method can return one of these values.</span></span>



| <span data-ttu-id="f4fa8-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f4fa8-113">Return code</span></span>                                                                                              | <span data-ttu-id="f4fa8-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4fa8-114">Description</span></span>                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f4fa8-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f4fa8-115"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="f4fa8-116">L'operazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="f4fa8-116">The operation was completed successfully.</span></span> <br/>                                                                                             |
| <dl> <span data-ttu-id="f4fa8-117"><dt>**Lingua \_ di \_ \_ parola grande**</dt></span><span class="sxs-lookup"><span data-stu-id="f4fa8-117"><dt>**LANGUAGE\_S\_LARGE\_WORD** </dt></span></span> </dl> | <span data-ttu-id="f4fa8-118">Il valore di *CWC* è maggiore del valore di *UlMaxTokenSize* specificato in [**IStemmer:: init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init).</span><span class="sxs-lookup"><span data-stu-id="f4fa8-118">Value of *cwc* is larger than the value for *ulMaxTokenSize* that is specified in [**IStemmer::Init**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-init).</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="f4fa8-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f4fa8-119">Remarks</span></span>

<span data-ttu-id="f4fa8-120">Questo metodo viene chiamato dal metodo [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) dell'implementazione di [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) .</span><span class="sxs-lookup"><span data-stu-id="f4fa8-120">This method is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="f4fa8-121">Tutte le forme alternative per una parola, eccetto le ultime, vengono inserite nell'oggetto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) chiamando **IWordFormSink::P utaltword**.</span><span class="sxs-lookup"><span data-stu-id="f4fa8-121">All alternative forms for a word, except the last, are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling **IWordFormSink::PutAltWord**.</span></span> <span data-ttu-id="f4fa8-122">Il formato alternativo finale di una parola, che è sempre il formato originale della parola, viene gestito chiamando [**IWordFormSink::P utword**](iwordformsink-putword.md).</span><span class="sxs-lookup"><span data-stu-id="f4fa8-122">The final alternative form of a word, which is always the original form of the word, is handled by calling [**IWordFormSink::PutWord**](iwordformsink-putword.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f4fa8-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f4fa8-123">Requirements</span></span>



| <span data-ttu-id="f4fa8-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4fa8-124">Requirement</span></span> | <span data-ttu-id="f4fa8-125">Valore</span><span class="sxs-lookup"><span data-stu-id="f4fa8-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f4fa8-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4fa8-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f4fa8-127">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f4fa8-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f4fa8-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f4fa8-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f4fa8-129">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f4fa8-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f4fa8-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f4fa8-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4fa8-131"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4fa8-131"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4fa8-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f4fa8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4fa8-133">**IWordFormSink**</span><span class="sxs-lookup"><span data-stu-id="f4fa8-133">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
