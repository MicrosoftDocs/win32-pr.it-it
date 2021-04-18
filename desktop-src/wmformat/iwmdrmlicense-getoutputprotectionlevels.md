---
title: Metodo IWMDRMLicense GetOutputProtectionLevels
description: Il metodo GetOutputProtectionLevels recupera le informazioni relative a tutti i livelli di protezione di output (OPLs) assegnati alla licenza.
ms.assetid: 6596171a-67ac-42cd-80d9-f77507fc58eb
keywords:
- Metodo GetOutputProtectionLevels Windows Media Format
- Metodo GetOutputProtectionLevels Windows Media Format, interfaccia IWMDRMLicense
- Interfaccia IWMDRMLicense-formato Windows Media, metodo GetOutputProtectionLevels
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetOutputProtectionLevels
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5318ecdc8322699ac9d942425a98347799c37715
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299043"
---
# <a name="iwmdrmlicensegetoutputprotectionlevels-method"></a><span data-ttu-id="fd3eb-106">Metodo IWMDRMLicense:: GetOutputProtectionLevels</span><span class="sxs-lookup"><span data-stu-id="fd3eb-106">IWMDRMLicense::GetOutputProtectionLevels method</span></span>

<span data-ttu-id="fd3eb-107">Il metodo **GetOutputProtectionLevels** recupera le informazioni relative a tutti i livelli di protezione di output (OPLs) assegnati alla licenza.</span><span class="sxs-lookup"><span data-stu-id="fd3eb-107">The **GetOutputProtectionLevels** method retrieves information about all output protection levels (OPLs) assigned to the license.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd3eb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fd3eb-108">Syntax</span></span>


```C++
HRESULT GetOutputProtectionLevels(
  [out] WMDRM_OUTPUT_PROTECTION_LEVELS *pOPLs
);
```



## <a name="parameters"></a><span data-ttu-id="fd3eb-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fd3eb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd3eb-110">*pOPLs* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fd3eb-110">*pOPLs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd3eb-111">Puntatore a una struttura dei [**\_ livelli di \_ protezione \_ dell'output WMDRM**](wmdrm-output-protection-levels.md) che riceve le informazioni di OPL.</span><span class="sxs-lookup"><span data-stu-id="fd3eb-111">Pointer to a [**WMDRM\_OUTPUT\_PROTECTION\_LEVELS**](wmdrm-output-protection-levels.md) structure that receives the OPL information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd3eb-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fd3eb-112">Return value</span></span>

<span data-ttu-id="fd3eb-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fd3eb-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fd3eb-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="fd3eb-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fd3eb-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="fd3eb-115">Return code</span></span>                                                                          | <span data-ttu-id="fd3eb-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fd3eb-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fd3eb-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fd3eb-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fd3eb-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="fd3eb-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fd3eb-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="fd3eb-119">Remarks</span></span>

<span data-ttu-id="fd3eb-120">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="fd3eb-120">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd3eb-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fd3eb-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd3eb-122">**Interfaccia IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="fd3eb-122">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





