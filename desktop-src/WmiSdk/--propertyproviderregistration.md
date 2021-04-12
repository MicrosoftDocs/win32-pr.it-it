---
description: Registra i provider di proprietà in WMI.
ms.assetid: 24792884-3fb9-4974-83d5-1c5fc1fa72a1
ms.tgt_platform: multiple
title: Classe __PropertyProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PropertyProviderRegistration
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 6d618a62eab4ba799a2d0e152763fcef6567fd42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529305"
---
# <a name="__propertyproviderregistration-class"></a><span data-ttu-id="34bbc-103">\_\_Classe PropertyProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="34bbc-103">\_\_PropertyProviderRegistration class</span></span>

<span data-ttu-id="34bbc-104">La classe di sistema **\_ \_ PropertyProviderRegistration** registra i provider di proprietà in WMI.</span><span class="sxs-lookup"><span data-stu-id="34bbc-104">The **\_\_PropertyProviderRegistration** system class registers property providers in WMI.</span></span>

<span data-ttu-id="34bbc-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="34bbc-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="34bbc-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="34bbc-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="34bbc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="34bbc-107">Syntax</span></span>

``` syntax
class __PropertyProviderRegistration : __ProviderRegistration
{
  __Provider REF provider;
  boolean        SupportsPut = False;
  boolean        SupportsGet = False;
};
```

## <a name="members"></a><span data-ttu-id="34bbc-108">Members</span><span class="sxs-lookup"><span data-stu-id="34bbc-108">Members</span></span>

<span data-ttu-id="34bbc-109">La classe **\_ \_ PropertyProviderRegistration** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="34bbc-109">The **\_\_PropertyProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="34bbc-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="34bbc-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="34bbc-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="34bbc-111">Properties</span></span>

<span data-ttu-id="34bbc-112">La classe **\_ \_ PropertyProviderRegistration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="34bbc-112">The **\_\_PropertyProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="34bbc-113">**provider**</span><span class="sxs-lookup"><span data-stu-id="34bbc-113">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34bbc-114">Tipo di dati: **\_ \_ provider**</span><span class="sxs-lookup"><span data-stu-id="34bbc-114">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="34bbc-115">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="34bbc-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="34bbc-116">Riferimento a un'istanza del [**\_ \_ provider**](--provider.md) che rappresenta il percorso dell'oggetto del provider di proprietà.</span><span class="sxs-lookup"><span data-stu-id="34bbc-116">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path of the property provider.</span></span> <span data-ttu-id="34bbc-117">Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="34bbc-117">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="34bbc-118">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="34bbc-118">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34bbc-119">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="34bbc-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34bbc-120">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="34bbc-120">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="34bbc-121">Descrive se il provider di classi o istanze supporta il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="34bbc-121">Describes whether the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="34bbc-122">Vero</span><span class="sxs-lookup"><span data-stu-id="34bbc-122">True</span></span>
</dt> <dd>

<span data-ttu-id="34bbc-123">Il provider supporta il recupero dei dati mediante l'implementazione di [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="34bbc-123">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="34bbc-124">Falso</span><span class="sxs-lookup"><span data-stu-id="34bbc-124">False</span></span>
</dt> <dd>

<span data-ttu-id="34bbc-125">Il provider non supporta il recupero dei dati e restituisce il **\_ provider WBEM \_ e \_ non \_ idoneo** per [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="34bbc-125">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="34bbc-126">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="34bbc-126">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="34bbc-127">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="34bbc-127">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="34bbc-128">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="34bbc-128">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="34bbc-129">Descrive se la classe o il provider di istanze supporta la modifica dei dati.</span><span class="sxs-lookup"><span data-stu-id="34bbc-129">Describes whether the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="34bbc-130">Vero</span><span class="sxs-lookup"><span data-stu-id="34bbc-130">True</span></span>
</dt> <dd>

<span data-ttu-id="34bbc-131">Il provider supporta la modifica della classe o dell'istanza implementando uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="34bbc-131">The provider supports class or instance modification by implementing one of the following methods:</span></span>

-   <span data-ttu-id="34bbc-132">[**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provider di classi)</span><span class="sxs-lookup"><span data-stu-id="34bbc-132">[**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers)</span></span>
-   <span data-ttu-id="34bbc-133">[**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provider di classi)</span><span class="sxs-lookup"><span data-stu-id="34bbc-133">[**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers)</span></span>

</dd> <dt>

<span data-ttu-id="34bbc-134">Falso</span><span class="sxs-lookup"><span data-stu-id="34bbc-134">False</span></span>
</dt> <dd>

<span data-ttu-id="34bbc-135">Il provider non supporta la modifica dei dati e restituisce il **\_ provider WBEM e \_ \_ non \_ idoneo** per [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) o [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="34bbc-135">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34bbc-136">Commenti</span><span class="sxs-lookup"><span data-stu-id="34bbc-136">Remarks</span></span>

<span data-ttu-id="34bbc-137">La classe **\_ \_ PropertyProviderRegistration** deriva da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="34bbc-137">The **\_\_PropertyProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="34bbc-138">Solo gli amministratori possono registrare un provider di proprietà creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e **\_ \_ PropertyProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="34bbc-138">Only administrators can register a property provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_PropertyProviderRegistration**.</span></span> <span data-ttu-id="34bbc-139">Solo gli amministratori possono eliminare un provider di proprietà.</span><span class="sxs-lookup"><span data-stu-id="34bbc-139">Only administrators can delete a property provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="34bbc-140">Requisiti</span><span class="sxs-lookup"><span data-stu-id="34bbc-140">Requirements</span></span>



| <span data-ttu-id="34bbc-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="34bbc-141">Requirement</span></span> | <span data-ttu-id="34bbc-142">Valore</span><span class="sxs-lookup"><span data-stu-id="34bbc-142">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="34bbc-143">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34bbc-143">Minimum supported client</span></span><br/> | <span data-ttu-id="34bbc-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="34bbc-144">Windows Vista</span></span><br/>       |
| <span data-ttu-id="34bbc-145">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="34bbc-145">Minimum supported server</span></span><br/> | <span data-ttu-id="34bbc-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="34bbc-146">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="34bbc-147">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="34bbc-147">Namespace</span></span><br/>                | <span data-ttu-id="34bbc-148">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="34bbc-148">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="34bbc-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="34bbc-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34bbc-150">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="34bbc-150">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="34bbc-151">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="34bbc-151">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="34bbc-152">Registrazione di un provider di proprietà</span><span class="sxs-lookup"><span data-stu-id="34bbc-152">Registering a Property Provider</span></span>](registering-a-property-provider.md)
</dt> </dl>

 

