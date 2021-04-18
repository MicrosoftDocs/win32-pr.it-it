---
description: L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: 'Metodo IMpeg2PsiParser:: GetPmtVersionNumber'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3af4b20067af52216181848f4cc63ac5a7784ba9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303816"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a><span data-ttu-id="f2e4b-104">Metodo IMpeg2PsiParser:: GetPmtVersionNumber</span><span class="sxs-lookup"><span data-stu-id="f2e4b-104">IMpeg2PsiParser::GetPmtVersionNumber method</span></span>

<span data-ttu-id="f2e4b-105">L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="f2e4b-106">Non si tratta di un'API DirectShow supportata.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="f2e4b-107">Il `GetPmtVersionNumber` metodo recupera il \_ campo del numero di versione da un PMT specificato.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-107">The `GetPmtVersionNumber` method retrieves the version\_number field from a specified PMT.</span></span> <span data-ttu-id="f2e4b-108">Il numero di versione viene incrementato ogni volta che viene modificata la definizione del programma.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-108">The version number is incremented whenever the definition of the program changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2e4b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2e4b-109">Syntax</span></span>


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a><span data-ttu-id="f2e4b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2e4b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2e4b-111">*wProgramNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f2e4b-111">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2e4b-112">Specifica il \_ campo numero di programma del programma, come specificato in Pat.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-112">Specifies the program\_number field of the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="f2e4b-113">*pPmtVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f2e4b-113">*pPmtVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f2e4b-114">Puntatore a una variabile che riceve il campo del numero di versione \_ .</span><span class="sxs-lookup"><span data-stu-id="f2e4b-114">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2e4b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2e4b-115">Return value</span></span>

<span data-ttu-id="f2e4b-116">Il metodo restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f2e4b-116">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="f2e4b-117">I valori possibili includono, ma non sono limitati, i valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-117">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="f2e4b-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f2e4b-118">Return code</span></span>                                                                          | <span data-ttu-id="f2e4b-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2e4b-119">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="f2e4b-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f2e4b-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f2e4b-121">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-121">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f2e4b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2e4b-122">Remarks</span></span>

<span data-ttu-id="f2e4b-123">Usare il metodo **GetRecordProgramNumber** per ottenere il numero di programma.</span><span class="sxs-lookup"><span data-stu-id="f2e4b-123">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="f2e4b-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2e4b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2e4b-125">**Interfaccia IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="f2e4b-125">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="f2e4b-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="f2e4b-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="f2e4b-127">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="f2e4b-127">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




