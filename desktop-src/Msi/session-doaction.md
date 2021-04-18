---
description: Il metodo DoAction dell'oggetto Session esegue la funzione Action corrispondente al nome fornito.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Metodo Session. DoAction (fotoacquire. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3084cfd51e7efbcfbfbc3cbcf2c9be21d8373d21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329108"
---
# <a name="sessiondoaction-method"></a><span data-ttu-id="d156a-103">Session. DoAction, metodo</span><span class="sxs-lookup"><span data-stu-id="d156a-103">Session.DoAction method</span></span>

<span data-ttu-id="d156a-104">Il metodo **DoAction** dell'oggetto [**Session**](session-object.md) esegue la funzione Action corrispondente al nome fornito.</span><span class="sxs-lookup"><span data-stu-id="d156a-104">The **DoAction** method of the [**Session**](session-object.md) object executes the action function corresponding to the name supplied.</span></span> <span data-ttu-id="d156a-105">Se viene fornito un nome di azione null, il motore utilizzerà il valore in maiuscolo della [proprietà Action](action.md) come azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="d156a-105">If a Null action name is supplied, the engine uses the uppercase value of the [ACTION property](action.md) as the action to perform.</span></span> <span data-ttu-id="d156a-106">Se non viene definito alcun valore della proprietà, viene eseguita l'azione predefinita, attualmente definita come INSTALL.</span><span class="sxs-lookup"><span data-stu-id="d156a-106">If no property value is defined, the default action is performed, currently defined as INSTALL.</span></span> <span data-ttu-id="d156a-107">Questo metodo restituisce un'enumerazione Integer.</span><span class="sxs-lookup"><span data-stu-id="d156a-107">This method returns an integer enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="d156a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d156a-108">Syntax</span></span>


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a><span data-ttu-id="d156a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="d156a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d156a-110">*action*</span><span class="sxs-lookup"><span data-stu-id="d156a-110">*action*</span></span> 
</dt> <dd>

<span data-ttu-id="d156a-111">Nome stringa obbligatorio dell'azione da eseguire.</span><span class="sxs-lookup"><span data-stu-id="d156a-111">Required string name of the action to execute.</span></span> <span data-ttu-id="d156a-112">Distinzione tra maiuscole e minuscole.</span><span class="sxs-lookup"><span data-stu-id="d156a-112">Case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d156a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d156a-113">Return value</span></span>

<span data-ttu-id="d156a-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="d156a-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d156a-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="d156a-115">Remarks</span></span>

<span data-ttu-id="d156a-116">Le azioni che aggiornano il sistema, ad esempio le azioni [InstallFiles](installfiles-action.md) e [WriteRegistryValori consente](writeregistryvalues-action.md) , non possono essere eseguite chiamando il metodo **DoAction** .</span><span class="sxs-lookup"><span data-stu-id="d156a-116">Actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **DoAction** method.</span></span> <span data-ttu-id="d156a-117">L'eccezione a questa regola è rappresentata dal caso in cui il metodo **DoAction** viene chiamato da un'azione personalizzata pianificata nella [tabella InstallExecuteSequence](installexecutesequence-table.md) tra le azioni [InstallInitialize](installinitialize-action.md) e [InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="d156a-117">The exception to this rule is if the **DoAction** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="d156a-118">È possibile chiamare le azioni che non aggiornano il sistema, ad esempio [AppSearch](appsearch-action.md) o [CostInitialize](costinitialize-action.md).</span><span class="sxs-lookup"><span data-stu-id="d156a-118">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="d156a-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d156a-119">Requirements</span></span>



| <span data-ttu-id="d156a-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d156a-120">Requirement</span></span> | <span data-ttu-id="d156a-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d156a-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d156a-122">Versione</span><span class="sxs-lookup"><span data-stu-id="d156a-122">Version</span></span><br/> | <span data-ttu-id="d156a-123">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d156a-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d156a-124">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d156a-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d156a-125">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="d156a-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d156a-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d156a-126">Header</span></span><br/>  | <dl> <span data-ttu-id="d156a-127"><dt>Fotoacquisisci. h</dt></span><span class="sxs-lookup"><span data-stu-id="d156a-127"><dt>Photoacquire.h</dt></span></span> </dl>                                                                                                                                                               |
| <span data-ttu-id="d156a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d156a-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="d156a-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d156a-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d156a-130">IID</span><span class="sxs-lookup"><span data-stu-id="d156a-130">IID</span></span><br/>     | <span data-ttu-id="d156a-131">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d156a-131">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




