---
description: Funge da classe padre per le classi utilizzate per registrare i provider di classi e istanze in WMI.
ms.assetid: f7c569be-8927-42a4-b96a-abe4b7e3e23c
ms.tgt_platform: multiple
title: Classe __ObjectProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ObjectProviderRegistration
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
ms.openlocfilehash: a60b24278fb235cec38c127e7ebbbb481e49a140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345901"
---
# <a name="__objectproviderregistration-class"></a><span data-ttu-id="5ce0e-103">\_\_Classe ObjectProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="5ce0e-103">\_\_ObjectProviderRegistration class</span></span>

<span data-ttu-id="5ce0e-104">La classe di sistema astratta **\_ \_ ObjectProviderRegistration** funge da classe padre per le classi utilizzate per registrare i provider di classi e istanze in WMI.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-104">The **\_\_ObjectProviderRegistration** abstract system class serves as the parent class for classes that are used to register class and instance providers in WMI.</span></span>

<span data-ttu-id="5ce0e-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5ce0e-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ce0e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5ce0e-107">Syntax</span></span>

``` syntax
[abstract]
class __ObjectProviderRegistration : __ProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = False;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a><span data-ttu-id="5ce0e-108">Members</span><span class="sxs-lookup"><span data-stu-id="5ce0e-108">Members</span></span>

<span data-ttu-id="5ce0e-109">La classe **\_ \_ ObjectProviderRegistration** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="5ce0e-109">The **\_\_ObjectProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="5ce0e-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ce0e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5ce0e-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="5ce0e-111">Properties</span></span>

<span data-ttu-id="5ce0e-112">La classe **\_ \_ ObjectProviderRegistration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-112">The **\_\_ObjectProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5ce0e-113">**InteractionType**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ce0e-114">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5ce0e-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ce0e-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ce0e-116">Indica se il provider di classi o istanze fornisce i propri dati oppure si basa su WMI e sul repository Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-116">Indicates whether or not the class or instance provider supplies its own data, or relies on WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="5ce0e-117">I provider Pull supportano l'accesso dinamico ai dati e i provider di push archiviano i dati nel repository CIM e si basano su WMI per fornire l'accesso.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-117">Pull providers support dynamic access to their data, and push providers store their data in the CIM repository, and rely on WMI to provide access to it.</span></span> <span data-ttu-id="5ce0e-118">Per ulteriori informazioni, vedere [determinare lo stato di push o pull](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="5ce0e-119">Il valore predefinito è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="5ce0e-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span><span class="sxs-lookup"><span data-stu-id="5ce0e-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5ce0e-121">Il provider è un provider di pull.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="5ce0e-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span><span class="sxs-lookup"><span data-stu-id="5ce0e-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5ce0e-123">Il provider è un provider di push.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="5ce0e-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span><span class="sxs-lookup"><span data-stu-id="5ce0e-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5ce0e-125">Il provider è un provider di verifica push.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="5ce0e-126">Si noti che la verifica push non è supportata in questo momento.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-126">Note that push-verify is not supported at this time.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5ce0e-127">**provider**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ce0e-128">Tipo di dati: **\_ \_ provider**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="5ce0e-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="5ce0e-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5ce0e-130">Riferimento a un'istanza del [**\_ \_ provider**](--provider.md) che rappresenta il percorso di un oggetto del provider di oggetti.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents an object path to the object provider.</span></span> <span data-ttu-id="5ce0e-131">Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="5ce0e-132">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ce0e-133">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5ce0e-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ce0e-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ce0e-135">Matrice dei tipi di supporto incluso nel provider per l'elaborazione delle query.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="5ce0e-136">I provider di classi non supportano alcun tipo di query.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-136">Class providers do not support any type of queries.</span></span> <span data-ttu-id="5ce0e-137">I provider di istanze possono impostare **QuerySupportLevels** su **null** se non supportano l'elaborazione delle query.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="5ce0e-138">I provider che supportano le query implementano il metodo [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) e impostano questa proprietà su uno o più dei valori seguenti (il tipo di proprietà è una matrice).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values (the property type is an array).</span></span>

<span data-ttu-id="5ce0e-139">"WQL: UnarySelect"</span><span class="sxs-lookup"><span data-stu-id="5ce0e-139">"WQL:UnarySelect"</span></span>

<span data-ttu-id="5ce0e-140">"WQL: References"</span><span class="sxs-lookup"><span data-stu-id="5ce0e-140">"WQL:References"</span></span>

<span data-ttu-id="5ce0e-141">"WQL: Associatisti"</span><span class="sxs-lookup"><span data-stu-id="5ce0e-141">"WQL:Associators"</span></span>

<span data-ttu-id="5ce0e-142">"WQL: V1ProviderDefined"</span><span class="sxs-lookup"><span data-stu-id="5ce0e-142">"WQL:V1ProviderDefined"</span></span>

</dd> <dt>

<span data-ttu-id="5ce0e-143">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ce0e-144">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ce0e-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ce0e-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ce0e-146">Non usato.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="5ce0e-147">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ce0e-148">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ce0e-149">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ce0e-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ce0e-150">Se **true**, il provider supporta l'eliminazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="5ce0e-151">Vero</span><span class="sxs-lookup"><span data-stu-id="5ce0e-151">True</span></span>
</dt> <dd>

<span data-ttu-id="5ce0e-152">Il provider supporta l'eliminazione di una classe o di un'istanza implementando uno dei [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (provider di classi) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (provider di istanze).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-152">The provider supports class or instance deletion by implementing one of either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="5ce0e-153">Falso</span><span class="sxs-lookup"><span data-stu-id="5ce0e-153">False</span></span>
</dt> <dd>

<span data-ttu-id="5ce0e-154">Il provider non supporta l'eliminazione dei dati e restituisce **il \_ provider WBEM e \_ non è \_ \_ in grado** di [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) o [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5ce0e-155">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ce0e-156">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ce0e-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ce0e-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ce0e-158">Se **true**, il provider supporta l'enumerazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-158">If **True**, the provider supports data enumeration.</span></span>

<dt>

<span data-ttu-id="5ce0e-159">Vero</span><span class="sxs-lookup"><span data-stu-id="5ce0e-159">True</span></span>
</dt> <dd>

<span data-ttu-id="5ce0e-160">Il provider supporta l'enumerazione dei dati implementando uno dei [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (provider di classi) o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (provider di istanze).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="5ce0e-161">Falso</span><span class="sxs-lookup"><span data-stu-id="5ce0e-161">False</span></span>
</dt> <dd>

<span data-ttu-id="5ce0e-162">Il provider non supporta l'enumerazione dei dati e restituisce **il \_ provider WBEM e \_ non è \_ \_ in grado** di [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) o [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5ce0e-163">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ce0e-164">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ce0e-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ce0e-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ce0e-166">Se **true**, il provider di classi o istanze supporta il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="5ce0e-167">Vero</span><span class="sxs-lookup"><span data-stu-id="5ce0e-167">True</span></span>
</dt> <dd>

<span data-ttu-id="5ce0e-168">Il provider supporta il recupero dei dati mediante l'implementazione di [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="5ce0e-169">Falso</span><span class="sxs-lookup"><span data-stu-id="5ce0e-169">False</span></span>
</dt> <dd>

<span data-ttu-id="5ce0e-170">Il provider non supporta il recupero dei dati e restituisce il **\_ provider WBEM \_ e \_ non \_ idoneo** per [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5ce0e-171">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ce0e-172">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ce0e-173">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ce0e-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ce0e-174">Se **true**, la classe o il provider di istanze supporta la modifica dei dati.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>

<span data-ttu-id="5ce0e-175">Vero</span><span class="sxs-lookup"><span data-stu-id="5ce0e-175">True</span></span>
</dt> <dd>

<span data-ttu-id="5ce0e-176">Il provider supporta la modifica della classe o dell'istanza implementando uno dei [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provider di classi) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provider di classi).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-176">The provider supports class or instance modification by implementing one of either [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>

<span data-ttu-id="5ce0e-177">Falso</span><span class="sxs-lookup"><span data-stu-id="5ce0e-177">False</span></span>
</dt> <dd>

<span data-ttu-id="5ce0e-178">Il provider non supporta la modifica dei dati e restituisce il **\_ provider WBEM e \_ \_ non \_ idoneo** per [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) o [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="5ce0e-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5ce0e-180">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="5ce0e-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="5ce0e-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="5ce0e-182">Non usato.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ce0e-183">Commenti</span><span class="sxs-lookup"><span data-stu-id="5ce0e-183">Remarks</span></span>

<span data-ttu-id="5ce0e-184">La classe **\_ \_ ObjectProviderRegistration** deriva da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-184">The **\_\_ObjectProviderRegistration** class is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

<span data-ttu-id="5ce0e-185">I provider di classi devono impostare la proprietà **SupportsEnumeration** su **true** perché i provider devono essere in grado di fornire WMI con un elenco delle relative classi.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-185">Class providers must set the **SupportsEnumeration** property to **True** because the providers must be able to supply WMI with a list of their classes.</span></span> <span data-ttu-id="5ce0e-186">Se un provider di classi tenta di impostare questa proprietà su **false**, WMI contrassegna la registrazione come non valida.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-186">If a class provider attempts to set this property to **False**, WMI flags the registration as illegal.</span></span> <span data-ttu-id="5ce0e-187">I provider di istanze non devono supportare l'enumerazione e possono scegliere di impostare **SupportsEnumeration** su **true** o **false**.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-187">Instance providers are not required to support enumeration, and can choose to set **SupportsEnumeration** to either **True** or **False**.</span></span>

<span data-ttu-id="5ce0e-188">Un provider che imposta **QuerySupportLevels** su "WQL: UnarySelect" può accettare una query costituita dall'istruzione SELECT di base come supportata nella versione 1,0 di WMI.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-188">A provider that sets **QuerySupportLevels** to "WQL:UnarySelect" can accept a query that consists of the basic SELECT statement as supported in WMI version 1.0.</span></span> <span data-ttu-id="5ce0e-189">È previsto che i provider di classi e istanze siano in grado di gestire la proprietà di sistema della **\_ \_ classe** .</span><span class="sxs-lookup"><span data-stu-id="5ce0e-189">Both class and instance providers are expected to be able to handle the **\_\_CLASS** system property.</span></span> <span data-ttu-id="5ce0e-190">Sono previsti anche provider di classi per elaborare la proprietà di sistema della **\_ \_ superclasse** e l'operatore ISA.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-190">Class providers are also expected to process the **\_\_SUPERCLASS** system property and the ISA operator.</span></span> <span data-ttu-id="5ce0e-191">L'operatore ISA viene utilizzato per espandere un set di risultati in classi derivate.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-191">The ISA operator is used to expand a result set to derived classes.</span></span> <span data-ttu-id="5ce0e-192">Se a un provider viene assegnata una query che non è in grado di interpretare, viene richiesto che WMI la gestisca restituendo il valore di errore **WBEM \_ E \_ troppo \_ complesso** .</span><span class="sxs-lookup"><span data-stu-id="5ce0e-192">If a provider is given a query that it cannot interpret, it requests that WMI handle it by returning the **WBEM\_E\_TOO\_COMPLEX** error value.</span></span> <span data-ttu-id="5ce0e-193">Per una descrizione della sintassi WQL valida, vedere [esecuzione di query con WQL](querying-with-wql.md).</span><span class="sxs-lookup"><span data-stu-id="5ce0e-193">For a description of valid WQL syntax, see [Querying with WQL](querying-with-wql.md).</span></span>

<span data-ttu-id="5ce0e-194">Un provider che imposta **QuerySupportLevels** su **WQL: V1ProviderDefined** può provare a supportare un set più ampio della sintassi SQL a proprio rischio, ad esempio la `ORDER BY` clausola.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-194">A provider that sets **QuerySupportLevels** to **WQL:V1ProviderDefined** can try to support a larger set of the SQL syntax at its own risk, such as the `ORDER BY` clause.</span></span> <span data-ttu-id="5ce0e-195">WMI non interpreta le clausole aggiuntive o tenta di verificare che il set di risultati sia corretto.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-195">WMI does not interpret the additional clauses, or attempt to ensure that the result set is correct.</span></span>

<span data-ttu-id="5ce0e-196">Solo gli amministratori possono registrare o eliminare un provider creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e registrando tale provider.</span><span class="sxs-lookup"><span data-stu-id="5ce0e-196">Only administrators can register or delete a provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and registering it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ce0e-197">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5ce0e-197">Requirements</span></span>



| <span data-ttu-id="5ce0e-198">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ce0e-198">Requirement</span></span> | <span data-ttu-id="5ce0e-199">Valore</span><span class="sxs-lookup"><span data-stu-id="5ce0e-199">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5ce0e-200">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ce0e-200">Minimum supported client</span></span><br/> | <span data-ttu-id="5ce0e-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ce0e-201">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5ce0e-202">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5ce0e-202">Minimum supported server</span></span><br/> | <span data-ttu-id="5ce0e-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ce0e-203">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5ce0e-204">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5ce0e-204">Namespace</span></span><br/>                | <span data-ttu-id="5ce0e-205">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="5ce0e-205">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5ce0e-206">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5ce0e-206">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ce0e-207">**\_\_ProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="5ce0e-207">**\_\_ProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--providerregistration)
</dt> <dt>

[<span data-ttu-id="5ce0e-208">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="5ce0e-208">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="5ce0e-209">Registrazione di un provider</span><span class="sxs-lookup"><span data-stu-id="5ce0e-209">Registering a Provider</span></span>](registering-a-provider.md)
</dt> </dl>

 

