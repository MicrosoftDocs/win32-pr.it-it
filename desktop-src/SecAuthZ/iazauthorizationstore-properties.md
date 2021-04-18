---
description: L'interfaccia IAzAuthorizationStore espone le proprietà seguenti.
ms.assetid: FAA581E5-98F4-48DD-9B21-911896AE5A31
title: Proprietà di IAzAuthorizationStore
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ecd324ce31397007ac8e665df37d2308217673e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316191"
---
# <a name="iazauthorizationstore-properties"></a><span data-ttu-id="9bd9e-103">Proprietà di IAzAuthorizationStore</span><span class="sxs-lookup"><span data-stu-id="9bd9e-103">IAzAuthorizationStore Properties</span></span>

<span data-ttu-id="9bd9e-104">L'interfaccia [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) espone le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="9bd9e-104">The [**IAzAuthorizationStore**](/windows/desktop/api/Azroles/nn-azroles-iazauthorizationstore) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9bd9e-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="9bd9e-105">In this section</span></span>

-   [<span data-ttu-id="9bd9e-106">**Proprietà ApplicationData**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-106">**ApplicationData Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_applicationdata)
-   [<span data-ttu-id="9bd9e-107">**Proprietà ApplicationGroups**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-107">**ApplicationGroups Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_applicationgroups)
-   [<span data-ttu-id="9bd9e-108">**Proprietà Applications**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-108">**Applications Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_applications)
-   [<span data-ttu-id="9bd9e-109">**Proprietà ApplyStoreSacl**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-109">**ApplyStoreSacl Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_applystoresacl)
-   [<span data-ttu-id="9bd9e-110">**Proprietà DelegatedPolicyUsers**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-110">**DelegatedPolicyUsers Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_delegatedpolicyusers)
-   [<span data-ttu-id="9bd9e-111">**Proprietà DelegatedPolicyUsersName**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-111">**DelegatedPolicyUsersName Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_delegatedpolicyusersname)
-   [<span data-ttu-id="9bd9e-112">**Proprietà Description**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-112">**Description Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_description)
-   [<span data-ttu-id="9bd9e-113">**Proprietà DomainTimeout**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-113">**DomainTimeout Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_domaintimeout)
-   [<span data-ttu-id="9bd9e-114">**Proprietà GenerateAudits**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-114">**GenerateAudits Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_generateaudits)
-   [<span data-ttu-id="9bd9e-115">**Proprietà MaxScriptEngines**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-115">**MaxScriptEngines Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_maxscriptengines)
-   [<span data-ttu-id="9bd9e-116">**Proprietà PolicyAdministrators**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-116">**PolicyAdministrators Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_policyadministrators)
-   [<span data-ttu-id="9bd9e-117">**Proprietà PolicyAdministratorsName**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-117">**PolicyAdministratorsName Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_policyadministratorsname)
-   [<span data-ttu-id="9bd9e-118">**Proprietà PolicyReaders**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-118">**PolicyReaders Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_policyreaders)
-   [<span data-ttu-id="9bd9e-119">**Proprietà PolicyReadersName**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-119">**PolicyReadersName Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_policyreadersname)
-   [<span data-ttu-id="9bd9e-120">**Proprietà ScriptEngineTimeout**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-120">**ScriptEngineTimeout Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_scriptenginetimeout)
-   [<span data-ttu-id="9bd9e-121">**Proprietà TargetMachine**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-121">**TargetMachine Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_targetmachine)
-   [<span data-ttu-id="9bd9e-122">**Proprietà scrivibile**</span><span class="sxs-lookup"><span data-stu-id="9bd9e-122">**Writable Property**</span></span>](/windows/desktop/api/Azroles/nf-azroles-iazauthorizationstore-get_writable)

 

 



