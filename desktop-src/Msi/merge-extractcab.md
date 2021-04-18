---
description: Il metodo ExtractCAB dell'oggetto merge estrae il file con estensione cab incorporato da un modulo e lo salva come file specificato. Il programma di installazione crea questo file se non esiste già e sovrascritto, se esistente.
ms.assetid: a6fe8b69-8f4a-45f7-b7e6-7620a00500bb
title: Metodo merge. ExtractCAB (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractCAB
- IMsmMerge.ExtractCAB
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: d0bdc79fb0087456d035bf732faca384b35b2a9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324918"
---
# <a name="mergeextractcab-method"></a><span data-ttu-id="e0851-104">Merge. ExtractCAB, metodo</span><span class="sxs-lookup"><span data-stu-id="e0851-104">Merge.ExtractCAB method</span></span>

<span data-ttu-id="e0851-105">Il metodo **ExtractCAB** dell'oggetto [**merge**](merge-object.md) estrae il file con estensione cab incorporato da un modulo e lo salva come file specificato.</span><span class="sxs-lookup"><span data-stu-id="e0851-105">The **ExtractCAB** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and saves it as the specified file.</span></span> <span data-ttu-id="e0851-106">Il programma di installazione crea questo file se non esiste già e sovrascritto, se esistente.</span><span class="sxs-lookup"><span data-stu-id="e0851-106">The installer creates this file if it does not already exist and overwritten if it does exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0851-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e0851-107">Syntax</span></span>


```JScript
Merge.ExtractCAB(
  FileName
)
```



## <a name="parameters"></a><span data-ttu-id="e0851-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e0851-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0851-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="e0851-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="e0851-110">Il file di destinazione completo.</span><span class="sxs-lookup"><span data-stu-id="e0851-110">The fully qualified destination file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0851-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e0851-111">Return value</span></span>

<span data-ttu-id="e0851-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e0851-112">This method does not return a value.</span></span>

## <a name="c"></a><span data-ttu-id="e0851-113">C++</span><span class="sxs-lookup"><span data-stu-id="e0851-113">C++</span></span>

<span data-ttu-id="e0851-114">Vedere funzione [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) .</span><span class="sxs-lookup"><span data-stu-id="e0851-114">See [**ExtractCAB**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractcab) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0851-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e0851-115">Requirements</span></span>



| <span data-ttu-id="e0851-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0851-116">Requirement</span></span> | <span data-ttu-id="e0851-117">Valore</span><span class="sxs-lookup"><span data-stu-id="e0851-117">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e0851-118">Versione</span><span class="sxs-lookup"><span data-stu-id="e0851-118">Version</span></span><br/> | <span data-ttu-id="e0851-119">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="e0851-119">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="e0851-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e0851-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e0851-121"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0851-121"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="e0851-122">DLL</span><span class="sxs-lookup"><span data-stu-id="e0851-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="e0851-123"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e0851-123"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
