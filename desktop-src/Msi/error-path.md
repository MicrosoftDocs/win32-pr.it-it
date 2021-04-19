---
description: In Windows Installer versioni 1,0 e 1,1 la proprietà Path è sempre la stringa vuota. Le versioni future possono usare questo valore per restituire il percorso del file o della directory che non è stato possibile creare.
ms.assetid: b79dd347-acda-47d7-aa3b-c0f9a6ca1d3b
title: Proprietà Error. Path (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Path
- IMsmError.get_Path
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 5a2e462790d6f929943fe2fe364228cd73d3deb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326377"
---
# <a name="errorpath-property"></a><span data-ttu-id="7b5ae-104">Proprietà Error. Path</span><span class="sxs-lookup"><span data-stu-id="7b5ae-104">Error.Path property</span></span>

<span data-ttu-id="7b5ae-105">In Windows Installer versioni 1,0 e 1,1 la proprietà Path è sempre la stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-105">In Windows Installer versions 1.0 and 1.1 the Path property is always the empty string.</span></span> <span data-ttu-id="7b5ae-106">Le versioni future possono usare questo valore per restituire il percorso del file o della directory che non è stato possibile creare.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-106">Future versions may use this value to return the path to the file or directory that could not be created.</span></span>

<span data-ttu-id="7b5ae-107">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b5ae-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b5ae-108">Syntax</span></span>


```JScript
propVal = Error.Path
```



## <a name="property-value"></a><span data-ttu-id="7b5ae-109">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7b5ae-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="7b5ae-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b5ae-110">Remarks</span></span>

<span data-ttu-id="7b5ae-111">Questo valore è valido solo per errori di tipo msmErrorFileCreate o msmErrorDirCreate.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-111">This value is only valid for errors of type msmErrorFileCreate or msmErrorDirCreate.</span></span> <span data-ttu-id="7b5ae-112">È possibile determinare il tipo di errore chiamando la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="7b5ae-112">You can determine the type of error by calling [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="7b5ae-113">C++</span><span class="sxs-lookup"><span data-stu-id="7b5ae-113">C++</span></span>

<span data-ttu-id="7b5ae-114">Vedere [**ottenere \_**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) la funzione PATH.</span><span class="sxs-lookup"><span data-stu-id="7b5ae-114">See [**get\_Path**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_path) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b5ae-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b5ae-115">Requirements</span></span>



| <span data-ttu-id="7b5ae-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b5ae-116">Requirement</span></span> | <span data-ttu-id="7b5ae-117">Valore</span><span class="sxs-lookup"><span data-stu-id="7b5ae-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b5ae-118">Versione</span><span class="sxs-lookup"><span data-stu-id="7b5ae-118">Version</span></span><br/> | <span data-ttu-id="7b5ae-119">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="7b5ae-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="7b5ae-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b5ae-120">Header</span></span><br/>  | <dl> <span data-ttu-id="7b5ae-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b5ae-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b5ae-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7b5ae-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7b5ae-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b5ae-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

