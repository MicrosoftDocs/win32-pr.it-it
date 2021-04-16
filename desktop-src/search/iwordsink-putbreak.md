---
description: Inserisce un'interruzioni dopo la parola precedente.
ms.assetid: C8622067-D8CE-4099-8B9F-941720F4706B
title: Metodo IWordSink::P utBreak (search. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordSink.PutBreak
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: c6407f1307b4860960c5202af13de736c7921139
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342931"
---
# <a name="iwordsinkputbreak-method"></a><span data-ttu-id="e248b-103">IWordSink::P metodo utBreak</span><span class="sxs-lookup"><span data-stu-id="e248b-103">IWordSink::PutBreak method</span></span>

<span data-ttu-id="e248b-104">Inserisce un'interruzioni dopo la parola precedente.</span><span class="sxs-lookup"><span data-stu-id="e248b-104">Puts a break after the preceding word.</span></span>

## <a name="syntax"></a><span data-ttu-id="e248b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e248b-105">Syntax</span></span>


```C++
HRESULT PutBreak(
  [in] WORDREP_BREAK_TYPE breakType
);
```



## <a name="parameters"></a><span data-ttu-id="e248b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e248b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e248b-107">*breakType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e248b-107">*breakType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e248b-108">Valore del [**\_ \_ tipo di WORDREP break**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) che indica il tipo di interruzioni inserite dal WordSink dopo la parola precedente.</span><span class="sxs-lookup"><span data-stu-id="e248b-108">A value from [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) that indicates the type of break that the WordSink inserts after the preceding word.</span></span> <span data-ttu-id="e248b-109">Ogni break occupa una posizione univoca nell'indice.</span><span class="sxs-lookup"><span data-stu-id="e248b-109">Each break occupies a unique position in the index.</span></span> <span data-ttu-id="e248b-110">Pertanto, l'inserimento di interruzioni tra le parole cambia la distanza relativa tra le parole.</span><span class="sxs-lookup"><span data-stu-id="e248b-110">Therefore, inserting breaks between words changes the relative distance between words.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e248b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e248b-111">Return value</span></span>

<span data-ttu-id="e248b-112">Questo metodo può restituire uno di questi valori.</span><span class="sxs-lookup"><span data-stu-id="e248b-112">This method can return one of these values.</span></span>



| <span data-ttu-id="e248b-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e248b-113">Return code</span></span>                                                                          | <span data-ttu-id="e248b-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e248b-114">Description</span></span>                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="e248b-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e248b-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e248b-116">L'operazione è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="e248b-116">The operation was completed successfully.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e248b-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e248b-117">Remarks</span></span>

<span data-ttu-id="e248b-118">I metodi [**IWordSinkPutWord**](iwordsink-putword.md) e [**IWordSink::P utaltword**](iwordsink-putaltword.md) inseriscono automaticamente un'interruzioni di fine della parola (EOW, indicata dall' \_ elemento WORDREP break \_ EOW del tipo enumerato [**WORDREP \_ \_ break**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) ) dopo ogni parola.</span><span class="sxs-lookup"><span data-stu-id="e248b-118">The [**IWordSinkPutWord**](iwordsink-putword.md) and [**IWordSink::PutAltWord**](iwordsink-putaltword.md) methods automatically insert an end-of-word break (EOW, indicated by the WORDREP\_BREAK\_EOW element of the [**WORDREP\_BREAK\_TYPE**](/previous-versions/windows/desktop/legacy/ff819130(v=vs.85)) enumerated type) after each word.</span></span> <span data-ttu-id="e248b-119">Chiamare il metodo **PutBreak** per inserire un tipo di interruzioni diverso dalla fine della parola.</span><span class="sxs-lookup"><span data-stu-id="e248b-119">Call the **PutBreak** method to insert a break type other than end of word.</span></span> <span data-ttu-id="e248b-120">Questo metodo non modifica il buffer del testo di origine (*pSourceText*) o incrementa il numero di caratteri (*CWC*).</span><span class="sxs-lookup"><span data-stu-id="e248b-120">This method does not change the source text buffer (*pSourceText*) or increment the character count (*cwc*).</span></span> <span data-ttu-id="e248b-121">Tuttavia, incrementa la posizione corrente nell'indice e influiscono sui risultati della query.</span><span class="sxs-lookup"><span data-stu-id="e248b-121">However, it does increment the current position in the index and affects query results.</span></span>

## <a name="requirements"></a><span data-ttu-id="e248b-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e248b-122">Requirements</span></span>



| <span data-ttu-id="e248b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e248b-123">Requirement</span></span> | <span data-ttu-id="e248b-124">Valore</span><span class="sxs-lookup"><span data-stu-id="e248b-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e248b-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e248b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e248b-126">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e248b-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e248b-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e248b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e248b-128">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e248b-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e248b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e248b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e248b-130"><dt>Search. h</dt></span><span class="sxs-lookup"><span data-stu-id="e248b-130"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e248b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e248b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e248b-132">**IWordSink**</span><span class="sxs-lookup"><span data-stu-id="e248b-132">**IWordSink**</span></span>](iwordsink.md)
</dt> </dl>

 

 
