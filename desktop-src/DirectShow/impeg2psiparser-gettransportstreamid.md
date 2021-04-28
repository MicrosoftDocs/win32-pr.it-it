---
description: "Metodo IMpeg2PsiParser::GetTransportStreamId: l'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata."
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: Metodo IMpeg2PsiParser::GetTransportStreamId
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
ms.openlocfilehash: a24253b021abacf398a3a169b63bbb2f01ec2354
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084569"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a><span data-ttu-id="c3cb9-104">Metodo IMpeg2PsiParser::GetTransportStreamId</span><span class="sxs-lookup"><span data-stu-id="c3cb9-104">IMpeg2PsiParser::GetTransportStreamId method</span></span>

<span data-ttu-id="c3cb9-105">L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-105">The implementation of this method is provided as sample code with the DirectShow SDK.</span></span> <span data-ttu-id="c3cb9-106">Non è un'API DirectShow supportata.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-106">It is not a supported DirectShow API.</span></span>

<span data-ttu-id="c3cb9-107">Il `GetTransportStreamId` metodo recupera il campo \_ \_ dell'ID del flusso di trasporto da PAT.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-107">The `GetTransportStreamId` method retrieves the transport\_stream\_id field from the PAT.</span></span> <span data-ttu-id="c3cb9-108">Questo valore è definito dall'utente e può essere usato per distinguere un flusso di trasporto specifico da altri flussi nella stessa rete.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-108">This value is defined by the user, and can be used to distinguish a particular transport stream from other streams on the same network.</span></span> <span data-ttu-id="c3cb9-109">Un flusso di trasporto contiene al massimo un PAT.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-109">A transport stream contains at most one PAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3cb9-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c3cb9-110">Syntax</span></span>


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a><span data-ttu-id="c3cb9-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="c3cb9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c3cb9-112">*pStreamId* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="c3cb9-112">*pStreamId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c3cb9-113">Puntatore a una variabile che riceve il campo \_ dell'ID del flusso di \_ trasporto.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-113">Pointer to a variable that receives the transport\_stream\_id field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c3cb9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c3cb9-114">Return value</span></span>

<span data-ttu-id="c3cb9-115">Il metodo restituisce un **valore HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="c3cb9-115">The method returns an **HRESULT** value.</span></span> <span data-ttu-id="c3cb9-116">I valori possibili includono, ma non solo, i valori illustrati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-116">Possible values include, but are not limited to, the values shown in the following table.</span></span>



| <span data-ttu-id="c3cb9-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c3cb9-117">Return code</span></span>                                                                          | <span data-ttu-id="c3cb9-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3cb9-118">Description</span></span>         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="c3cb9-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c3cb9-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c3cb9-120">Operazione completata.</span><span class="sxs-lookup"><span data-stu-id="c3cb9-120">Success.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c3cb9-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c3cb9-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3cb9-122">**Interfaccia IMpeg2PsiParser**</span><span class="sxs-lookup"><span data-stu-id="c3cb9-122">**IMpeg2PsiParser Interface**</span></span>](impeg2psiparser.md)
</dt> <dt>

[<span data-ttu-id="c3cb9-123">Esempio di filtro del parser PSI</span><span class="sxs-lookup"><span data-stu-id="c3cb9-123">PSI Parser Filter Sample</span></span>](psi-parser-filter-sample.md)
</dt> </dl>

 

 




