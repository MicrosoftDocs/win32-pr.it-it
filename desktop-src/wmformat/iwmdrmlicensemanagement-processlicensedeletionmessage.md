---
title: Metodo IWMDRMLicenseManagement ProcessLicenseDeletionMessage (wmdrmsdk. h)
description: Il metodo ProcessLicenseDeletion Elimina una licenza che è stata importata per il contenuto originariamente protetto con un altro sistema di protezione del contenuto.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Metodo ProcessLicenseDeletionMessage Windows Media Format
- Metodo ProcessLicenseDeletionMessage Windows Media Format, interfaccia IWMDRMLicenseManagement
- Interfaccia IWMDRMLicenseManagement-formato Windows Media, metodo ProcessLicenseDeletionMessage
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9338c1bc4ef78e658cc25ab95f5c50556af3ed09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327466"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a><span data-ttu-id="22faf-106">IWMDRMLicenseManagement::P metodo rocessLicenseDeletionMessage</span><span class="sxs-lookup"><span data-stu-id="22faf-106">IWMDRMLicenseManagement::ProcessLicenseDeletionMessage method</span></span>

<span data-ttu-id="22faf-107">Il metodo **ProcessLicenseDeletion** Elimina una licenza che è stata importata per il contenuto originariamente protetto con un altro sistema di protezione del contenuto.</span><span class="sxs-lookup"><span data-stu-id="22faf-107">The **ProcessLicenseDeletion** method deletes a license that was imported for content originally protected with another content protection system.</span></span>

## <a name="syntax"></a><span data-ttu-id="22faf-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22faf-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a><span data-ttu-id="22faf-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="22faf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22faf-110">*bstrDeletionMessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22faf-110">*bstrDeletionMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22faf-111">Messaggio che identifica la licenza da eliminare.</span><span class="sxs-lookup"><span data-stu-id="22faf-111">Message identifying the license to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22faf-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22faf-112">Return value</span></span>

<span data-ttu-id="22faf-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="22faf-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="22faf-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="22faf-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="22faf-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="22faf-115">Return code</span></span>                                                                          | <span data-ttu-id="22faf-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22faf-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="22faf-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22faf-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="22faf-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="22faf-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="22faf-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="22faf-119">Remarks</span></span>

<span data-ttu-id="22faf-120">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="22faf-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="22faf-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22faf-121">Requirements</span></span>



| <span data-ttu-id="22faf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="22faf-122">Requirement</span></span> | <span data-ttu-id="22faf-123">Valore</span><span class="sxs-lookup"><span data-stu-id="22faf-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="22faf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22faf-124">Header</span></span><br/> | <dl> <span data-ttu-id="22faf-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="22faf-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22faf-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22faf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22faf-127">**Interfaccia IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="22faf-127">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





