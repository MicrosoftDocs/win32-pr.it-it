---
description: "Metodo IMpeg2PsiParser::GetPmtVersionNumber: l'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata."
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: Metodo IMpeg2PsiParser::GetPmtVersionNumber
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
ms.openlocfilehash: 6f4fd8d0eba88ba1df54a1cc058bc0a2951b9a19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084559"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a><span data-ttu-id="d7710-104">Metodo IMpeg2PsiParser::GetPmtVersionNumber</span><span class="sxs-lookup"><span data-stu-id="d7710-104">IMpeg2PsiParser::GetPmtVersionNumber method</span></span>

<span data-ttu-id="d7710-105">L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="d7710-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="d7710-106">Non è un'API DirectShow supportata.</span><span class="sxs-lookup"><span data-stu-id="d7710-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="d7710-107">Il `GetPmtVersionNumber` metodo recupera il campo del numero di versione da un \_ pmt specificato.</span><span class="sxs-lookup"><span data-stu-id="d7710-107">The `GetPmtVersionNumber` method retrieves the version\_number field from a specified PMT.</span></span> <span data-ttu-id="d7710-108">Il numero di versione viene incrementato ogni volta che cambia la definizione del programma.</span><span class="sxs-lookup"><span data-stu-id="d7710-108">The version number is incremented whenever the definition of the program changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7710-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d7710-109">Syntax</span></span>


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a><span data-ttu-id="d7710-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d7710-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7710-111">*wProgramNumber* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d7710-111">*wProgramNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7710-112">Specifica il campo \_ del numero di programma del programma, come specificato nel campo PAT.</span><span class="sxs-lookup"><span data-stu-id="d7710-112">Specifies the program\_number field of the program, as given in the PAT.</span></span>

</dd> <dt>

<span data-ttu-id="d7710-113">*pPmtVersion* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="d7710-113">*pPmtVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7710-114">Puntatore a una variabile che riceve il campo del \_ numero di versione.</span><span class="sxs-lookup"><span data-stu-id="d7710-114">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7710-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d7710-115">Return value</span></span>

<span data-ttu-id="d7710-116">Il metodo restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="d7710-116">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="d7710-117">I valori possibili includono, ma non solo, i valori illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d7710-117">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="d7710-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d7710-118">Return code</span></span>                                                                          | <span data-ttu-id="d7710-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d7710-119">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="d7710-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d7710-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d7710-121">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="d7710-121">Success.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7710-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="d7710-122">Remarks</span></span>

<span data-ttu-id="d7710-123">Usare il **metodo GetRecordProgramNumber** per ottenere il numero di programma.</span><span class="sxs-lookup"><span data-stu-id="d7710-123">Use the **GetRecordProgramNumber** method to obtain the program number.</span></span>

## <a name="see-also"></a><span data-ttu-id="d7710-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d7710-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7710-125">**Interfaccia IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="d7710-125">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="d7710-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span><span class="sxs-lookup"><span data-stu-id="d7710-126">**IMpeg2PsiParser::GetRecordProgramNumber**</span></span>](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[<span data-ttu-id="d7710-127">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="d7710-127">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




