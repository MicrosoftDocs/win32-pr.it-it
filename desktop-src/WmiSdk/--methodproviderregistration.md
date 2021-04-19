---
description: Registra i provider di metodi con WMI.
ms.assetid: c5a8ccd3-487e-42a3-bb31-d27da9a711c4
ms.tgt_platform: multiple
title: Classe __MethodProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __MethodProviderRegistration
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: dd59a88c9c0ff7b4b6726b58ce69f879eb3893ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317591"
---
# <a name="__methodproviderregistration-class"></a><span data-ttu-id="863a4-103">\_\_Classe MethodProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="863a4-103">\_\_MethodProviderRegistration class</span></span>

<span data-ttu-id="863a4-104">La classe di sistema **\_ \_ MethodProviderRegistration** registra i provider di metodi con WMI.</span><span class="sxs-lookup"><span data-stu-id="863a4-104">The **\_\_MethodProviderRegistration** system class registers method providers with WMI.</span></span>

<span data-ttu-id="863a4-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="863a4-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="863a4-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="863a4-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="863a4-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="863a4-107">Syntax</span></span>

``` syntax
class __MethodProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
};
```

## <a name="members"></a><span data-ttu-id="863a4-108">Members</span><span class="sxs-lookup"><span data-stu-id="863a4-108">Members</span></span>

<span data-ttu-id="863a4-109">La classe **\_ \_ MethodProviderRegistration** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="863a4-109">The **\_\_MethodProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="863a4-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="863a4-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="863a4-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="863a4-111">Properties</span></span>

<span data-ttu-id="863a4-112">La classe **\_ \_ MethodProviderRegistration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="863a4-112">The **\_\_MethodProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="863a4-113">**provider**</span><span class="sxs-lookup"><span data-stu-id="863a4-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="863a4-114">Tipo di dati: **\_ \_ provider**</span><span class="sxs-lookup"><span data-stu-id="863a4-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="863a4-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="863a4-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="863a4-116">Riferimento a un'istanza del [**\_ \_ provider**](--provider.md) che rappresenta il percorso dell'oggetto del provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="863a4-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the method provider.</span></span> <span data-ttu-id="863a4-117">Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="863a4-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="863a4-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="863a4-118">Remarks</span></span>

<span data-ttu-id="863a4-119">La classe **\_ \_ MethodProviderRegistration** deriva da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="863a4-119">The **\_\_MethodProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="863a4-120">Solo gli amministratori possono registrare o eliminare un provider di metodi creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e **\_ \_ MethodProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="863a4-120">Only administrators can register or delete a method provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_MethodProviderRegistration**.</span></span>

## <a name="requirements"></a><span data-ttu-id="863a4-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="863a4-121">Requirements</span></span>



| <span data-ttu-id="863a4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="863a4-122">Requirement</span></span> | <span data-ttu-id="863a4-123">Valore</span><span class="sxs-lookup"><span data-stu-id="863a4-123">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="863a4-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="863a4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="863a4-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="863a4-125">Windows Vista</span></span><br/>       |
| <span data-ttu-id="863a4-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="863a4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="863a4-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="863a4-127">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="863a4-128">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="863a4-128">Namespace</span></span><br/>                | <span data-ttu-id="863a4-129">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="863a4-129">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="863a4-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="863a4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="863a4-131">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="863a4-131">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="863a4-132">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="863a4-132">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="863a4-133">Registrazione di un provider di metodi</span><span class="sxs-lookup"><span data-stu-id="863a4-133">Registering a Method Provider</span></span>](registering-a-method-provider.md)
</dt> </dl>

 

