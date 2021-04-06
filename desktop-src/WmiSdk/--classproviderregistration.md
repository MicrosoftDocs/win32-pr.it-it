---
description: Registra i provider di classi in WMI.
ms.assetid: 1af7d9ed-c5e4-47e4-839d-53d579ef7cea
ms.tgt_platform: multiple
title: Classe __ClassProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ClassProviderRegistration
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 32442122624035ec376bed3be8b3ef20c80f8524
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760460"
---
# <a name="__classproviderregistration-class"></a><span data-ttu-id="4e429-103">\_\_Classe ClassProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="4e429-103">\_\_ClassProviderRegistration class</span></span>

<span data-ttu-id="4e429-104">La classe di sistema **\_ \_ ClassProviderRegistration** registra i provider di classi in WMI.</span><span class="sxs-lookup"><span data-stu-id="4e429-104">The **\_\_ClassProviderRegistration** system class registers class providers in WMI.</span></span>

<span data-ttu-id="4e429-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="4e429-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4e429-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="4e429-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e429-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4e429-107">Syntax</span></span>

``` syntax
class __ClassProviderRegistration : __ObjectProviderRegistration
{
  boolean        SupportsBatching;
  datetime       CacheRefreshInterval;
  sint32         InteractionType = 0;
  __Provider REF provider;
  boolean        PerUserSchema;
  string         QuerySupportLevels[];
  string         ReferencedSetQueries[];
  string         ResultSetQueries[];
  boolean        ReSynchroniseOnNamespaceOpen;
  boolean        SuppportsBatching;
  boolean        SupportsEnumeration = False;
  boolean        SupportsDelete = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
  string         UnsupportedQueries[];
  uint32         Version;
};
```

## <a name="members"></a><span data-ttu-id="4e429-108">Members</span><span class="sxs-lookup"><span data-stu-id="4e429-108">Members</span></span>

<span data-ttu-id="4e429-109">La classe **\_ \_ ClassProviderRegistration** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="4e429-109">The **\_\_ClassProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="4e429-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e429-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4e429-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="4e429-111">Properties</span></span>

<span data-ttu-id="4e429-112">La classe **\_ \_ ClassProviderRegistration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="4e429-112">The **\_\_ClassProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4e429-113">**CacheRefreshInterval**</span><span class="sxs-lookup"><span data-stu-id="4e429-113">**CacheRefreshInterval**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-114">Tipo di dati: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="4e429-114">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="4e429-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-116">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4e429-116">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e429-117">**InteractionType**</span><span class="sxs-lookup"><span data-stu-id="4e429-117">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-118">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4e429-118">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e429-119">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-119">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-120">Indica se il provider di classi o istanze fornisce dati oppure si basa su WMI e sul repository Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="4e429-120">Indicates whether or not the class or instance provider supplies data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="4e429-121">I provider Pull supportano l'accesso dinamico ai dati e i provider di push archiviano i dati nel repository CIM e si basano su WMI per fornire l'accesso.</span><span class="sxs-lookup"><span data-stu-id="4e429-121">Pull providers support dynamic access to data, and push providers store data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="4e429-122">Il valore predefinito è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="4e429-122">The default value is 0 (zero).</span></span> <span data-ttu-id="4e429-123">Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4e429-123">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="4e429-124">Per ulteriori informazioni, vedere [determinare lo stato di push o pull](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="4e429-124">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="4e429-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span><span class="sxs-lookup"><span data-stu-id="4e429-125"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="4e429-126">Il provider è un provider di pull.</span><span class="sxs-lookup"><span data-stu-id="4e429-126">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="4e429-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span><span class="sxs-lookup"><span data-stu-id="4e429-127"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="4e429-128">Il provider è un provider di push.</span><span class="sxs-lookup"><span data-stu-id="4e429-128">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="4e429-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span><span class="sxs-lookup"><span data-stu-id="4e429-129"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="4e429-130">Il provider è un provider di verifica push.</span><span class="sxs-lookup"><span data-stu-id="4e429-130">Provider is a push-verify provider.</span></span> <span data-ttu-id="4e429-131">Si noti che al momento i provider **PushVerify** non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="4e429-131">Note that **PushVerify** providers are not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e429-132">**PerUserSchema**</span><span class="sxs-lookup"><span data-stu-id="4e429-132">**PerUserSchema**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-133">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4e429-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e429-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-135">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4e429-135">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e429-136">**provider**</span><span class="sxs-lookup"><span data-stu-id="4e429-136">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-137">Tipo di dati: **\_ \_ provider**</span><span class="sxs-lookup"><span data-stu-id="4e429-137">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="4e429-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="4e429-138">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4e429-139">Percorso dell'oggetto a un provider di classi.</span><span class="sxs-lookup"><span data-stu-id="4e429-139">Object path to a class provider.</span></span> <span data-ttu-id="4e429-140">Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4e429-140">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e429-141">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="4e429-141">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-142">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4e429-142">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4e429-143">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-143">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-144">Matrice dei tipi di supporto incluso nel provider per l'elaborazione delle query.</span><span class="sxs-lookup"><span data-stu-id="4e429-144">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="4e429-145">Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4e429-145">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span> <span data-ttu-id="4e429-146">I provider di classi sono necessari per supportare almeno un tipo di query.</span><span class="sxs-lookup"><span data-stu-id="4e429-146">Class providers are required to support at least one type of query.</span></span> <span data-ttu-id="4e429-147">I provider di istanze possono impostare **QuerySupportLevels** su **null** se non supportano l'elaborazione delle query.</span><span class="sxs-lookup"><span data-stu-id="4e429-147">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="4e429-148">I provider che supportano le query implementano il metodo [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) e impostano questa proprietà su uno o più dei valori seguenti:</span><span class="sxs-lookup"><span data-stu-id="4e429-148">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values:</span></span>

<dt>



 <span data-ttu-id="4e429-149">("WQL: UnarySelect")</span><span class="sxs-lookup"><span data-stu-id="4e429-149">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4e429-150">("WQL: References")</span><span class="sxs-lookup"><span data-stu-id="4e429-150">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4e429-151">("WQL: Associrs")</span><span class="sxs-lookup"><span data-stu-id="4e429-151">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="4e429-152">("WQL: V1ProviderDefined")</span><span class="sxs-lookup"><span data-stu-id="4e429-152">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4e429-153">**ReferencedSetQueries**</span><span class="sxs-lookup"><span data-stu-id="4e429-153">**ReferencedSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-154">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4e429-154">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4e429-155">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-155">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-156">Una o più query che descrivono il set di classi di riferimento supportate da un provider di classi.</span><span class="sxs-lookup"><span data-stu-id="4e429-156">One or more queries that describe the set of referenced classes that a class provider supports.</span></span> <span data-ttu-id="4e429-157">I provider che possono fornire classi di associazione devono includere almeno una query in questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="4e429-157">Providers that can supply association classes must include at least one query in this property.</span></span>

</dd> <dt>

<span data-ttu-id="4e429-158">**ResultSetQueries**</span><span class="sxs-lookup"><span data-stu-id="4e429-158">**ResultSetQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-159">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4e429-159">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4e429-160">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-160">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-161">Una o più query che descrivono il set di tutte le classi che possono essere fornite dal provider di classi o un superset di tali classi.</span><span class="sxs-lookup"><span data-stu-id="4e429-161">One or more queries that describe the set of all classes that can be supplied by the class provider, or a superset of those classes.</span></span> <span data-ttu-id="4e429-162">Questa proprietà non specifica mai un subset di classi supportate.</span><span class="sxs-lookup"><span data-stu-id="4e429-162">This property never specifies a subset of supported classes.</span></span>

</dd> <dt>

<span data-ttu-id="4e429-163">**ReSynchroniseOnNamespaceOpen**</span><span class="sxs-lookup"><span data-stu-id="4e429-163">**ReSynchroniseOnNamespaceOpen**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-164">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4e429-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e429-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-166">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4e429-166">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e429-167">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="4e429-167">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-168">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4e429-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e429-169">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-170">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4e429-170">Not used.</span></span>

<span data-ttu-id="4e429-171">Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4e429-171">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="4e429-172">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="4e429-172">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-173">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4e429-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e429-174">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-175">Se **true**, il provider supporta l'eliminazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="4e429-175">If **TRUE**, the provider supports data deletion.</span></span> <span data-ttu-id="4e429-176">Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4e429-176">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="4e429-177">True</span><span class="sxs-lookup"><span data-stu-id="4e429-177">(True)</span></span>


</dt> <dd>

<span data-ttu-id="4e429-178">Il provider supporta l'eliminazione di una classe o di un'istanza implementando uno dei [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (provider di classi) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (provider di istanze).</span><span class="sxs-lookup"><span data-stu-id="4e429-178">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="4e429-179">False</span><span class="sxs-lookup"><span data-stu-id="4e429-179">(False)</span></span>


</dt> <dd>

<span data-ttu-id="4e429-180">Il provider non supporta l'eliminazione dei dati e restituisce **il \_ provider WBEM e \_ non è \_ \_ in grado** di [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) o [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="4e429-180">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e429-181">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="4e429-181">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-182">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4e429-182">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e429-183">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-183">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-184">Se **true**, il provider supporta l'enumerazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="4e429-184">If **TRUE**, the provider supports data enumeration.</span></span> <span data-ttu-id="4e429-185">Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4e429-185">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="4e429-186">True</span><span class="sxs-lookup"><span data-stu-id="4e429-186">(True)</span></span>


</dt> <dd>

<span data-ttu-id="4e429-187">Il provider supporta l'enumerazione dei dati implementando uno dei [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (provider di classi) o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (provider di istanze).</span><span class="sxs-lookup"><span data-stu-id="4e429-187">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="4e429-188">False</span><span class="sxs-lookup"><span data-stu-id="4e429-188">(False)</span></span>


</dt> <dd>

<span data-ttu-id="4e429-189">Il provider non supporta l'enumerazione dei dati e restituisce **il \_ provider WBEM e \_ non è \_ \_ in grado** di [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) o [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="4e429-189">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e429-190">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="4e429-190">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-191">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4e429-191">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e429-192">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-193">Se **true**, il provider di classi o istanze supporta il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="4e429-193">If **TRUE**, the class or instance provider supports data retrieval.</span></span> <span data-ttu-id="4e429-194">Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4e429-194">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="4e429-195">True</span><span class="sxs-lookup"><span data-stu-id="4e429-195">(True)</span></span>


</dt> <dd>

<span data-ttu-id="4e429-196">Il provider supporta il recupero dei dati mediante l'implementazione di [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="4e429-196">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>



 <span data-ttu-id="4e429-197">False</span><span class="sxs-lookup"><span data-stu-id="4e429-197">(False)</span></span>


</dt> <dd>

<span data-ttu-id="4e429-198">Il provider non supporta il recupero dei dati e restituisce il **\_ provider WBEM \_ e \_ non \_ idoneo** per [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="4e429-198">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e429-199">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="4e429-199">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-200">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4e429-200">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e429-201">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-201">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-202">Se **true**, la classe o il provider di istanze supporta la modifica dei dati.</span><span class="sxs-lookup"><span data-stu-id="4e429-202">If **TRUE**, the class or instance provider supports data modification.</span></span> <span data-ttu-id="4e429-203">Questa proprietà viene ereditata da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4e429-203">This property is inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md).</span></span>

<dt>



 <span data-ttu-id="4e429-204">True</span><span class="sxs-lookup"><span data-stu-id="4e429-204">(True)</span></span>


</dt> <dd>

<span data-ttu-id="4e429-205">Il provider supporta la modifica della classe o dell'istanza implementando uno dei [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provider di classi) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provider di classi).</span><span class="sxs-lookup"><span data-stu-id="4e429-205">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="4e429-206">False</span><span class="sxs-lookup"><span data-stu-id="4e429-206">(False)</span></span>


</dt> <dd>

<span data-ttu-id="4e429-207">Il provider non supporta la modifica dei dati e restituisce il **\_ provider WBEM e \_ \_ non \_ idoneo** per [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) o [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="4e429-207">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="4e429-208">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="4e429-208">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-209">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4e429-209">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e429-210">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-210">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-211">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4e429-211">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e429-212">**SuppportsBatching**</span><span class="sxs-lookup"><span data-stu-id="4e429-212">**SuppportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-213">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="4e429-213">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4e429-214">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-214">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-215">Non usato.</span><span class="sxs-lookup"><span data-stu-id="4e429-215">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="4e429-216">**UnsupportedQueries**</span><span class="sxs-lookup"><span data-stu-id="4e429-216">**UnsupportedQueries**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-217">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="4e429-217">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="4e429-218">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-218">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-219">Una o più query che descrivono il set di classi non supportate dal provider di classi.</span><span class="sxs-lookup"><span data-stu-id="4e429-219">One or more queries that describe the set of classes that the class provider does not support.</span></span> <span data-ttu-id="4e429-220">Utilizzare questa proprietà per sottrarre dal set di classi implicito da **ResultSetQueries**.</span><span class="sxs-lookup"><span data-stu-id="4e429-220">Use this property to subtract from the set of classes implied by **ResultSetQueries**.</span></span>

</dd> <dt>

<span data-ttu-id="4e429-221">**Versione**</span><span class="sxs-lookup"><span data-stu-id="4e429-221">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4e429-222">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4e429-222">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4e429-223">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="4e429-223">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="4e429-224">Versione del provider di classi.</span><span class="sxs-lookup"><span data-stu-id="4e429-224">Version of this class provider.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4e429-225">Commenti</span><span class="sxs-lookup"><span data-stu-id="4e429-225">Remarks</span></span>

<span data-ttu-id="4e429-226">La classe **\_ \_ ClassProviderRegistration** deriva da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), derivata da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="4e429-226">The **\_\_ClassProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="4e429-227">Le proprietà ereditate da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md) indicano se il provider di classi supporta il recupero, la modifica, l'eliminazione, l'enumerazione e l'elaborazione di query dei dati.</span><span class="sxs-lookup"><span data-stu-id="4e429-227">The properties inherited from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md) indicate whether or not the class provider supports data retrieval, modification, deletion, enumeration and query processing.</span></span> <span data-ttu-id="4e429-228">La proprietà **InteractionType** specifica se il provider di classi è o meno progettato come provider pull o push.</span><span class="sxs-lookup"><span data-stu-id="4e429-228">The **InteractionType** property specifies whether or not the class provider is designed as a pull or push provider.</span></span> <span data-ttu-id="4e429-229">Per ulteriori informazioni, vedere [determinare lo stato di push o pull](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="4e429-229">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span>

<span data-ttu-id="4e429-230">La classe [**\_ \_ ProviderRegistration**](--providerregistration.md) definisce la proprietà del [**provider**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="4e429-230">The [**\_\_ProviderRegistration**](--providerregistration.md) class defines the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) property.</span></span> <span data-ttu-id="4e429-231">Solo gli amministratori possono registrare un provider creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e **\_ \_ ClassProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="4e429-231">Only administrators can register a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_ClassProviderRegistration**.</span></span> <span data-ttu-id="4e429-232">Solo gli amministratori possono eliminare un provider.</span><span class="sxs-lookup"><span data-stu-id="4e429-232">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="4e429-233">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4e429-233">Requirements</span></span>



| <span data-ttu-id="4e429-234">Requisito</span><span class="sxs-lookup"><span data-stu-id="4e429-234">Requirement</span></span> | <span data-ttu-id="4e429-235">Valore</span><span class="sxs-lookup"><span data-stu-id="4e429-235">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="4e429-236">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e429-236">Minimum supported client</span></span><br/> | <span data-ttu-id="4e429-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4e429-237">Windows Vista</span></span><br/>       |
| <span data-ttu-id="4e429-238">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4e429-238">Minimum supported server</span></span><br/> | <span data-ttu-id="4e429-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4e429-239">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="4e429-240">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="4e429-240">Namespace</span></span><br/>                | <span data-ttu-id="4e429-241">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="4e429-241">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="4e429-242">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4e429-242">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e429-243">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="4e429-243">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="4e429-244">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="4e429-244">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="4e429-245">Registrazione di un provider di classi</span><span class="sxs-lookup"><span data-stu-id="4e429-245">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="4e429-246">Registrazione di un provider di istanze</span><span class="sxs-lookup"><span data-stu-id="4e429-246">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> <dt>

[<span data-ttu-id="4e429-247">**\_\_Win32Provider**</span><span class="sxs-lookup"><span data-stu-id="4e429-247">**\_\_Win32Provider**</span></span>](--win32provider.md)
</dt> </dl>

 

