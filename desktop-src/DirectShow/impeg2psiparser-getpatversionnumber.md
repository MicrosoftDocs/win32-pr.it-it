---
description: L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: 'Metodo IMpeg2PsiParser:: GetPatVersionNumber'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6117060cf0c8d3c56d03e5838376485244fde8d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401123"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a><span data-ttu-id="33523-104">Metodo IMpeg2PsiParser:: GetPatVersionNumber</span><span class="sxs-lookup"><span data-stu-id="33523-104">IMpeg2PsiParser::GetPatVersionNumber method</span></span>

<span data-ttu-id="33523-105">L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="33523-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="33523-106">Non si tratta di un'API DirectShow supportata.</span><span class="sxs-lookup"><span data-stu-id="33523-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="33523-107">Il `GetPatVersionNumber` metodo recupera il \_ campo del numero di versione da Pat.</span><span class="sxs-lookup"><span data-stu-id="33523-107">The `GetPatVersionNumber` method retrieves the version\_number field from the PAT.</span></span> <span data-ttu-id="33523-108">Un flusso di trasporto contiene al massimo un PAT.</span><span class="sxs-lookup"><span data-stu-id="33523-108">A transport stream contains at most one PAT.</span></span> <span data-ttu-id="33523-109">Il numero di versione viene incrementato ogni volta che vengono modificate le informazioni nella tabella.</span><span class="sxs-lookup"><span data-stu-id="33523-109">The version number is incremented whenever the information in the table changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="33523-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33523-110">Syntax</span></span>


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a><span data-ttu-id="33523-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="33523-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33523-112">*pPatVersion* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="33523-112">*pPatVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33523-113">Puntatore a una variabile che riceve il campo del numero di versione \_ .</span><span class="sxs-lookup"><span data-stu-id="33523-113">Pointer to a variable that receives the version\_number field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33523-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33523-114">Return value</span></span>

<span data-ttu-id="33523-115">Il metodo restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33523-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="33523-116">I valori possibili includono, ma non sono limitati, i valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="33523-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="33523-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="33523-117">Return code</span></span>                                                                          | <span data-ttu-id="33523-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33523-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="33523-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="33523-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="33523-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="33523-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="33523-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33523-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33523-122">**Interfaccia IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="33523-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="33523-123">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="33523-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




