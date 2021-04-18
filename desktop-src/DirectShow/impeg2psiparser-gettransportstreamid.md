---
description: L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: 'Metodo IMpeg2PsiParser:: GetTransportStreamId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetTransportStreamId
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9615c50d8d16aa6d78e3e1b83a3ec0e356c6cb50
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304180"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a><span data-ttu-id="a39f0-104">Metodo IMpeg2PsiParser:: GetTransportStreamId</span><span class="sxs-lookup"><span data-stu-id="a39f0-104">IMpeg2PsiParser::GetTransportStreamId method</span></span>

<span data-ttu-id="a39f0-105">L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="a39f0-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="a39f0-106">Non si tratta di un'API DirectShow supportata.</span><span class="sxs-lookup"><span data-stu-id="a39f0-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="a39f0-107">Il `GetTransportStreamId` metodo recupera il \_ \_ campo ID del flusso di trasporto da Pat.</span><span class="sxs-lookup"><span data-stu-id="a39f0-107">The `GetTransportStreamId` method retrieves the transport\_stream\_id field from the PAT.</span></span> <span data-ttu-id="a39f0-108">Questo valore è definito dall'utente e può essere usato per distinguere un flusso di trasporto specifico da altri flussi nella stessa rete.</span><span class="sxs-lookup"><span data-stu-id="a39f0-108">This value is defined by the user, and can be used to distinguish a particular transport stream from other streams on the same network.</span></span> <span data-ttu-id="a39f0-109">Un flusso di trasporto contiene al massimo un PAT.</span><span class="sxs-lookup"><span data-stu-id="a39f0-109">A transport stream contains at most one PAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="a39f0-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a39f0-110">Syntax</span></span>


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a><span data-ttu-id="a39f0-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="a39f0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a39f0-112">*pStreamId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a39f0-112">*pStreamId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a39f0-113">Puntatore a una variabile che riceve il \_ campo ID del flusso di trasporto \_ .</span><span class="sxs-lookup"><span data-stu-id="a39f0-113">Pointer to a variable that receives the transport\_stream\_id field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a39f0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a39f0-114">Return value</span></span>

<span data-ttu-id="a39f0-115">Il metodo restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a39f0-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="a39f0-116">I valori possibili includono, ma non sono limitati, i valori mostrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a39f0-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="a39f0-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a39f0-117">Return code</span></span>                                                                          | <span data-ttu-id="a39f0-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a39f0-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="a39f0-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a39f0-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a39f0-120">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a39f0-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="a39f0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a39f0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a39f0-122">**Interfaccia IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="a39f0-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="a39f0-123">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="a39f0-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




