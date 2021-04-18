---
description: L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: 'Metodo IMpeg2PsiParser:: GetRecordProgramNumber'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2bedc5922ce90fa2fda612f30571f884e75841d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303815"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a><span data-ttu-id="c3077-104">Metodo IMpeg2PsiParser:: GetRecordProgramNumber</span><span class="sxs-lookup"><span data-stu-id="c3077-104">IMpeg2PsiParser::GetRecordProgramNumber method</span></span>

<span data-ttu-id="c3077-105">L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="c3077-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="c3077-106">Non si tratta di un'API DirectShow supportata.</span><span class="sxs-lookup"><span data-stu-id="c3077-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="c3077-107">Il `GetRecordProgramNumber` metodo recupera il numero di programma per un programma specificato.</span><span class="sxs-lookup"><span data-stu-id="c3077-107">The `GetRecordProgramNumber` method retrieves the program number for a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3077-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3077-108">Syntax</span></span>


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="c3077-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3077-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3077-110">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c3077-110">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c3077-111">Specifica la voce del PAT che definisce il programma, indicizzato da zero.</span><span class="sxs-lookup"><span data-stu-id="c3077-111">Specifies the entry in the PAT that defines the program, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="c3077-112">*pwVal* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c3077-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3077-113">Puntatore a una variabile che riceve il \_ campo del numero di programma da Pat.</span><span class="sxs-lookup"><span data-stu-id="c3077-113">Pointer to a variable that receives the program\_number field from the PAT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3077-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3077-114">Return value</span></span>

<span data-ttu-id="c3077-115">Il metodo restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c3077-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="c3077-116">I valori possibili includono, ma non sono limitati, i valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c3077-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="c3077-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c3077-117">Return code</span></span>                                                                          | <span data-ttu-id="c3077-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3077-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="c3077-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c3077-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c3077-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c3077-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c3077-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3077-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3077-122">**Interfaccia IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="c3077-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="c3077-123">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="c3077-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




