---
description: La proprietà ModuleKeys di sola lettura dell'oggetto Error restituisce un puntatore a una raccolta di stringhe contenente le chiavi primarie della riga nel modulo che causa l'errore, una chiave per ogni voce della raccolta.
ms.assetid: b02b609b-4682-4228-b29a-364f079e863c
title: Proprietà Error. ModuleKeys (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.ModuleKeys
- IMsmError.get_ModuleKeys
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 53d2ac37f8864318a83c13672c081ed5dea42b0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326386"
---
# <a name="errormodulekeys-property"></a><span data-ttu-id="d9621-103">Proprietà Error. ModuleKeys</span><span class="sxs-lookup"><span data-stu-id="d9621-103">Error.ModuleKeys property</span></span>

<span data-ttu-id="d9621-104">La proprietà **ModuleKeys** di sola lettura dell'oggetto [**Error**](error-object.md) restituisce un puntatore a una raccolta di stringhe contenente le chiavi primarie della riga nel modulo che causa l'errore, una chiave per ogni voce della raccolta.</span><span class="sxs-lookup"><span data-stu-id="d9621-104">The read-only **ModuleKeys** property of the [**Error**](error-object.md) object returns a pointer to a string collection containing the primary keys of the row in the module causing the error, one key per entry in the collection.</span></span>

<span data-ttu-id="d9621-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d9621-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9621-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9621-106">Syntax</span></span>


```JScript
propVal = Error.ModuleKeys
```



## <a name="property-value"></a><span data-ttu-id="d9621-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d9621-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="d9621-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="d9621-108">Remarks</span></span>

<span data-ttu-id="d9621-109">Il client è responsabile del rilascio della raccolta di stringhe quando non è più necessario.</span><span class="sxs-lookup"><span data-stu-id="d9621-109">The client is responsible for releasing the string collection when it is no longer needed.</span></span>

<span data-ttu-id="d9621-110">La raccolta è vuota se i valori non sono validi per il tipo di errore.</span><span class="sxs-lookup"><span data-stu-id="d9621-110">The collection is empty if the values do not apply to the type of the error.</span></span> <span data-ttu-id="d9621-111">È possibile determinare il tipo di errore chiamando la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d9621-111">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="d9621-112">C++</span><span class="sxs-lookup"><span data-stu-id="d9621-112">C++</span></span>

<span data-ttu-id="d9621-113">Vedere [**ottenere \_**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) la funzione ModuleKeys.</span><span class="sxs-lookup"><span data-stu-id="d9621-113">See [**get\_ModuleKeys**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_modulekeys) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9621-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9621-114">Requirements</span></span>



| <span data-ttu-id="d9621-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9621-115">Requirement</span></span> | <span data-ttu-id="d9621-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d9621-116">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9621-117">Versione</span><span class="sxs-lookup"><span data-stu-id="d9621-117">Version</span></span><br/> | <span data-ttu-id="d9621-118">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="d9621-118">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="d9621-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d9621-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d9621-120"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="d9621-120"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="d9621-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d9621-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="d9621-122"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9621-122"><dt>Mergemod.dll</dt></span></span> </dl> |



 

