---
description: "Metodo IMpeg2PsiParser::GetCountOfPrograms: l'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata."
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: Metodo IMpeg2PsiParser::GetCountOfPrograms
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
ms.openlocfilehash: d6bfe698a45ea1cfe0a4bac6e65b839292bc1996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119429"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a><span data-ttu-id="7bd31-104">Metodo IMpeg2PsiParser::GetCountOfPrograms</span><span class="sxs-lookup"><span data-stu-id="7bd31-104">IMpeg2PsiParser::GetCountOfPrograms method</span></span>

<span data-ttu-id="7bd31-105">L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="7bd31-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="7bd31-106">Non è un'API DirectShow supportata.</span><span class="sxs-lookup"><span data-stu-id="7bd31-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="7bd31-107">Il `GetCountOfPrograms` metodo recupera il numero di programmi nel flusso di trasporto.</span><span class="sxs-lookup"><span data-stu-id="7bd31-107">The `GetCountOfPrograms` method retrieves the number of programs in the transport stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bd31-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7bd31-108">Syntax</span></span>


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a><span data-ttu-id="7bd31-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="7bd31-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bd31-110">*pNumOfPrograms* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="7bd31-110">*pNumOfPrograms* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7bd31-111">Puntatore a una variabile che riceve il numero di programmi.</span><span class="sxs-lookup"><span data-stu-id="7bd31-111">Pointer to a variable that receives the number of programs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bd31-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7bd31-112">Return value</span></span>

<span data-ttu-id="7bd31-113">Il metodo restituisce un valore HRESULT.</span><span class="sxs-lookup"><span data-stu-id="7bd31-113">The method returns an HRESULT value.</span></span> <span data-ttu-id="7bd31-114">I valori possibili includono, ma non solo, i valori illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7bd31-114">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="7bd31-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7bd31-115">Return code</span></span>                                                                          | <span data-ttu-id="7bd31-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7bd31-116">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="7bd31-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7bd31-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="7bd31-118">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="7bd31-118">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="7bd31-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7bd31-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bd31-120">**Interfaccia IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="7bd31-120">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="7bd31-121">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="7bd31-121">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




