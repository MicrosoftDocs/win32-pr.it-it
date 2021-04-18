---
description: Il metodo ApriModulo dell'oggetto merge apre un modulo Windows Installer Merge in modalità di sola lettura. Prima di poter eseguire il merge di un modulo con un database di installazione, è necessario aprirlo.
ms.assetid: fc976899-2c39-4314-b2fb-417e0dfc53b9
title: Metodo merge. ApriModulo (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenModule
- IMsmMerge.OpenModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 9d83a9331c91817f70c49ecf74c7171c5e627be6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333976"
---
# <a name="mergeopenmodule-method"></a><span data-ttu-id="c2a3e-104">Merge. ApriModulo, metodo</span><span class="sxs-lookup"><span data-stu-id="c2a3e-104">Merge.OpenModule method</span></span>

<span data-ttu-id="c2a3e-105">Il metodo **ApriModulo** dell'oggetto [**merge**](merge-object.md) apre un modulo Windows Installer Merge in modalità di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c2a3e-105">The **OpenModule** method of the [**Merge**](merge-object.md) object opens a Windows Installer merge module in read-only mode.</span></span> <span data-ttu-id="c2a3e-106">Prima di poter eseguire il merge di un modulo con un database di installazione, è necessario aprirlo.</span><span class="sxs-lookup"><span data-stu-id="c2a3e-106">A module must be opened before it can be merged with an installation database.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a3e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2a3e-107">Syntax</span></span>


```JScript
Merge.OpenModule(
  FileName,
  Language
)
```



## <a name="parameters"></a><span data-ttu-id="c2a3e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2a3e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2a3e-109">*FileName*</span><span class="sxs-lookup"><span data-stu-id="c2a3e-109">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a3e-110">Nome file completo che punta a un modulo merge.</span><span class="sxs-lookup"><span data-stu-id="c2a3e-110">Fully qualified file name pointing to a merge module.</span></span>

</dd> <dt>

<span data-ttu-id="c2a3e-111">*Lingua*</span><span class="sxs-lookup"><span data-stu-id="c2a3e-111">*Language*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a3e-112">Identificatore di lingua valido (LANGID).</span><span class="sxs-lookup"><span data-stu-id="c2a3e-112">A valid language identifier (LANGID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2a3e-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2a3e-113">Return value</span></span>

<span data-ttu-id="c2a3e-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c2a3e-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2a3e-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c2a3e-115">Remarks</span></span>

<span data-ttu-id="c2a3e-116">Questa funzione apre il modulo merge in modalità di sola lettura ed esclude altri programmi da scrivere nel modulo merge fino a quando non viene chiamato il metodo [**CloseModule**](merge-closemodule.md) .</span><span class="sxs-lookup"><span data-stu-id="c2a3e-116">This function opens the merge module in read-only mode and excludes other programs from writing to the merge module until the [**CloseModule**](merge-closemodule.md) method is called.</span></span>

<span data-ttu-id="c2a3e-117">Il programma di installazione tenta di aprire il modulo nella lingua specificata dalla *lingua* o in una lingua più generale.</span><span class="sxs-lookup"><span data-stu-id="c2a3e-117">The installer attempts to open the module in the language specified by *Language*, or a more general language.</span></span> <span data-ttu-id="c2a3e-118">Se, ad esempio, il *linguaggio* viene specificato come 1033, nella lingua predefinita è possibile aprire un modulo con la lingua predefinita 1033, 9 o 0.</span><span class="sxs-lookup"><span data-stu-id="c2a3e-118">For example, if *Language* is specified as 1033, a module with a default language of 1033, 9, or 0 can be opened in its default language.</span></span> <span data-ttu-id="c2a3e-119">Un valore di *lingua* 9 apre i moduli con la lingua predefinita 9 o 0.</span><span class="sxs-lookup"><span data-stu-id="c2a3e-119">A *Language* value of 9 opens modules with a default language of 9 or 0.</span></span> <span data-ttu-id="c2a3e-120">Se la lingua predefinita del modulo non soddisfa i requisiti specificati, viene effettuato un tentativo di trasformare il modulo nella lingua richiesta.</span><span class="sxs-lookup"><span data-stu-id="c2a3e-120">If the default language of the module does not meet the specified requirements, an attempt is made to transform the module to the requested language.</span></span> <span data-ttu-id="c2a3e-121">Se l'operazione ha esito negativo, il modulo viene trasformato in linguaggi sempre più generali, fino alla lingua neutra.</span><span class="sxs-lookup"><span data-stu-id="c2a3e-121">If that fails, the module is transformed to increasingly general languages, all the way to language neutral.</span></span> <span data-ttu-id="c2a3e-122">Se nessuna delle trasformazioni ha esito positivo, non è possibile aprire il modulo.</span><span class="sxs-lookup"><span data-stu-id="c2a3e-122">If none of the transforms succeed, the module fails to open.</span></span> <span data-ttu-id="c2a3e-123">In questo caso, viene aggiunto un errore all'elenco errori di tipo msmErrorLanguageUnsupported.</span><span class="sxs-lookup"><span data-stu-id="c2a3e-123">In this case, an error is added to the error list of type msmErrorLanguageUnsupported.</span></span> <span data-ttu-id="c2a3e-124">Se si verifica un errore durante la trasformazione del modulo nella lingua desiderata, viene aggiunto un errore all'elenco errori di tipo msmErrorLanguageFailed.</span><span class="sxs-lookup"><span data-stu-id="c2a3e-124">If there is an error transforming the module to the desired language, an error is added to the error list of type msmErrorLanguageFailed.</span></span> <span data-ttu-id="c2a3e-125">Per informazioni dettagliate, vedere la proprietà [**Type**](error-type.md) dell'oggetto [**Error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c2a3e-125">For details, see the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span> <span data-ttu-id="c2a3e-126">L'apertura di un modulo merge Cancella tutti gli errori che non sono stati ancora recuperati.</span><span class="sxs-lookup"><span data-stu-id="c2a3e-126">Opening a merge module clears any errors that have not already been retrieved.</span></span>

### <a name="c"></a><span data-ttu-id="c2a3e-127">C++</span><span class="sxs-lookup"><span data-stu-id="c2a3e-127">C++</span></span>

<span data-ttu-id="c2a3e-128">Vedere funzione [**ApriModulo**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) .</span><span class="sxs-lookup"><span data-stu-id="c2a3e-128">See [**OpenModule**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openmodule) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a3e-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2a3e-129">Requirements</span></span>



| <span data-ttu-id="c2a3e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2a3e-130">Requirement</span></span> | <span data-ttu-id="c2a3e-131">Valore</span><span class="sxs-lookup"><span data-stu-id="c2a3e-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a3e-132">Versione</span><span class="sxs-lookup"><span data-stu-id="c2a3e-132">Version</span></span><br/> | <span data-ttu-id="c2a3e-133">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="c2a3e-133">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="c2a3e-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2a3e-134">Header</span></span><br/>  | <dl> <span data-ttu-id="c2a3e-135"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a3e-135"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2a3e-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c2a3e-136">DLL</span></span><br/>     | <dl> <span data-ttu-id="c2a3e-137"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2a3e-137"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
