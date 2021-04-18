---
description: La proprietà del linguaggio di sola lettura dell'oggetto Error restituisce il LANGID dell'errore corrente.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Proprietà Error. Language (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6c80802c41f076a2b1c0b320b591bc591da8546e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329750"
---
# <a name="errorlanguage-property"></a><span data-ttu-id="fa5c4-103">Proprietà Error. Language</span><span class="sxs-lookup"><span data-stu-id="fa5c4-103">Error.Language property</span></span>

<span data-ttu-id="fa5c4-104">La proprietà del **linguaggio** di sola lettura dell'oggetto [**Error**](error-object.md) restituisce il **LangID** dell'errore corrente.</span><span class="sxs-lookup"><span data-stu-id="fa5c4-104">The read-only **Language** property of the [**Error**](error-object.md) object returns the **LANGID** of the current error.</span></span>

<span data-ttu-id="fa5c4-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="fa5c4-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa5c4-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fa5c4-106">Syntax</span></span>


```JScript
propVal = Error.Language
```



## <a name="property-value"></a><span data-ttu-id="fa5c4-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="fa5c4-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="fa5c4-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="fa5c4-108">Remarks</span></span>

<span data-ttu-id="fa5c4-109">Il valore della proprietà **Language** è-1, a meno che l'errore non sia di tipo MsmErrorLanguageUnsupported o msmErrorLanguageFailed.</span><span class="sxs-lookup"><span data-stu-id="fa5c4-109">The value of the **Language** property is -1 unless the error is of type msmErrorLanguageUnsupported or msmErrorLanguageFailed.</span></span> <span data-ttu-id="fa5c4-110">È possibile determinare il tipo di errore chiamando la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="fa5c4-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="fa5c4-111">C++</span><span class="sxs-lookup"><span data-stu-id="fa5c4-111">C++</span></span>

<span data-ttu-id="fa5c4-112">Vedere [**get \_ Language function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).</span><span class="sxs-lookup"><span data-stu-id="fa5c4-112">See [**get\_Language Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa5c4-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fa5c4-113">Requirements</span></span>



| <span data-ttu-id="fa5c4-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa5c4-114">Requirement</span></span> | <span data-ttu-id="fa5c4-115">Valore</span><span class="sxs-lookup"><span data-stu-id="fa5c4-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fa5c4-116">Versione</span><span class="sxs-lookup"><span data-stu-id="fa5c4-116">Version</span></span><br/> | <span data-ttu-id="fa5c4-117">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="fa5c4-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="fa5c4-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fa5c4-118">Header</span></span><br/>  | <dl> <span data-ttu-id="fa5c4-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa5c4-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="fa5c4-120">DLL</span><span class="sxs-lookup"><span data-stu-id="fa5c4-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="fa5c4-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa5c4-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

