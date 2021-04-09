---
description: L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: 'Metodo IMpeg2PsiParser:: GetCountOfPrograms'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: e4f01b2a360465b9670b52547cff1ff4c312a705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876729"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a><span data-ttu-id="8b953-104">Metodo IMpeg2PsiParser:: GetCountOfPrograms</span><span class="sxs-lookup"><span data-stu-id="8b953-104">IMpeg2PsiParser::GetCountOfPrograms method</span></span>

<span data-ttu-id="8b953-105">L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="8b953-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="8b953-106">Non si tratta di un'API DirectShow supportata.</span><span class="sxs-lookup"><span data-stu-id="8b953-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="8b953-107">Il `GetCountOfPrograms` metodo recupera il numero di programmi nel flusso di trasporto.</span><span class="sxs-lookup"><span data-stu-id="8b953-107">The `GetCountOfPrograms` method retrieves the number of programs in the transport stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b953-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8b953-108">Syntax</span></span>


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a><span data-ttu-id="8b953-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8b953-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b953-110">*pNumOfPrograms* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8b953-110">*pNumOfPrograms* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b953-111">Puntatore a una variabile che riceve il numero di programmi.</span><span class="sxs-lookup"><span data-stu-id="8b953-111">Pointer to a variable that receives the number of programs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b953-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8b953-112">Return value</span></span>

<span data-ttu-id="8b953-113">Il metodo restituisce un valore HRESULT.</span><span class="sxs-lookup"><span data-stu-id="8b953-113">The method returns an HRESULT value.</span></span> <span data-ttu-id="8b953-114">I valori possibili includono, ma non sono limitati, i valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8b953-114">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="8b953-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8b953-115">Return code</span></span>                                                                          | <span data-ttu-id="8b953-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8b953-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="8b953-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8b953-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8b953-118">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="8b953-118">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8b953-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8b953-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b953-120">**Interfaccia IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="8b953-120">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="8b953-121">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="8b953-121">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




