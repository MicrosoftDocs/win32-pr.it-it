---
description: Il metodo ExtractFilesEx dell'oggetto merge estrae il file con estensione cab incorporato da un modulo e quindi scrive tali file nella directory di destinazione.
ms.assetid: 8b063052-4f92-466a-9c52-bda26ed13d5c
title: Metodo merge. ExtractFilesEx (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.ExtractFilesEx
- IMsmMerge.ExtractFilesEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: be6aa1001be0d3ecd6cbb9c4cd1d8c04b4649f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332940"
---
# <a name="mergeextractfilesex-method"></a><span data-ttu-id="3b968-103">Merge. ExtractFilesEx, metodo</span><span class="sxs-lookup"><span data-stu-id="3b968-103">Merge.ExtractFilesEx method</span></span>

<span data-ttu-id="3b968-104">Il metodo **ExtractFilesEx** dell'oggetto [**merge**](merge-object.md) estrae il file con estensione cab incorporato da un modulo e quindi scrive tali file nella directory di destinazione.</span><span class="sxs-lookup"><span data-stu-id="3b968-104">The **ExtractFilesEx** method of the [**Merge**](merge-object.md) object extracts the embedded .cab file from a module and then writes those files to the destination directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b968-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3b968-105">Syntax</span></span>


```JScript
Merge.ExtractFilesEx(
  Path,
  fLongFileNames,
  pFilePaths
)
```



## <a name="parameters"></a><span data-ttu-id="3b968-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3b968-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b968-107">*Percorso*</span><span class="sxs-lookup"><span data-stu-id="3b968-107">*Path*</span></span> 
</dt> <dd>

<span data-ttu-id="3b968-108">Directory di destinazione completo.</span><span class="sxs-lookup"><span data-stu-id="3b968-108">The fully qualified destination directory.</span></span>

</dd> <dt>

<span data-ttu-id="3b968-109">*fLongFileNames*</span><span class="sxs-lookup"><span data-stu-id="3b968-109">*fLongFileNames*</span></span> 
</dt> <dd>

<span data-ttu-id="3b968-110">Impostare questa impostazione per specificare l'utilizzo di nomi di file lunghi per i segmenti di percorso e i nomi file finali.</span><span class="sxs-lookup"><span data-stu-id="3b968-110">Set to specify using long file names for path segments and final file names.</span></span>

</dd> <dt>

<span data-ttu-id="3b968-111">*pFilePaths*</span><span class="sxs-lookup"><span data-stu-id="3b968-111">*pFilePaths*</span></span> 
</dt> <dd>

<span data-ttu-id="3b968-112">Si tratta di un elenco di percorsi completi per i file estratti correttamente.</span><span class="sxs-lookup"><span data-stu-id="3b968-112">This is a list of fully qualified paths for the files that were successfully extracted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b968-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3b968-113">Return value</span></span>

<span data-ttu-id="3b968-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="3b968-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b968-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="3b968-115">Remarks</span></span>

<span data-ttu-id="3b968-116">Tutti i file nella directory di destinazione con lo stesso nome verranno sovrascritti.</span><span class="sxs-lookup"><span data-stu-id="3b968-116">Any files in the destination directory with the same name are overwritten.</span></span> <span data-ttu-id="3b968-117">Il percorso viene creato se non esiste già.</span><span class="sxs-lookup"><span data-stu-id="3b968-117">The path is created if it does not already exist.</span></span>

### <a name="c"></a><span data-ttu-id="3b968-118">C++</span><span class="sxs-lookup"><span data-stu-id="3b968-118">C++</span></span>

<span data-ttu-id="3b968-119">Vedere funzione [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) .</span><span class="sxs-lookup"><span data-stu-id="3b968-119">See [**ExtractFilesEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-extractfilesex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b968-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3b968-120">Requirements</span></span>



| <span data-ttu-id="3b968-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b968-121">Requirement</span></span> | <span data-ttu-id="3b968-122">Valore</span><span class="sxs-lookup"><span data-stu-id="3b968-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3b968-123">Versione</span><span class="sxs-lookup"><span data-stu-id="3b968-123">Version</span></span><br/> | <span data-ttu-id="3b968-124">Mergemod.dll 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="3b968-124">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="3b968-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3b968-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3b968-126"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b968-126"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="3b968-127">DLL</span><span class="sxs-lookup"><span data-stu-id="3b968-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="3b968-128"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b968-128"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




