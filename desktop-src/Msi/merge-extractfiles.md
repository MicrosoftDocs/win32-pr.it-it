---
description: Il metodo ExtractFiles dell'oggetto merge estrae il file con estensione cab incorporato da un modulo e quindi scrive tali file nella directory di destinazione.
ms.assetid: 846355d6-32f2-4b04-91dc-acd60445fbd9
title: Metodo merge. ExtractFiles (Advpub. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFiles
- IMsmMerge.ExtractFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 3869dc37b841d386891eb70940054bd78805bf94
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327805"
---
# <a name="mergeextractfiles-method"></a><span data-ttu-id="14a31-103">Merge. ExtractFiles, metodo</span><span class="sxs-lookup"><span data-stu-id="14a31-103">Merge.ExtractFiles method</span></span>

<span data-ttu-id="14a31-104">Il metodo **ExtractFiles** dell'oggetto [**merge**](merge-object.md) estrae il file con estensione cab incorporato da un modulo e quindi scrive tali file nella directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="14a31-104">The **ExtractFiles** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="14a31-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14a31-105">Syntax</span></span>


```JScript
Merge.ExtractFiles(
  Path
)
```



## <a name="parameters"></a><span data-ttu-id="14a31-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="14a31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14a31-107">*Percorso*</span><span class="sxs-lookup"><span data-stu-id="14a31-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="14a31-108">Directory di destinazione completo.</span><span class="sxs-lookup"><span data-stu-id="14a31-108">The fully qualified destination directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14a31-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14a31-109">Return value</span></span>

<span data-ttu-id="14a31-110">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="14a31-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="14a31-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="14a31-111">Remarks</span></span>

<span data-ttu-id="14a31-112">Tutti i file nella directory di destinazione con lo stesso nome verranno sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="14a31-112">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="14a31-113">Il percorso viene creato se non esiste già.</span><span class="sxs-lookup"><span data-stu-id="14a31-113">The path is created if it does not already exist.</span></span>

<span data-ttu-id="14a31-114">**ExtractFiles** estrae sempre i file usando nomi di file brevi per il percorso.</span><span class="sxs-lookup"><span data-stu-id="14a31-114">**ExtractFiles** always extracts files using short file names for the path.</span></span> <span data-ttu-id="14a31-115">Per usare nomi di file lunghi per il percorso, usare il [**Metodo ExtractFilesEx**](merge-extractfilesex.md).</span><span class="sxs-lookup"><span data-stu-id="14a31-115">To use long file names for the path, use the [**ExtractFilesEx method**](merge-extractfilesex.md).</span></span>

### <a name="c"></a><span data-ttu-id="14a31-116">C++</span><span class="sxs-lookup"><span data-stu-id="14a31-116">C++</span></span>

<span data-ttu-id="14a31-117">Vedere funzione [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) .</span><span class="sxs-lookup"><span data-stu-id="14a31-117">See [**ExtractFiles**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-extractfiles) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="14a31-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14a31-118">Requirements</span></span>



| <span data-ttu-id="14a31-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="14a31-119">Requirement</span></span> | <span data-ttu-id="14a31-120">Valore</span><span class="sxs-lookup"><span data-stu-id="14a31-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14a31-121">Versione</span><span class="sxs-lookup"><span data-stu-id="14a31-121">Version</span></span><br/> | <span data-ttu-id="14a31-122">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="14a31-122">Mergemod.dll 1.0 or later</span></span><br/>                                                                     |
| <span data-ttu-id="14a31-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14a31-123">Header</span></span><br/>  | <dl> <span data-ttu-id="14a31-124"><dt>Advpub. h (include Mergemod. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14a31-124"><dt>Advpub.h (include Mergemod.h)</dt></span></span> </dl> |
| <span data-ttu-id="14a31-125">DLL</span><span class="sxs-lookup"><span data-stu-id="14a31-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="14a31-126"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14a31-126"><dt>Mergemod.dll</dt></span></span> </dl>                  |



 

 
