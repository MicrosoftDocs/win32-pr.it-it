---
description: "Metodo IMpeg2PsiParser::GetRecordProgramNumber: l'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata."
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: Metodo IMpeg2PsiParser::GetRecordProgramNumber
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
ms.openlocfilehash: 0fd99178edaa23f2cdf32672a746f79c368b4265
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089139"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a><span data-ttu-id="4d946-104">Metodo IMpeg2PsiParser::GetRecordProgramNumber</span><span class="sxs-lookup"><span data-stu-id="4d946-104">IMpeg2PsiParser::GetRecordProgramNumber method</span></span>

<span data-ttu-id="4d946-105">L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="4d946-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="4d946-106">Non è un'API DirectShow supportata.</span><span class="sxs-lookup"><span data-stu-id="4d946-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="4d946-107">Il `GetRecordProgramNumber` metodo recupera il numero di programma per un programma specificato.</span><span class="sxs-lookup"><span data-stu-id="4d946-107">The `GetRecordProgramNumber` method retrieves the program number for a specified program.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d946-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4d946-108">Syntax</span></span>


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a><span data-ttu-id="4d946-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="4d946-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d946-110">*dwIndex* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="4d946-110">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d946-111">Specifica la voce in PAT che definisce il programma, indicizzata da zero.</span><span class="sxs-lookup"><span data-stu-id="4d946-111">Specifies the entry in the PAT that defines the program, indexed from zero.</span></span>

</dd> <dt>

<span data-ttu-id="4d946-112">*pwVal* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="4d946-112">*pwVal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4d946-113">Puntatore a una variabile che riceve il campo del \_ numero di programma da PAT.</span><span class="sxs-lookup"><span data-stu-id="4d946-113">Pointer to a variable that receives the program\_number field from the PAT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d946-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4d946-114">Return value</span></span>

<span data-ttu-id="4d946-115">Il metodo restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="4d946-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="4d946-116">I valori possibili includono, ma non sono limitati, i valori illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="4d946-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="4d946-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="4d946-117">Return code</span></span>                                                                          | <span data-ttu-id="4d946-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d946-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="4d946-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4d946-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4d946-120">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="4d946-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4d946-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4d946-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d946-122">**Interfaccia IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="4d946-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="4d946-123">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="4d946-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




