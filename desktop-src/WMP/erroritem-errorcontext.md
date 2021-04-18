---
title: ErrorItem. errorContext
description: La proprietà errorContext recupera un valore che indica il contesto dell'errore.
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- Media Player Windows ErrorItem. errorContext
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324742"
---
# <a name="erroritemerrorcontext"></a><span data-ttu-id="87b1f-104">ErrorItem. errorContext</span><span class="sxs-lookup"><span data-stu-id="87b1f-104">ErrorItem.errorContext</span></span>

<span data-ttu-id="87b1f-105">La proprietà **errorContext** recupera un valore che indica il contesto dell'errore.</span><span class="sxs-lookup"><span data-stu-id="87b1f-105">The **errorContext** property retrieves a value indicating the context of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a><span data-ttu-id="87b1f-106">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="87b1f-106">Possible Values</span></span>

<span data-ttu-id="87b1f-107">Questa proprietà è una **stringa** di sola lettura che rappresenta il codice del contesto dell'errore.</span><span class="sxs-lookup"><span data-stu-id="87b1f-107">This property is a read-only **String** that represents the error context code.</span></span>

## <a name="remarks"></a><span data-ttu-id="87b1f-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="87b1f-108">Remarks</span></span>

<span data-ttu-id="87b1f-109">Il contesto di errore è costituito dalle informazioni utilizzate da Microsoft per fornire informazioni aggiuntive per il personale del supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="87b1f-109">The error context is information that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="87b1f-110">**Windows Media Player 10 Mobile:** Questa proprietà restituisce sempre una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="87b1f-110">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="87b1f-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="87b1f-111">Requirements</span></span>



| <span data-ttu-id="87b1f-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="87b1f-112">Requirement</span></span> | <span data-ttu-id="87b1f-113">Valore</span><span class="sxs-lookup"><span data-stu-id="87b1f-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="87b1f-114">Versione</span><span class="sxs-lookup"><span data-stu-id="87b1f-114">Version</span></span><br/> | <span data-ttu-id="87b1f-115">Windows Media Player versione 7,0 o successiva</span><span class="sxs-lookup"><span data-stu-id="87b1f-115">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="87b1f-116">DLL</span><span class="sxs-lookup"><span data-stu-id="87b1f-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="87b1f-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87b1f-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87b1f-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="87b1f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b1f-119">**Oggetto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="87b1f-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





