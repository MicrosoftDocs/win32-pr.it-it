---
description: Inserisce il modulo Word originale nell'oggetto IWordFormSink.
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: Metodo IWordFormSink::P utWord (search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306099"
---
# <a name="iwordformsinkputword-method"></a><span data-ttu-id="d0ca0-103">IWordFormSink::P metodo utWord</span><span class="sxs-lookup"><span data-stu-id="d0ca0-103">IWordFormSink::PutWord method</span></span>

<span data-ttu-id="d0ca0-104">Inserisce il modulo Word originale nell'oggetto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) .</span><span class="sxs-lookup"><span data-stu-id="d0ca0-104">Puts the original word form in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0ca0-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d0ca0-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="d0ca0-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d0ca0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0ca0-107">*pwcInBuf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0ca0-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ca0-108">Puntatore a un buffer che contiene la forma alternativa finale di una parola, che è sempre la parola originale.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-108">A pointer to a buffer that contains the final alternative form of a word, which is always the original word.</span></span>

</dd> <dt>

<span data-ttu-id="d0ca0-109">*CWC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d0ca0-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0ca0-110">Numero di caratteri in *pwcInBuf*.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0ca0-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d0ca0-111">Return value</span></span>

<span data-ttu-id="d0ca0-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-112">This method can return one of these values.</span></span>



| <span data-ttu-id="d0ca0-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d0ca0-113">Return code</span></span>                                                                          | <span data-ttu-id="d0ca0-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0ca0-114">Description</span></span>                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="d0ca0-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d0ca0-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d0ca0-116">L'operazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-116">The operation was completed successfully.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="d0ca0-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d0ca0-117">Remarks</span></span>

<span data-ttu-id="d0ca0-118">**PutWord** viene chiamato dal metodo [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) dell'implementazione di [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) .</span><span class="sxs-lookup"><span data-stu-id="d0ca0-118">**PutWord** is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="d0ca0-119">Questo metodo gestisce il formato originale di una parola e viene chiamato per ultimo.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-119">This method handles the original form of a word and is called last.</span></span> <span data-ttu-id="d0ca0-120">Tutte le forme alternative precedenti per una parola vengono inserite nell'oggetto [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) chiamando [**IWordFormSink::P utaltword**](iwordformsink-putphrase.md).</span><span class="sxs-lookup"><span data-stu-id="d0ca0-120">All preceding alternative forms for a word are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling [**IWordFormSink::PutAltWord**](iwordformsink-putphrase.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d0ca0-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d0ca0-121">Requirements</span></span>



| <span data-ttu-id="d0ca0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0ca0-122">Requirement</span></span> | <span data-ttu-id="d0ca0-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d0ca0-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ca0-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0ca0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d0ca0-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0ca0-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d0ca0-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d0ca0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d0ca0-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="d0ca0-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d0ca0-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d0ca0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0ca0-129"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="d0ca0-129"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0ca0-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d0ca0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ca0-131">**IWordFormSink**</span><span class="sxs-lookup"><span data-stu-id="d0ca0-131">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
