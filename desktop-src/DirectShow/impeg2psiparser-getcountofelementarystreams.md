---
description: L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: 'Metodo IMpeg2PsiParser:: GetCountOfElementaryStreams'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6593b699592c913940b14c2c26aea42057acfa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303818"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a><span data-ttu-id="80f95-104">Metodo IMpeg2PsiParser:: GetCountOfElementaryStreams</span><span class="sxs-lookup"><span data-stu-id="80f95-104">IMpeg2PsiParser::GetCountOfElementaryStreams method</span></span>

<span data-ttu-id="80f95-105">L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="80f95-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="80f95-106">Non si tratta di un'API DirectShow supportata.</span><span class="sxs-lookup"><span data-stu-id="80f95-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="80f95-107">Il `GetCountOfElementaryStreams` metodo recupera il numero di flussi elementari in un programma specificato.</span><span class="sxs-lookup"><span data-stu-id="80f95-107">The `GetCountOfElementaryStreams` method retrieves the number of elementary streams in a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="80f95-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="80f95-108">Syntax</span></span>


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="80f95-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="80f95-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80f95-110">*wProgramNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80f95-110">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80f95-111">Specifica il \_ campo del numero di programma per il programma, come specificato in Pat.</span><span class="sxs-lookup"><span data-stu-id="80f95-111">Specifies the program\_number field for the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="80f95-112">*pwVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="80f95-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80f95-113">Puntatore a una variabile che riceve il numero di flussi elementari nel programma.</span><span class="sxs-lookup"><span data-stu-id="80f95-113">Pointer to a variable that receives the number of elementary streams in the program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80f95-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="80f95-114">Return value</span></span>

<span data-ttu-id="80f95-115">Il metodo restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="80f95-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="80f95-116">I valori possibili includono, ma non sono limitati, i valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="80f95-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="80f95-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="80f95-117">Return code</span></span>                                                                          | <span data-ttu-id="80f95-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80f95-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="80f95-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="80f95-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="80f95-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="80f95-120">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="80f95-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="80f95-121">Remarks</span></span>

<span data-ttu-id="80f95-122">Usare il metodo **GetRecordProgramNumber** per ottenere il numero di programma.</span><span class="sxs-lookup"><span data-stu-id="80f95-122">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="80f95-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="80f95-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80f95-124">**Interfaccia IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="80f95-124">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="80f95-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="80f95-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="80f95-126">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="80f95-126">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




