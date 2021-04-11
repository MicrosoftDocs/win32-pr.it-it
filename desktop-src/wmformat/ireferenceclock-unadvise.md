---
title: IReferenceClock Unadvise (metodo)
description: Il metodo Unadvise Annulla una richiesta di notifica.
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Metodo Unadvise Windows Media Format
- Unadvise metodo Windows Media Format, interfaccia IReferenceClock
- Interfaccia IReferenceClock-formato Windows Media, metodo Unadvise
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104117124"
---
# <a name="ireferenceclockunadvise-method"></a><span data-ttu-id="95542-106">Metodo IReferenceClock:: Unadvise</span><span class="sxs-lookup"><span data-stu-id="95542-106">IReferenceClock::Unadvise method</span></span>

<span data-ttu-id="95542-107">Il metodo **Unadvise** Annulla una richiesta di notifica.</span><span class="sxs-lookup"><span data-stu-id="95542-107">The **Unadvise** method cancels a notification request.</span></span>

## <a name="syntax"></a><span data-ttu-id="95542-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95542-108">Syntax</span></span>


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a><span data-ttu-id="95542-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="95542-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95542-110">*dwAdviseCookie*</span><span class="sxs-lookup"><span data-stu-id="95542-110">*dwAdviseCookie*</span></span> 
</dt> <dd>

<span data-ttu-id="95542-111">Identificatore della richiesta da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="95542-111">Identifier of the request to remove.</span></span> <span data-ttu-id="95542-112">Usare il valore restituito da AdviseTime nel parametro pdwAdviseCookie.</span><span class="sxs-lookup"><span data-stu-id="95542-112">Use the value returned by AdviseTime in the pdwAdviseCookie parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95542-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95542-113">Return value</span></span>

<span data-ttu-id="95542-114">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="95542-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="95542-115">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="95542-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="95542-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="95542-116">Return code</span></span>                                                                             | <span data-ttu-id="95542-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95542-117">Description</span></span>                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="95542-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="95542-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="95542-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="95542-119">The method succeeded.</span></span><br/>                    |
| <dl> <span data-ttu-id="95542-120"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="95542-120"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="95542-121">L'identificatore passato non esiste.</span><span class="sxs-lookup"><span data-stu-id="95542-121">The identifier passed in does not exist.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="95542-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95542-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95542-123">**Interfaccia IReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="95542-123">**IReferenceClock Interface**</span></span>](ireferenceclock.md)
</dt> </dl>

 

 





