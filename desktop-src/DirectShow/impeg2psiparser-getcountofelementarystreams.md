---
description: "Metodo IMpeg2PsiParser::GetCountOfElementaryStreams: l'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata."
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: Metodo IMpeg2PsiParser::GetCountOfElementaryStreams
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
ms.openlocfilehash: fc81c0a66751751a73a3895fd31fe8651aee8caf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089159"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a><span data-ttu-id="46572-104">Metodo IMpeg2PsiParser::GetCountOfElementaryStreams</span><span class="sxs-lookup"><span data-stu-id="46572-104">IMpeg2PsiParser::GetCountOfElementaryStreams method</span></span>

<span data-ttu-id="46572-105">L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="46572-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="46572-106">Non è un'API DirectShow supportata.</span><span class="sxs-lookup"><span data-stu-id="46572-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="46572-107">Il `GetCountOfElementaryStreams` metodo recupera il numero di flussi elementari in un programma specificato.</span><span class="sxs-lookup"><span data-stu-id="46572-107">The `GetCountOfElementaryStreams` method retrieves the number of elementary streams in a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="46572-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="46572-108">Syntax</span></span>


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="46572-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="46572-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46572-110">*wProgramNumber* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="46572-110">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46572-111">Specifica il campo del \_ numero di programma per il programma, come specificato nel campo PAT.</span><span class="sxs-lookup"><span data-stu-id="46572-111">Specifies the program\_number field for the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="46572-112">*pwVal* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="46572-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46572-113">Puntatore a una variabile che riceve il numero di flussi elementari nel programma.</span><span class="sxs-lookup"><span data-stu-id="46572-113">Pointer to a variable that receives the number of elementary streams in the program.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46572-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="46572-114">Return value</span></span>

<span data-ttu-id="46572-115">Il metodo restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="46572-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="46572-116">I valori possibili includono, ma non solo, i valori illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="46572-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="46572-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="46572-117">Return code</span></span>                                                                          | <span data-ttu-id="46572-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46572-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="46572-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="46572-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="46572-120">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="46572-120">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="46572-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="46572-121">Remarks</span></span>

<span data-ttu-id="46572-122">Usare il **metodo GetRecordProgramNumber** per ottenere il numero di programma.</span><span class="sxs-lookup"><span data-stu-id="46572-122">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="46572-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="46572-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46572-124">**Interfaccia IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="46572-124">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="46572-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="46572-125">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="46572-126">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="46572-126">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




