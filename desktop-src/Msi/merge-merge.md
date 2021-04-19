---
description: Il metodo Merge dell'oggetto merge esegue un'Unione del database corrente e del modulo corrente.
ms.assetid: 4b580b1f-5071-42f1-8022-a152817f9fdc
title: Metodo merge. Merge (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.Merge
- IMsmMerge.Merge
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: f33a0ba8218ae38d8fb31cefb6910f5b2c16484d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332261"
---
# <a name="mergemerge-method"></a><span data-ttu-id="8809a-103">Merge. Merge (metodo)</span><span class="sxs-lookup"><span data-stu-id="8809a-103">Merge.Merge method</span></span>

<span data-ttu-id="8809a-104">Il metodo **merge** dell'oggetto [**merge**](merge-object.md) esegue un'Unione del database corrente e del modulo corrente.</span><span class="sxs-lookup"><span data-stu-id="8809a-104">The **Merge** method of the [**Merge**](merge-object.md) object executes a merge of the current database and current module.</span></span> <span data-ttu-id="8809a-105">Il merge collega i componenti del modulo alla funzionalità identificata dalla *funzionalità*.</span><span class="sxs-lookup"><span data-stu-id="8809a-105">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="8809a-106">La radice dell'albero di directory del modulo viene reindirizzata alla posizione specificata da *RedirectDir*.</span><span class="sxs-lookup"><span data-stu-id="8809a-106">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

<span data-ttu-id="8809a-107">Il metodo **merge** può essere chiamato una sola volta per unire una determinata combinazione di file con estensione msi e MSM.</span><span class="sxs-lookup"><span data-stu-id="8809a-107">The **Merge** method can only be called once to merge a particular combination of .msi and .msm files.</span></span>

## <a name="syntax"></a><span data-ttu-id="8809a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8809a-108">Syntax</span></span>


```JScript
Merge.Merge(
  Feature,
  RedirectDir
)
```



## <a name="parameters"></a><span data-ttu-id="8809a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8809a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8809a-110">*Funzionalità*</span><span class="sxs-lookup"><span data-stu-id="8809a-110">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="8809a-111">Nome di una funzionalità nel database.</span><span class="sxs-lookup"><span data-stu-id="8809a-111">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="8809a-112">*RedirectDir*</span><span class="sxs-lookup"><span data-stu-id="8809a-112">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="8809a-113">Chiave di una voce nella tabella di [directory](directory-table.md) del database.</span><span class="sxs-lookup"><span data-stu-id="8809a-113">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="8809a-114">Questo parametro può essere null o una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="8809a-114">This parameter may be null or an empty string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8809a-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8809a-115">Return value</span></span>

<span data-ttu-id="8809a-116">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="8809a-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8809a-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="8809a-117">Remarks</span></span>

<span data-ttu-id="8809a-118">Una volta completata l'Unione, i componenti del modulo vengono collegati alla funzionalità identificata dalla *funzionalità*.</span><span class="sxs-lookup"><span data-stu-id="8809a-118">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="8809a-119">Questa funzionalità non è stata creata e deve essere una funzionalità esistente.</span><span class="sxs-lookup"><span data-stu-id="8809a-119">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="8809a-120">Si noti che il metodo **merge** ottiene tutti i riferimenti alle funzionalità nel modulo e sostituisce il riferimento alla funzionalità per tutte le occorrenze del GUID null nel database del modulo.</span><span class="sxs-lookup"><span data-stu-id="8809a-120">Note that the **Merge** method gets all the feature references in the module and substitutes the feature reference for all occurrences of the null GUID in the module database.</span></span> <span data-ttu-id="8809a-121">Per altre informazioni, vedere [riferimento alle funzionalità nei moduli merge](referencing-features-in-merge-modules.md).</span><span class="sxs-lookup"><span data-stu-id="8809a-121">For more information, see [Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).</span></span>

<span data-ttu-id="8809a-122">Il modulo può essere collegato a funzionalità aggiuntive usando il metodo [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="8809a-122">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span> <span data-ttu-id="8809a-123">Si noti che la chiamata al metodo **Connect** crea solo associazioni di componenti di funzionalità.</span><span class="sxs-lookup"><span data-stu-id="8809a-123">Note that calling the **Connect** method only creates feature-component associations.</span></span> <span data-ttu-id="8809a-124">Non modifica le righe che sono già state unite nel database.</span><span class="sxs-lookup"><span data-stu-id="8809a-124">It does not modify the rows that have already been merged in to the database.</span></span>

<span data-ttu-id="8809a-125">Le modifiche apportate al database vengono salvate solo se viene chiamato il metodo [**ChiudiDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) con *BCommit* impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="8809a-125">Changes made to the database are saved if and only if the [**CloseDatabase**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-closedatabase) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="8809a-126">Se si verificano conflitti di merge, incluse le esclusioni, vengono inseriti nell'enumeratore Error per il recupero successivo, ma non determina l'esito negativo dell'operazione di merge.</span><span class="sxs-lookup"><span data-stu-id="8809a-126">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="8809a-127">Gli errori possono essere recuperati tramite la proprietà [**Errors**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="8809a-127">Errors may be retrieved through the [**Errors**](error-object.md) property.</span></span> <span data-ttu-id="8809a-128">Gli errori e i messaggi informativi vengono inseriti nel file di log corrente.</span><span class="sxs-lookup"><span data-stu-id="8809a-128">Errors and informational messages are posted to the current log file.</span></span>

### <a name="c"></a><span data-ttu-id="8809a-129">C++</span><span class="sxs-lookup"><span data-stu-id="8809a-129">C++</span></span>

<span data-ttu-id="8809a-130">Vedere funzione [**merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) .</span><span class="sxs-lookup"><span data-stu-id="8809a-130">See [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="8809a-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8809a-131">Requirements</span></span>



| <span data-ttu-id="8809a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="8809a-132">Requirement</span></span> | <span data-ttu-id="8809a-133">Valore</span><span class="sxs-lookup"><span data-stu-id="8809a-133">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8809a-134">Versione</span><span class="sxs-lookup"><span data-stu-id="8809a-134">Version</span></span><br/> | <span data-ttu-id="8809a-135">Mergemod.dll 1,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="8809a-135">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="8809a-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8809a-136">Header</span></span><br/>  | <dl> <span data-ttu-id="8809a-137"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="8809a-137"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="8809a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="8809a-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="8809a-139"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8809a-139"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
