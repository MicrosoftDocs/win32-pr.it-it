---
description: Il metodo MergeEx dell'oggetto merge è equivalente alla funzione Merge, ad eccezione del fatto che accetta un argomento aggiuntivo.
ms.assetid: 83b6d62b-d176-42ac-b513-d1c2e562965c
title: Metodo merge. MergeEx (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.MergeEx
- IMsmMerge.MergeEx
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 12accfcbc87877300b803ae90d8c924802410e9f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326374"
---
# <a name="mergemergeex-method"></a><span data-ttu-id="bec13-103">Merge. MergeEx, metodo</span><span class="sxs-lookup"><span data-stu-id="bec13-103">Merge.MergeEx method</span></span>

<span data-ttu-id="bec13-104">Il metodo **MergeEx** dell'oggetto [**merge**](merge-object.md) è equivalente alla funzione [**merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) , ad eccezione del fatto che accetta un argomento aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="bec13-104">The **MergeEx** method of the [**Merge**](merge-object.md) object is equivalent to the [**Merge**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-merge) function, except that it takes an extra argument.</span></span> <span data-ttu-id="bec13-105">L'argomento *pConfiguration* è un'interfaccia implementata dal client.</span><span class="sxs-lookup"><span data-stu-id="bec13-105">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="bec13-106">L'argomento può essere null.</span><span class="sxs-lookup"><span data-stu-id="bec13-106">The argument may be null.</span></span> <span data-ttu-id="bec13-107">La presenza di questo argomento indica che il client è in grado di supportare la funzionalità di configurazione, ma non obbliga il client a fornire i dati di configurazione per un elemento configurabile specifico.</span><span class="sxs-lookup"><span data-stu-id="bec13-107">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

<span data-ttu-id="bec13-108">Il metodo [**merge**](merge-merge.md) esegue un'Unione del database corrente e del modulo corrente.</span><span class="sxs-lookup"><span data-stu-id="bec13-108">The [**Merge**](merge-merge.md) method executes a merge of the current database and current module.</span></span> <span data-ttu-id="bec13-109">Il merge collega i componenti del modulo alla funzionalità identificata dalla *funzionalità*.</span><span class="sxs-lookup"><span data-stu-id="bec13-109">The merge attaches the components in the module to the feature identified by *Feature*.</span></span> <span data-ttu-id="bec13-110">La radice dell'albero di directory del modulo viene reindirizzata alla posizione specificata da *RedirectDir*.</span><span class="sxs-lookup"><span data-stu-id="bec13-110">The root of the module's directory tree is redirected to the location given by *RedirectDir*.</span></span>

## <a name="syntax"></a><span data-ttu-id="bec13-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bec13-111">Syntax</span></span>


```JScript
Merge.MergeEx(
  Feature,
  RedirectDir,
  pConfiguration
)
```



## <a name="parameters"></a><span data-ttu-id="bec13-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="bec13-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bec13-113">*Funzionalità*</span><span class="sxs-lookup"><span data-stu-id="bec13-113">*Feature*</span></span> 
</dt> <dd>

<span data-ttu-id="bec13-114">Nome di una funzionalità nel database.</span><span class="sxs-lookup"><span data-stu-id="bec13-114">The name of a feature in the database.</span></span>

</dd> <dt>

<span data-ttu-id="bec13-115">*RedirectDir*</span><span class="sxs-lookup"><span data-stu-id="bec13-115">*RedirectDir*</span></span> 
</dt> <dd>

<span data-ttu-id="bec13-116">Chiave di una voce nella tabella di [directory](directory-table.md) del database.</span><span class="sxs-lookup"><span data-stu-id="bec13-116">The key of an entry in the [Directory table](directory-table.md) of the database.</span></span> <span data-ttu-id="bec13-117">Questo parametro può essere null o una stringa vuota.</span><span class="sxs-lookup"><span data-stu-id="bec13-117">This parameter may be null or an empty string.</span></span>

</dd> <dt>

<span data-ttu-id="bec13-118">*pConfiguration*</span><span class="sxs-lookup"><span data-stu-id="bec13-118">*pConfiguration*</span></span> 
</dt> <dd>

<span data-ttu-id="bec13-119">L'argomento *pConfiguration* è un'interfaccia implementata dal client.</span><span class="sxs-lookup"><span data-stu-id="bec13-119">The *pConfiguration* argument is an interface implemented by the client.</span></span> <span data-ttu-id="bec13-120">L'argomento può essere null.</span><span class="sxs-lookup"><span data-stu-id="bec13-120">The argument may be null.</span></span> <span data-ttu-id="bec13-121">La presenza di questo argomento indica che il client è in grado di supportare la funzionalità di configurazione, ma non obbliga il client a fornire i dati di configurazione per un elemento configurabile specifico.</span><span class="sxs-lookup"><span data-stu-id="bec13-121">The presence of this argument indicates that the client is capable of supporting the configuration functionality, but does not obligate the client to provide configuration data for any specific configurable item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bec13-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bec13-122">Return value</span></span>

<span data-ttu-id="bec13-123">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="bec13-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bec13-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="bec13-124">Remarks</span></span>

<span data-ttu-id="bec13-125">Una volta completata l'Unione, i componenti del modulo vengono collegati alla funzionalità identificata dalla *funzionalità*.</span><span class="sxs-lookup"><span data-stu-id="bec13-125">Once the merge is complete, components in the module are attached to the feature identified by *Feature*.</span></span> <span data-ttu-id="bec13-126">Questa funzionalità non è stata creata e deve essere una funzionalità esistente.</span><span class="sxs-lookup"><span data-stu-id="bec13-126">This feature is not created and must be an existing feature.</span></span> <span data-ttu-id="bec13-127">Il modulo può essere collegato a funzionalità aggiuntive usando il metodo [**Connect**](merge-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="bec13-127">The module may be attached to additional features using the [**Connect**](merge-connect.md) method.</span></span>

<span data-ttu-id="bec13-128">Le modifiche apportate al database vengono salvate solo se viene chiamato il metodo [**ChiudiDatabase**](merge-closedatabase.md) con *BCommit* impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="bec13-128">Changes made to the database are saved if and only if the [**CloseDatabase**](merge-closedatabase.md) method is called with *bCommit* set to **TRUE**.</span></span>

<span data-ttu-id="bec13-129">Se si verificano conflitti di merge, incluse le esclusioni, vengono inseriti nell'enumeratore Error per il recupero successivo, ma non determina l'esito negativo dell'operazione di merge.</span><span class="sxs-lookup"><span data-stu-id="bec13-129">If any merge conflicts occur, including exclusions, they are placed in the error enumerator for later retrieval, but does not cause the merge to fail.</span></span> <span data-ttu-id="bec13-130">Gli errori possono essere recuperati tramite la proprietà [**Errors**](merge-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="bec13-130">Errors may be retrieved through the [**Errors**](merge-errors.md) property.</span></span> <span data-ttu-id="bec13-131">Gli errori e i messaggi informativi vengono inseriti nel file di log corrente.</span><span class="sxs-lookup"><span data-stu-id="bec13-131">Errors and informational messages are posted to the current log file.</span></span>

<span data-ttu-id="bec13-132">Quando l'Unione non riesce a causa di una configurazione errata del modulo, la funzione [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) restituisce E ha \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="bec13-132">When the merge fails because of an incorrect module configuration the [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function returns E\_FAIL.</span></span> <span data-ttu-id="bec13-133">Sono inclusi gli errori msmErrorType seguenti: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem** e **msmErrorDataRequestFailed**.</span><span class="sxs-lookup"><span data-stu-id="bec13-133">This includes these msmErrorType errors: **msmErrorBadNullSubstitution**, **msmErrorBadSubstitutionType**, **msmErrorBadNullResponse**, **msmErrorMissingConfigItem**, and **msmErrorDataRequestFailed**.</span></span> <span data-ttu-id="bec13-134">Questi errori comportano l'arresto immediato dell'Unione quando viene rilevato l'errore.</span><span class="sxs-lookup"><span data-stu-id="bec13-134">These errors cause the merge to stop immediately when the error is encountered.</span></span> <span data-ttu-id="bec13-135">L'oggetto Error viene ancora aggiunto all'enumeratore quando **MergeEx** restituisce E ha \_ esito negativo.</span><span class="sxs-lookup"><span data-stu-id="bec13-135">The error object is still added to the enumerator when **MergeEx** returns E\_FAIL.</span></span> <span data-ttu-id="bec13-136">Per ulteriori informazioni sugli errori msmErrorType, vedere [**get \_ Type function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).</span><span class="sxs-lookup"><span data-stu-id="bec13-136">For more information about msmErrorType errors, see [**get\_Type Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).</span></span> <span data-ttu-id="bec13-137">Tutti gli altri errori provocano la restituzione di false da parte di **MergeEx** \_ e la continuazione del merge.</span><span class="sxs-lookup"><span data-stu-id="bec13-137">All other errors cause **MergeEx** to return S\_FALSE and cause the merge to continue.</span></span>

### <a name="c"></a><span data-ttu-id="bec13-138">C++</span><span class="sxs-lookup"><span data-stu-id="bec13-138">C++</span></span>

<span data-ttu-id="bec13-139">Vedere funzione [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) .</span><span class="sxs-lookup"><span data-stu-id="bec13-139">See [**MergeEx**](/windows/desktop/api/Mergemod/nf-mergemod-imsmmerge2-mergeex) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bec13-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bec13-140">Requirements</span></span>



| <span data-ttu-id="bec13-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bec13-141">Requirement</span></span> | <span data-ttu-id="bec13-142">Valore</span><span class="sxs-lookup"><span data-stu-id="bec13-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bec13-143">Versione</span><span class="sxs-lookup"><span data-stu-id="bec13-143">Version</span></span><br/> | <span data-ttu-id="bec13-144">Mergemod.dll 2,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="bec13-144">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="bec13-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bec13-145">Header</span></span><br/>  | <dl> <span data-ttu-id="bec13-146"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="bec13-146"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="bec13-147">DLL</span><span class="sxs-lookup"><span data-stu-id="bec13-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="bec13-148"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bec13-148"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 
