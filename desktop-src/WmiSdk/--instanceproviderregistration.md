---
description: Registra i provider di istanze in WMI.
ms.assetid: 6eba9bff-a5b9-4741-94ef-7d65b33d9aff
ms.tgt_platform: multiple
title: Classe __InstanceProviderRegistration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __InstanceProviderRegistration
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
ms.openlocfilehash: 45923c0c3ea3bfc28e67634e3b447e46b62765f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315254"
---
# <a name="__instanceproviderregistration-class"></a><span data-ttu-id="befae-103">\_\_Classe InstanceProviderRegistration</span><span class="sxs-lookup"><span data-stu-id="befae-103">\_\_InstanceProviderRegistration class</span></span>

<span data-ttu-id="befae-104">La classe di sistema **\_ \_ InstanceProviderRegistration** registra i provider di istanza in WMI.</span><span class="sxs-lookup"><span data-stu-id="befae-104">The **\_\_InstanceProviderRegistration** system class registers instance providers in WMI.</span></span>

<span data-ttu-id="befae-105">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="befae-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="befae-106">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="befae-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="befae-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="befae-107">Syntax</span></span>

``` syntax
class __InstanceProviderRegistration : __ObjectProviderRegistration
{
  sint32         InteractionType = 0;
  __Provider REF provider;
  string         QuerySupportLevels[];
  boolean        SupportsBatching;
  boolean        SupportsDelete = False;
  boolean        SupportsEnumeration = True;
  boolean        SupportsGet = False;
  boolean        SupportsPut = False;
  boolean        SupportsTransactions;
};
```

## <a name="members"></a><span data-ttu-id="befae-108">Members</span><span class="sxs-lookup"><span data-stu-id="befae-108">Members</span></span>

<span data-ttu-id="befae-109">La classe **\_ \_ InstanceProviderRegistration** dispone di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="befae-109">The **\_\_InstanceProviderRegistration** class has these types of members:</span></span>

-   [<span data-ttu-id="befae-110">Proprietà</span><span class="sxs-lookup"><span data-stu-id="befae-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="befae-111">Proprietà</span><span class="sxs-lookup"><span data-stu-id="befae-111">Properties</span></span>

<span data-ttu-id="befae-112">La classe **\_ \_ InstanceProviderRegistration** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="befae-112">The **\_\_InstanceProviderRegistration** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="befae-113">**InteractionType**</span><span class="sxs-lookup"><span data-stu-id="befae-113">**InteractionType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befae-114">Tipo di dati: **sint32**</span><span class="sxs-lookup"><span data-stu-id="befae-114">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="befae-115">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="befae-115">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="befae-116">Indica che un provider di classi o istanze fornisce dati o recupera dati da WMI e dal repository Common Information Model (CIM).</span><span class="sxs-lookup"><span data-stu-id="befae-116">Indicates that a class or instance provider supplies data, or retrieves data from WMI and the Common Information Model (CIM) repository.</span></span> <span data-ttu-id="befae-117">I provider Pull supportano l'accesso dinamico ai dati; e i provider di push archiviano i dati nel repository CIM e usano WMI per fornire l'accesso.</span><span class="sxs-lookup"><span data-stu-id="befae-117">Pull providers support dynamic access to their data; and push providers store their data in the CIM repository, and use WMI to provide access to it.</span></span> <span data-ttu-id="befae-118">Per ulteriori informazioni, vedere [determinare lo stato di push o pull](determining-push-or-pull-status.md).</span><span class="sxs-lookup"><span data-stu-id="befae-118">For more information, see [Determining Push or Pull Status](determining-push-or-pull-status.md).</span></span> <span data-ttu-id="befae-119">Il valore predefinito è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="befae-119">The default value is 0 (zero).</span></span>

<dt>

<span id="Pull"></span><span id="pull"></span><span id="PULL"></span>

<span data-ttu-id="befae-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span><span class="sxs-lookup"><span data-stu-id="befae-120"><span id="Pull"></span><span id="pull"></span><span id="PULL"></span>**Pull** (0)</span></span>


</dt> <dd>

<span data-ttu-id="befae-121">Il provider è un provider di pull.</span><span class="sxs-lookup"><span data-stu-id="befae-121">Provider is a pull provider.</span></span>

</dd> <dt>

<span id="Push"></span><span id="push"></span><span id="PUSH"></span>

<span data-ttu-id="befae-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span><span class="sxs-lookup"><span data-stu-id="befae-122"><span id="Push"></span><span id="push"></span><span id="PUSH"></span>**Push** (1)</span></span>


</dt> <dd>

<span data-ttu-id="befae-123">Il provider è un provider di push.</span><span class="sxs-lookup"><span data-stu-id="befae-123">Provider is a push provider.</span></span>

</dd> <dt>

<span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>

<span data-ttu-id="befae-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span><span class="sxs-lookup"><span data-stu-id="befae-124"><span id="PushVerify"></span><span id="pushverify"></span><span id="PUSHVERIFY"></span>**PushVerify** (2)</span></span>


</dt> <dd>

<span data-ttu-id="befae-125">Il provider è un provider di verifica push.</span><span class="sxs-lookup"><span data-stu-id="befae-125">Provider is a push-verify provider.</span></span> <span data-ttu-id="befae-126">Si noti che i provider di verifica push non sono attualmente supportati.</span><span class="sxs-lookup"><span data-stu-id="befae-126">Note that push-verify providers are not currently supported.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="befae-127">**provider**</span><span class="sxs-lookup"><span data-stu-id="befae-127">**provider**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befae-128">Tipo di dati: **\_ \_ provider**</span><span class="sxs-lookup"><span data-stu-id="befae-128">Data type: **\_\_Provider**</span></span>
</dt> <dt>

<span data-ttu-id="befae-129">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="befae-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="befae-130">Riferimento a un'istanza del [**\_ \_ provider**](--provider.md) che rappresenta il percorso dell'oggetto al provider dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="befae-130">Reference to an instance of [**\_\_Provider**](--provider.md) that represents the object path to the instance provider.</span></span> <span data-ttu-id="befae-131">Questa proprietà viene ereditata da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="befae-131">This property is inherited from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span>

</dd> <dt>

<span data-ttu-id="befae-132">**QuerySupportLevels**</span><span class="sxs-lookup"><span data-stu-id="befae-132">**QuerySupportLevels**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befae-133">Tipo di dati: matrice di **stringhe**</span><span class="sxs-lookup"><span data-stu-id="befae-133">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="befae-134">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="befae-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="befae-135">Matrice dei tipi di supporto incluso nel provider per l'elaborazione delle query.</span><span class="sxs-lookup"><span data-stu-id="befae-135">Array of the types of provider-included support for query processing.</span></span> <span data-ttu-id="befae-136">I provider di classi non supportano tutti i tipi di query.</span><span class="sxs-lookup"><span data-stu-id="befae-136">Class providers do not support all types of queries.</span></span> <span data-ttu-id="befae-137">I provider di istanze possono impostare **QuerySupportLevels** su **null** se non supportano l'elaborazione delle query.</span><span class="sxs-lookup"><span data-stu-id="befae-137">Instance providers can set **QuerySupportLevels** to **NULL** if they do not support query processing.</span></span> <span data-ttu-id="befae-138">I provider che supportano le query implementano il metodo [**IWbemServices:: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) e impostano questa proprietà su uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="befae-138">Providers that support queries implement the [**IWbemServices::ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) method, and set this property to one or more of the following values.</span></span>

<dt>



 <span data-ttu-id="befae-139">("WQL: UnarySelect")</span><span class="sxs-lookup"><span data-stu-id="befae-139">("WQL:UnarySelect")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="befae-140">("WQL: References")</span><span class="sxs-lookup"><span data-stu-id="befae-140">("WQL:References")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="befae-141">("WQL: Associrs")</span><span class="sxs-lookup"><span data-stu-id="befae-141">("WQL:Associators")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="befae-142">("WQL: V1ProviderDefined")</span><span class="sxs-lookup"><span data-stu-id="befae-142">("WQL:V1ProviderDefined")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="befae-143">**SupportsBatching**</span><span class="sxs-lookup"><span data-stu-id="befae-143">**SupportsBatching**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befae-144">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="befae-144">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="befae-145">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="befae-145">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="befae-146">Non usato.</span><span class="sxs-lookup"><span data-stu-id="befae-146">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="befae-147">**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="befae-147">**SupportsDelete**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befae-148">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="befae-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="befae-149">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="befae-149">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="befae-150">Se **true**, il provider supporta l'eliminazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="befae-150">If **True**, the provider supports data deletion.</span></span>

<dt>

<span data-ttu-id="befae-151">Vero</span><span class="sxs-lookup"><span data-stu-id="befae-151">True</span></span>
</dt> <dd>

<span data-ttu-id="befae-152">Il provider supporta l'eliminazione di una classe o di un'istanza implementando [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (provider di classi) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (provider di istanze).</span><span class="sxs-lookup"><span data-stu-id="befae-152">The provider supports class or instance deletion by implementing either [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) (class providers), or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) (instance providers).</span></span>

</dd> <dt>

<span data-ttu-id="befae-153">Falso</span><span class="sxs-lookup"><span data-stu-id="befae-153">False</span></span>
</dt> <dd>

<span data-ttu-id="befae-154">Il provider non supporta l'eliminazione dei dati e restituisce **il \_ provider WBEM e \_ non è \_ \_ in grado** di [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) o [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="befae-154">The provider does not support data deletion, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) or [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="befae-155">**SupportsEnumeration**</span><span class="sxs-lookup"><span data-stu-id="befae-155">**SupportsEnumeration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befae-156">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="befae-156">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="befae-157">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="befae-157">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="befae-158">Se **true**, il provider supporta l'enumerazione dei dati.</span><span class="sxs-lookup"><span data-stu-id="befae-158">If **True**, the provider supports data enumeration.</span></span>

<dt>



 <span data-ttu-id="befae-159">True</span><span class="sxs-lookup"><span data-stu-id="befae-159">(True)</span></span>


</dt> <dd>

<span data-ttu-id="befae-160">Il provider supporta l'enumerazione dei dati implementando uno dei [**IWbemServices:: CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (provider di classi) o [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (provider di istanze).</span><span class="sxs-lookup"><span data-stu-id="befae-160">The provider supports data enumeration by implementing one of either [**IWbemServices::CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) (class providers), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) (instance providers).</span></span>

</dd> <dt>



 <span data-ttu-id="befae-161">False</span><span class="sxs-lookup"><span data-stu-id="befae-161">(False)</span></span>


</dt> <dd>

<span data-ttu-id="befae-162">Il provider non supporta l'enumerazione dei dati e restituisce **il \_ provider WBEM e \_ non è \_ \_ in grado** di [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) o [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span><span class="sxs-lookup"><span data-stu-id="befae-162">The provider does not support data enumeration, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) or [**CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="befae-163">**SupportsGet**</span><span class="sxs-lookup"><span data-stu-id="befae-163">**SupportsGet**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befae-164">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="befae-164">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="befae-165">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="befae-165">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="befae-166">Se **true**, il provider di classi o istanze supporta il recupero dei dati.</span><span class="sxs-lookup"><span data-stu-id="befae-166">If **True**, the class or instance provider supports data retrieval.</span></span>

<dt>

<span data-ttu-id="befae-167">Vero</span><span class="sxs-lookup"><span data-stu-id="befae-167">True</span></span>
</dt> <dd>

<span data-ttu-id="befae-168">Il provider supporta il recupero dei dati mediante l'implementazione di [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="befae-168">The provider supports data retrieval by implementing [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> <dt>

<span data-ttu-id="befae-169">Falso</span><span class="sxs-lookup"><span data-stu-id="befae-169">False</span></span>
</dt> <dd>

<span data-ttu-id="befae-170">Il provider non supporta il recupero dei dati e restituisce il **\_ provider WBEM \_ e \_ non \_ idoneo** per [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span><span class="sxs-lookup"><span data-stu-id="befae-170">The provider does not support data retrieval, and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="befae-171">**SupportsPut**</span><span class="sxs-lookup"><span data-stu-id="befae-171">**SupportsPut**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befae-172">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="befae-172">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="befae-173">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="befae-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="befae-174">Se **true**, la classe o il provider di istanze supporta la modifica dei dati.</span><span class="sxs-lookup"><span data-stu-id="befae-174">If **True**, the class or instance provider supports data modification.</span></span>

<dt>



 <span data-ttu-id="befae-175">True</span><span class="sxs-lookup"><span data-stu-id="befae-175">(True)</span></span>


</dt> <dd>

<span data-ttu-id="befae-176">Il provider supporta la modifica della classe o dell'istanza implementando uno dei metodi seguenti: [**IWbemServices::P utclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (provider di classi) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (provider di classi).</span><span class="sxs-lookup"><span data-stu-id="befae-176">The provider supports class or instance modification by implementing one of the following methods: [**IWbemServices::PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) (class providers), or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) (class providers).</span></span>

</dd> <dt>



 <span data-ttu-id="befae-177">False</span><span class="sxs-lookup"><span data-stu-id="befae-177">(False)</span></span>


</dt> <dd>

<span data-ttu-id="befae-178">Il provider non supporta la modifica dei dati e restituisce il **\_ provider WBEM e \_ \_ non \_ idoneo** per [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) o [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span><span class="sxs-lookup"><span data-stu-id="befae-178">The provider does not support data modification and returns **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** from [**PutClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync) or [**PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync).</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="befae-179">**SupportsTransactions**</span><span class="sxs-lookup"><span data-stu-id="befae-179">**SupportsTransactions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="befae-180">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="befae-180">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="befae-181">Tipo di accesso: lettura/scrittura</span><span class="sxs-lookup"><span data-stu-id="befae-181">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="befae-182">Non usato.</span><span class="sxs-lookup"><span data-stu-id="befae-182">Not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="befae-183">Commenti</span><span class="sxs-lookup"><span data-stu-id="befae-183">Remarks</span></span>

<span data-ttu-id="befae-184">La classe **\_ \_ InstanceProviderRegistration** deriva da [**\_ \_ ObjectProviderRegistration**](--objectproviderregistration.md), derivata da [**\_ \_ ProviderRegistration**](--providerregistration.md).</span><span class="sxs-lookup"><span data-stu-id="befae-184">The **\_\_InstanceProviderRegistration** class is derived from [**\_\_ObjectProviderRegistration**](--objectproviderregistration.md), which is derived from [**\_\_ProviderRegistration**](--providerregistration.md).</span></span> <span data-ttu-id="befae-185">Solo gli amministratori possono registrare un provider di istanze creando un'istanza di [**\_ \_ Win32Provider**](--win32provider.md) e **\_ \_ InstanceProviderRegistration**.</span><span class="sxs-lookup"><span data-stu-id="befae-185">Only administrators can register an instance provider by creating an instance of [**\_\_Win32Provider**](--win32provider.md) and **\_\_InstanceProviderRegistration**.</span></span> <span data-ttu-id="befae-186">Solo gli amministratori possono eliminare un provider.</span><span class="sxs-lookup"><span data-stu-id="befae-186">Only administrators can delete a provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="befae-187">Requisiti</span><span class="sxs-lookup"><span data-stu-id="befae-187">Requirements</span></span>



| <span data-ttu-id="befae-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="befae-188">Requirement</span></span> | <span data-ttu-id="befae-189">Valore</span><span class="sxs-lookup"><span data-stu-id="befae-189">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="befae-190">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="befae-190">Minimum supported client</span></span><br/> | <span data-ttu-id="befae-191">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="befae-191">Windows Vista</span></span><br/>       |
| <span data-ttu-id="befae-192">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="befae-192">Minimum supported server</span></span><br/> | <span data-ttu-id="befae-193">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="befae-193">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="befae-194">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="befae-194">Namespace</span></span><br/>                | <span data-ttu-id="befae-195">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="befae-195">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="befae-196">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="befae-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="befae-197">**\_\_ObjectProviderRegistration**</span><span class="sxs-lookup"><span data-stu-id="befae-197">**\_\_ObjectProviderRegistration**</span></span>](/windows/desktop/WmiSdk/--objectproviderregistration)
</dt> <dt>

[<span data-ttu-id="befae-198">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="befae-198">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="befae-199">Registrazione di un provider di classi</span><span class="sxs-lookup"><span data-stu-id="befae-199">Registering a Class Provider</span></span>](registering-a-class-provider.md)
</dt> <dt>

[<span data-ttu-id="befae-200">Registrazione di un provider di istanze</span><span class="sxs-lookup"><span data-stu-id="befae-200">Registering an Instance Provider</span></span>](registering-an-instance-provider.md)
</dt> </dl>

 

