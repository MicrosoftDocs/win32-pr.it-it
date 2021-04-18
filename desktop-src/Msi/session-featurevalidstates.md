---
description: La proprietà FeatureValidStates dell'oggetto Session restituisce un Integer che rappresenta i flag di bit con ogni bit pertinente che rappresenta uno stato di installazione valido per la funzionalità specificata.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Proprietà Session. FeatureValidStates
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureValidStates
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b76080bb7854c75cbfbb06697de9fc7d7a1af0c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330775"
---
# <a name="sessionfeaturevalidstates-property"></a><span data-ttu-id="c6830-103">Proprietà Session. FeatureValidStates</span><span class="sxs-lookup"><span data-stu-id="c6830-103">Session.FeatureValidStates property</span></span>

<span data-ttu-id="c6830-104">La proprietà **FeatureValidStates** dell'oggetto [**Session**](session-object.md) restituisce un Integer che rappresenta i flag di bit con ogni bit pertinente che rappresenta uno stato di installazione valido per la funzionalità specificata.</span><span class="sxs-lookup"><span data-stu-id="c6830-104">The **FeatureValidStates** property of the [**Session**](session-object.md) object returns an integer representing bit flags with each relevant bit representing a valid installation state for the specified feature.</span></span>

<span data-ttu-id="c6830-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="c6830-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c6830-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c6830-106">Syntax</span></span>


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a><span data-ttu-id="c6830-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="c6830-107">Property value</span></span>

<span data-ttu-id="c6830-108">Nome di stringa obbligatorio dell'elemento della funzionalità di cui devono essere recuperati gli Stati di installazione validi.</span><span class="sxs-lookup"><span data-stu-id="c6830-108">Required string name of the feature item whose valid installation states are to be retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="c6830-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="c6830-109">Remarks</span></span>

<span data-ttu-id="c6830-110">Il valore restituito è costituito da flag di bit, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="c6830-110">The return value is composed of bit flags as follows.</span></span> <span data-ttu-id="c6830-111">Bit 0: se impostato, local è uno stato valido.</span><span class="sxs-lookup"><span data-stu-id="c6830-111">Bit 0: if set, Local is a valid state.</span></span> <span data-ttu-id="c6830-112">Bit 1: se impostato, l'origine è uno stato valido.</span><span class="sxs-lookup"><span data-stu-id="c6830-112">Bit 1: if set, Source is a valid state.</span></span>

<span data-ttu-id="c6830-113">La proprietà **FeatureValidStates** ha esito positivo solo dopo che il programma di installazione ha chiamato le azioni [CostInitialize](costinitialize-action.md) e [CostFinalize secondo](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="c6830-113">The **FeatureValidStates** property only succeeds after the installer has called the [CostInitialize](costinitialize-action.md) and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="c6830-114">**FeatureValidStates** determina la validità dello stato eseguendo una query su tutti i componenti collegati alla funzionalità specificata senza considerare lo stato di installazione corrente di un componente.</span><span class="sxs-lookup"><span data-stu-id="c6830-114">**FeatureValidStates** determines state validity by querying all components that are linked to the specified feature without taking into account the current installed state of any component.</span></span>

<span data-ttu-id="c6830-115">I possibili stati validi per una funzionalità sono determinati come segue:</span><span class="sxs-lookup"><span data-stu-id="c6830-115">The possible valid states for a feature are determined as follows:</span></span>

-   <span data-ttu-id="c6830-116">Se la funzionalità non contiene componenti, sia \_ l'origine InstallState locale che quella InstallState \_ sono stati validi per la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c6830-116">If the feature does not contain components, both INSTALLSTATE\_LOCAL and INSTALLSTATE\_SOURCE are valid states for the feature.</span></span>
-   <span data-ttu-id="c6830-117">Se almeno un componente della funzionalità dispone di un attributo di msidbComponentAttributesLocalOnly o msidbComponentAttributesOptional, INSTALLSTATE \_ local è uno stato valido per la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c6830-117">If at least one component of the feature has an attribute of msidbComponentAttributesLocalOnly or msidbComponentAttributesOptional, INSTALLSTATE\_LOCAL is a valid state for the feature.</span></span>
-   <span data-ttu-id="c6830-118">Se almeno un componente della funzionalità dispone di un attributo di msidbComponentAttributesSourceOnly o msidbComponentAttributesOptional, INSTALLSTATE \_ source è uno stato valido per la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c6830-118">If at least one component of the feature has an attribute of msidbComponentAttributesSourceOnly or msidbComponentAttributesOptional, INSTALLSTATE\_SOURCE is a valid state for the feature.</span></span>
-   <span data-ttu-id="c6830-119">Se un file di un componente appartenente alla funzionalità viene patchato o da un'origine compressa, \_ l'origine InstallState non è inclusa come stato valido per la funzionalità.</span><span class="sxs-lookup"><span data-stu-id="c6830-119">If a file of a component belonging to the feature is patched or from a compressed source, then INSTALLSTATE\_SOURCE is not included as a valid state for the feature.</span></span>
-   <span data-ttu-id="c6830-120">L'annuncio INSTALLSTATE \_ non è uno stato valido se la funzionalità non consente l'annuncio (msidbFeatureAttributesDisallowAdvertise) o se la funzionalità richiede il supporto della piattaforma per gli annunci (msidbFeatureAttributesNoUnsupportedAdvertise) e la piattaforma non la supporta.</span><span class="sxs-lookup"><span data-stu-id="c6830-120">INSTALLSTATE\_ADVERTISE is not a valid state if the feature disallows advertisement (msidbFeatureAttributesDisallowAdvertise) or the feature requires platform support for advertisement (msidbFeatureAttributesNoUnsupportedAdvertise) and the platform does not support it.</span></span>
-   <span data-ttu-id="c6830-121">INSTALLSTATE \_ assente è uno stato valido per la funzionalità se gli attributi non includono msidbFeatureAttributesUIDisallowAbsent.</span><span class="sxs-lookup"><span data-stu-id="c6830-121">INSTALLSTATE\_ABSENT is a valid state for the feature if its attributes do not include msidbFeatureAttributesUIDisallowAbsent.</span></span>
-   <span data-ttu-id="c6830-122">Gli stati validi per le funzionalità figlio contrassegnate per seguire la funzionalità padre (msidbFeatureAttributesFollowParent) si basano sull'azione o sullo stato di installazione della funzionalità padre.</span><span class="sxs-lookup"><span data-stu-id="c6830-122">Valid states for child features marked to follow the parent feature (msidbFeatureAttributesFollowParent) are based upon the parent feature's action or installed state.</span></span>

<span data-ttu-id="c6830-123">Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="c6830-123">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6830-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c6830-124">Requirements</span></span>



| <span data-ttu-id="c6830-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6830-125">Requirement</span></span> | <span data-ttu-id="c6830-126">Valore</span><span class="sxs-lookup"><span data-stu-id="c6830-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6830-127">Versione</span><span class="sxs-lookup"><span data-stu-id="c6830-127">Version</span></span><br/> | <span data-ttu-id="c6830-128">Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c6830-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c6830-129">Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c6830-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c6830-130">Windows Installer in Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="c6830-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="c6830-131">DLL</span><span class="sxs-lookup"><span data-stu-id="c6830-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="c6830-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6830-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="c6830-133">IID</span><span class="sxs-lookup"><span data-stu-id="c6830-133">IID</span></span><br/>     | <span data-ttu-id="c6830-134">IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="c6830-134">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




