---
description: Il Metodo Sequence dell'oggetto Session apre una query sulla tabella specificata, ordinando le azioni in base ai numeri nella colonna Sequence.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Metodo Session. Sequence
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Sequence
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18708b79bdce73b29f46b4d62a15ceb8003d9c9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333039"
---
# <a name="sessionsequence-method"></a><span data-ttu-id="7f04a-103">Metodo Session. Sequence</span><span class="sxs-lookup"><span data-stu-id="7f04a-103">Session.Sequence method</span></span>

<span data-ttu-id="7f04a-104">Il metodo **Sequence** dell'oggetto [**Session**](session-object.md) apre una query sulla tabella specificata, ordinando le azioni in base ai numeri nella colonna Sequence.</span><span class="sxs-lookup"><span data-stu-id="7f04a-104">The **Sequence** method of the [**Session**](session-object.md) object opens a query on the specified table, ordering the actions by the numbers in the Sequence column.</span></span> <span data-ttu-id="7f04a-105">Per ogni riga recuperata, viene chiamato il metodo [**DoAction**](session-doaction.md) , purché le espressioni di condizione fornite non restituiscono false.</span><span class="sxs-lookup"><span data-stu-id="7f04a-105">For each row fetched, the [**DoAction**](session-doaction.md) method is called, provided that any supplied condition expression does not evaluate to False.</span></span> <span data-ttu-id="7f04a-106">Restituisce un msiDoActionStatusEnum di enumerazione, come descritto nel metodo [**DoAction**](session-doaction.md) .</span><span class="sxs-lookup"><span data-stu-id="7f04a-106">Returns an enumeration msiDoActionStatusEnum, as described in the [**DoAction**](session-doaction.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f04a-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7f04a-107">Syntax</span></span>


```JScript
Session.Sequence(
  table
)
```



## <a name="parameters"></a><span data-ttu-id="7f04a-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7f04a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f04a-109">*tabella*</span><span class="sxs-lookup"><span data-stu-id="7f04a-109">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="7f04a-110">Nome stringa obbligatorio della tabella da utilizzare per la sequenziazione.</span><span class="sxs-lookup"><span data-stu-id="7f04a-110">Required string name of the table to use for sequencing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f04a-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7f04a-111">Return value</span></span>

<span data-ttu-id="7f04a-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="7f04a-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7f04a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="7f04a-113">Remarks</span></span>

<span data-ttu-id="7f04a-114">Questo metodo in genere viene chiamato internamente dalle azioni di primo livello.</span><span class="sxs-lookup"><span data-stu-id="7f04a-114">This method is normally called internally by top-level actions.</span></span>

<span data-ttu-id="7f04a-115">Una sequenza di azione che contiene azioni che aggiornano il sistema, ad esempio le azioni [InstallFiles](installfiles-action.md) e [WriteRegistryValori consente](writeregistryvalues-action.md) , non può essere eseguita chiamando il metodo **Sequence** .</span><span class="sxs-lookup"><span data-stu-id="7f04a-115">An action sequence containing actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **Sequence** method.</span></span> <span data-ttu-id="7f04a-116">L'eccezione a questa regola è rappresentata dal caso in cui il metodo **Sequence** venga chiamato da un'azione personalizzata pianificata nella [tabella InstallExecuteSequence](installexecutesequence-table.md) tra le azioni [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="7f04a-116">The exception to this rule is if the **Sequence** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="7f04a-117">È possibile chiamare le azioni che non aggiornano il sistema, ad esempio [AppSearch](appsearch-action.md) o [CostInitialize](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="7f04a-117">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f04a-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7f04a-118">Requirements</span></span>



| <span data-ttu-id="7f04a-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f04a-119">Requirement</span></span> | <span data-ttu-id="7f04a-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7f04a-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f04a-121">Versione</span><span class="sxs-lookup"><span data-stu-id="7f04a-121">Version</span></span><br/> | <span data-ttu-id="7f04a-122">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7f04a-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7f04a-123">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7f04a-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7f04a-124">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="7f04a-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="7f04a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="7f04a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="7f04a-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f04a-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="7f04a-127">IID</span><span class="sxs-lookup"><span data-stu-id="7f04a-127">IID</span></span><br/>     | <span data-ttu-id="7f04a-128">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7f04a-128">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




