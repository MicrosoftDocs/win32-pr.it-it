---
description: Di seguito sono elencati i qualificatori standard specifici di WMI.
ms.assetid: 63bdbafc-51f3-4714-8b7e-9d5a61cef45e
ms.tgt_platform: multiple
title: Qualificatori WMI standard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: e73b053354d86c4a56698a7a65c17e302425f56d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314574"
---
# <a name="standard-wmi-qualifiers"></a><span data-ttu-id="0d2aa-103">Qualificatori WMI standard</span><span class="sxs-lookup"><span data-stu-id="0d2aa-103">Standard WMI Qualifiers</span></span>

<span data-ttu-id="0d2aa-104">Di seguito sono elencati i qualificatori standard specifici di WMI.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-104">The following lists standard qualifiers specific to WMI.</span></span>

<dt>

<span data-ttu-id="0d2aa-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Emendamento**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-105"><span id="Amendment"></span><span id="amendment"></span><span id="AMENDMENT"></span>**Amendment**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-106">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-106">Data type: **boolean**</span></span>

<span data-ttu-id="0d2aa-107">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-107">Applies to: classes</span></span>

<span data-ttu-id="0d2aa-108">Indica che una classe contiene qualificatori modificati localizzati.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-108">Indicates that a class contains amended qualifiers that are localized.</span></span> <span data-ttu-id="0d2aa-109">Il valore predefinito è **true**.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-109">The default is **TRUE**.</span></span>

<span data-ttu-id="0d2aa-110">La classe associata può essere convertita.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-110">The associated class can be translated.</span></span> <span data-ttu-id="0d2aa-111">Per accedere alla versione tradotta, utilizzare l'identificatore delle impostazioni locali per costruire un nome di spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-111">To access the translated version, use the locale identifier to construct a namespace name.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Bypass \_ GetObject**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-112"><span id="Bypass_GetObject"></span><span id="bypass_getobject"></span><span id="BYPASS_GETOBJECT"></span>**Bypass\_GetObject**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-113">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-113">Data type: **boolean**</span></span>

<span data-ttu-id="0d2aa-114">Si applica a: metodi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-114">Applies to: methods</span></span>

<span data-ttu-id="0d2aa-115">Indica che la chiamata al metodo deve passare direttamente alla chiamata **ExecMethodAsync** del provider anziché al provider che effettua prima una chiamata a **GetObject** per convalidare il percorso dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-115">Indicates that the method call should pass directly to the **ExecMethodAsync** call of the provider rather than the provider first making a call to **GetObject** to validate the object path.</span></span> <span data-ttu-id="0d2aa-116">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-116">The default is **FALSE**.</span></span> <span data-ttu-id="0d2aa-117">L'uso di **bypass \_ GetObject** può migliorare significativamente le prestazioni.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-117">Using **Bypass\_GetObject** can significantly improve performance.</span></span>

<span data-ttu-id="0d2aa-118">Prima di usare il comando **bypass \_ GetObject**, assicurarsi che non vengano eseguite nessuna delle azioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="0d2aa-118">Before using **Bypass\_GetObject**, ensure that neither of the following actions are taken:</span></span>

-   <span data-ttu-id="0d2aa-119">Derivare una classe dalla classe.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-119">Derive a class from your class.</span></span>
-   <span data-ttu-id="0d2aa-120">Eseguire l'override del metodo con il qualificatore **\_ GetObject di bypass** .</span><span class="sxs-lookup"><span data-stu-id="0d2aa-120">Override the method that has the **Bypass\_GetObject** qualifier.</span></span>

<span data-ttu-id="0d2aa-121">L'impossibilità di seguire queste precauzioni può comportare la chiamata all'implementazione del metodo della classe padre anziché della classe figlio.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-121">Failure to follow these precautions can result in invoking the method implementation of the parent class instead of the child class.</span></span> <span data-ttu-id="0d2aa-122">Per ulteriori informazioni, vedere Utilizzo del \_ qualificatore GetObject di bypass.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-122">For more information, see Using the Bypass\_GetObject Qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**\_Chiave CIM**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-123"><span id="CIM_Key"></span><span id="cim_key"></span><span id="CIM_KEY"></span>**CIM\_Key**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-124">Tipo di dati **: \_ booleano CIM**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-124">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="0d2aa-125">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d2aa-125">Applies to: properties</span></span>

<span data-ttu-id="0d2aa-126">Indica che la proprietà associata è una proprietà chiave in CIM ma non in WMI.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-126">Indicates that the associated property is a key property in CIM but not in WMI.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="0d2aa-127"><span id="CIMType"></span><span id="cimtype"></span><span id="CIMTYPE"></span>[**CIMType**](cimtype-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-128">Tipo di dati: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-128">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="0d2aa-129">Si applica a: proprietà, metodi, parametri</span><span class="sxs-lookup"><span data-stu-id="0d2aa-129">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="0d2aa-130">Contiene testo che descrive il tipo di una proprietà.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-130">Contains text describing the type of a property.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-131"><span id="ClassContext"></span><span id="classcontext"></span><span id="CLASSCONTEXT"></span>**ClassContext**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-132">Tipo di dati: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-132">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="0d2aa-133">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-133">Applies to: classes</span></span>

<span data-ttu-id="0d2aa-134">Indica che una classe dispone di istanze associate a più informazioni in modo dinamico fornite da un provider.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-134">Indicates that a class has instances associated with more information dynamically supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Deprecato**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-135"><span id="Deprecated"></span><span id="deprecated"></span><span id="DEPRECATED"></span>**Deprecated**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-136">Tipo di dati **: \_ booleano CIM**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-136">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="0d2aa-137">Si applica a: proprietà, classi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-137">Applies to: properties, classes</span></span>

<span data-ttu-id="0d2aa-138">Indica che la proprietà è stata sostituita da un'altra proprietà.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-138">Indicates the property has been superseded by another property.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Visualizzare**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-139"><span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>**Display**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-140">Si applica a: classi, proprietà</span><span class="sxs-lookup"><span data-stu-id="0d2aa-140">Applies to: classes, properties</span></span>

<span data-ttu-id="0d2aa-141">**UUID** della classe associata.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-141">The **UUID** of the associated class.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dinamico**](dynamic-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="0d2aa-142"><span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>[**Dynamic**](dynamic-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-143">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-143">Data type: **boolean**</span></span>

<span data-ttu-id="0d2aa-144">Si applica a: classi, proprietà</span><span class="sxs-lookup"><span data-stu-id="0d2aa-144">Applies to: classes, properties</span></span>

<span data-ttu-id="0d2aa-145">Indica una classe le cui istanze vengono create dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-145">Indicates a class whose instances are created dynamically.</span></span> <span data-ttu-id="0d2aa-146">Il valore di questo qualificatore deve essere impostato su **true**.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-146">The value of this qualifier must be set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-147"><span id="DynProps"></span><span id="dynprops"></span><span id="DYNPROPS"></span>**DynProps**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-148">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-148">Data type: **boolean**</span></span>

<span data-ttu-id="0d2aa-149">Si applica a: classi, istanze</span><span class="sxs-lookup"><span data-stu-id="0d2aa-149">Applies to: classes, instances</span></span>

<span data-ttu-id="0d2aa-150">Indica che un'istanza contiene valori forniti dai provider di proprietà dinamici.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-150">Indicates that an instance contains values provided by dynamic property providers.</span></span> <span data-ttu-id="0d2aa-151">Il valore predefinito è **true**.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-151">The default is **TRUE**.</span></span>

<span data-ttu-id="0d2aa-152">È necessario specificare questo qualificatore in tale istanza.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-152">You must specify this qualifier on such an instance.</span></span> <span data-ttu-id="0d2aa-153">È consentito solo il valore **true** .</span><span class="sxs-lookup"><span data-stu-id="0d2aa-153">Only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Fissa**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-154"><span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>**Fixed**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-155">Tipo di dati **: \_ booleano CIM**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-155">Data type: **CIM\_BOOLEAN**</span></span>

<span data-ttu-id="0d2aa-156">Si applica a: istanze di</span><span class="sxs-lookup"><span data-stu-id="0d2aa-156">Applies to: instances</span></span>

<span data-ttu-id="0d2aa-157">Indica che il valore di questa proprietà non può essere modificato nel corso della durata dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-157">Indicates that the value of this property cannot change during the lifetime of the instance.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-158"><span id="ID"></span><span id="id"></span>**ID**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-158"><span id="ID"></span><span id="id"></span>**ID**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-159">Tipo di dati: **VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-159">Data type: **VT\_I4**</span></span>

<span data-ttu-id="0d2aa-160">Si applica a: proprietà, parametri</span><span class="sxs-lookup"><span data-stu-id="0d2aa-160">Applies to: properties, parameters</span></span>

<span data-ttu-id="0d2aa-161">Identifica in modo univoco e Sequenzia una proprietà o un parametro di metodo quando le istruzioni MOF vengono generate automaticamente.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-161">Uniquely identifies and sequences a property or method parameter when MOF statements are generated automatically.</span></span>

<span data-ttu-id="0d2aa-162">Questo qualificatore è necessario solo per i parametri del metodo.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-162">This qualifier is required for method parameters only.</span></span> <span data-ttu-id="0d2aa-163">Quando si creano parametri per un metodo, i progettisti di classi devono iniziare con ID (0) per il primo parametro e usare ogni numero intero successivo per ogni parametro successivo.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-163">When creating parameters for a method, class designers should begin with Id(0) for the first parameter and use each successive integer for each successive parameter.</span></span> <span data-ttu-id="0d2aa-164">Se i qualificatori **ID** vengono omessi intenzionalmente, il compilatore MOF genera automaticamente i qualificatori **ID** .</span><span class="sxs-lookup"><span data-stu-id="0d2aa-164">If the **ID** qualifiers are unintentionally omitted, the MOF compiler generates **ID** qualifiers automatically.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implementato**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-165"><span id="Implemented"></span><span id="implemented"></span><span id="IMPLEMENTED"></span>**Implemented**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-166">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-166">Data type: **boolean**</span></span>

<span data-ttu-id="0d2aa-167">Si applica a: metodi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-167">Applies to: methods</span></span>

<span data-ttu-id="0d2aa-168">Indica che un metodo dispone di un'implementazione fornita da un provider.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-168">Indicates that a method has an implementation supplied by a provider.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-169"><span id="InstanceContext"></span><span id="instancecontext"></span><span id="INSTANCECONTEXT"></span>**InstanceContext**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-170">Tipo di dati: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-170">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="0d2aa-171">Si applica a: istanze di</span><span class="sxs-lookup"><span data-stu-id="0d2aa-171">Applies to: instances</span></span>

<span data-ttu-id="0d2aa-172">Indica che un'istanza contiene valori forniti da un provider di proprietà dinamico.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-172">Indicates that an instance contains values provided by a dynamic property provider.</span></span>

<span data-ttu-id="0d2aa-173">Il valore viene passato al provider di proprietà come argomento al metodo [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) .</span><span class="sxs-lookup"><span data-stu-id="0d2aa-173">The value is passed to the property provider as an argument to the [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty) method.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-174"><span id="Locale"></span><span id="locale"></span><span id="LOCALE"></span>**Locale**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-175">Tipo di dati: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-175">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="0d2aa-176">Si applica a: classi o istanze</span><span class="sxs-lookup"><span data-stu-id="0d2aa-176">Applies to: classes or instances</span></span>

<span data-ttu-id="0d2aa-177">Specifica la lingua dell'origine per una classe o un'istanza.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-177">Specifies the language of origin for a class or instance.</span></span> <span data-ttu-id="0d2aa-178">Per altre informazioni sui valori delle impostazioni locali, vedere [codici delle impostazioni locali](#locale-codes).</span><span class="sxs-lookup"><span data-stu-id="0d2aa-178">For more information about locale values, see [Locale Codes](#locale-codes).</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-179"><span id="NamespaceSecuritySDDL"></span><span id="namespacesecuritysddl"></span><span id="NAMESPACESECURITYSDDL"></span>**NamespaceSecuritySDDL**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-180">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-180">Data type: **string array**</span></span>

<span data-ttu-id="0d2aa-181">Si applica a: istanze dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-181">Applies to: namespace instances</span></span>

<span data-ttu-id="0d2aa-182">Specifica un descrittore di sicurezza per lo spazio dei nomi in formato [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .</span><span class="sxs-lookup"><span data-stu-id="0d2aa-182">Specifies a security descriptor for the namespace in [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span> <span data-ttu-id="0d2aa-183">Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi quando viene creato lo spazio dei nomi](setting-namespace-security-when-the-namespace-is-created.md).</span><span class="sxs-lookup"><span data-stu-id="0d2aa-183">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span> <span data-ttu-id="0d2aa-184">La stringa SDDL viene elaborata da WMI per stabilire la sicurezza dello spazio dei nomi ma non memorizzata come stringa.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-184">The SDDL string is processed by WMI to establish the namespace security but not stored as a string.</span></span> <span data-ttu-id="0d2aa-185">Se non viene specificato alcun descrittore di sicurezza, viene utilizzata la sicurezza predefinita.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-185">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="0d2aa-186">Per altre informazioni, vedere [impostazione dei descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="0d2aa-186">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Opzionale**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-187"><span id="Optional"></span><span id="optional"></span><span id="OPTIONAL"></span>**Optional**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-188">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-188">Data type: **boolean**</span></span>

<span data-ttu-id="0d2aa-189">Si applica a: parametri</span><span class="sxs-lookup"><span data-stu-id="0d2aa-189">Applies to: parameters</span></span>

<span data-ttu-id="0d2aa-190">Indica che un parametro non è obbligatorio e che dispone di un valore predefinito corretto.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-190">Indicates that a parameter is not required, and that it has a well-behaved default value.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Privilegi**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-191"><span id="Privileges"></span><span id="privileges"></span><span id="PRIVILEGES"></span>**Privileges**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-192">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-192">Data type: **string array**</span></span>

<span data-ttu-id="0d2aa-193">Si applica a: proprietà, metodi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-193">Applies to: properties, methods</span></span>

<span data-ttu-id="0d2aa-194">Insieme di valori utilizzati per informare il client quali privilegi sono necessari per creare istanze, compilare proprietà o eseguire metodi.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-194">Set of values used to inform the client which privileges are required to create instances, fill in properties, or perform methods.</span></span> <span data-ttu-id="0d2aa-195">Il valore predefinito è **false**.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-195">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-196"><span id="PropertyContext"></span><span id="propertycontext"></span><span id="PROPERTYCONTEXT"></span>**PropertyContext**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-197">Tipo di dati: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-197">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="0d2aa-198">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d2aa-198">Applies to: properties</span></span>

<span data-ttu-id="0d2aa-199">Indica che una proprietà dell'istanza contiene valori forniti dai provider di proprietà dinamici.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-199">Indicates that an instance property contains values provided by dynamic property providers.</span></span>

<span data-ttu-id="0d2aa-200">È necessario specificare questo qualificatore su una proprietà di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-200">You must specify this qualifier on such a property.</span></span> <span data-ttu-id="0d2aa-201">Il valore viene passato al provider di proprietà come argomento di [**IWbemPropertyProvider:: GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).</span><span class="sxs-lookup"><span data-stu-id="0d2aa-201">The value is passed to the property provider as an argument to [**IWbemPropertyProvider::GetProperty**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbempropertyprovider-getproperty).</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-202"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-203">Tipo di dati: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-203">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="0d2aa-204">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-204">Applies to: classes</span></span>

<span data-ttu-id="0d2aa-205">Il valore di questo qualificatore è il nome del provider dinamico che fornisce istanze della classe e aggiorna i dati dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-205">The value of this qualifier is the name of the dynamic provider that provides class instances and refreshes instance data.</span></span> <span data-ttu-id="0d2aa-206">Questo nome deve essere registrato con WMI creando un'istanza della classe [**\_ \_ Win32Provider**](--win32provider.md) con la proprietà **Name** che contiene questo nome.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-206">This name must be registered with WMI by creating an instance of the [**\_\_Win32Provider**](--win32provider.md) class with the **Name** property containing this name.</span></span> <span data-ttu-id="0d2aa-207">Quando questo qualificatore viene specificato in una classe le cui istanze vengono fornite in modo dinamico, è necessario specificare anche il qualificatore **dinamico** .</span><span class="sxs-lookup"><span data-stu-id="0d2aa-207">When this qualifier is specified on a class whose instances are provided dynamically, the **Dynamic** qualifier must also be specified.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-208"><span id="RequiresEncryption"></span><span id="requiresencryption"></span><span id="REQUIRESENCRYPTION"></span>**RequiresEncryption**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-209">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-209">Data type: **boolean**</span></span>

<span data-ttu-id="0d2aa-210">Si applica a: istanze dello spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-210">Applies to: namespace instances</span></span>

<span data-ttu-id="0d2aa-211">Se è impostato su **true**, **RequiresEncryption** contrassegna uno spazio dei nomi in modo che le applicazioni e gli script client debbano connettersi con l'autenticazione crittografata.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-211">If set to **TRUE**, **RequiresEncryption** marks a namespace so that client applications and scripts must connect with encrypted authentication.</span></span> <span data-ttu-id="0d2aa-212">Il livello di autenticazione deve essere impostato **su \_ \_ \_ \_ PKT \_ privacy a livello** di autenticazione di RPC C in C++.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-212">The authentication level must be set to **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY** in C++.</span></span> <span data-ttu-id="0d2aa-213">Nel Visual Basic di scripting, il livello di autenticazione deve essere impostato su **WbemAuthenticationLevelPktPrivacy**.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-213">In scripting or Visual Basic, authentication level must be set to **WbemAuthenticationLevelPktPrivacy**.</span></span> <span data-ttu-id="0d2aa-214">Per altre informazioni, vedere [impostazione dei descrittori di sicurezza spazio dei nomi](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="0d2aa-214">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span> <span data-ttu-id="0d2aa-215">Il qualificatore viene usato in [*MOF*](gloss-m.md) con il comando del preprocessore dello spazio dei nomi pragma.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-215">The qualifier is used in [*MOF*](gloss-m.md) with the pragma namespace preprocessor command.</span></span>

<span data-ttu-id="0d2aa-216">Per altre informazioni, vedere [impostazione del livello di sicurezza del processo predefinito con C++](setting-the-default-process-security-level-using-c-.md) o [impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="0d2aa-216">For more information, see [Setting the Default Process Security Level Using C++](setting-the-default-process-security-level-using-c-.md) or [Setting the Default Process Security Level Using VBScript](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="0d2aa-217">I livelli di autenticazione di scripting sono definiti in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span><span class="sxs-lookup"><span data-stu-id="0d2aa-217">Scripting authentication levels are defined in [**WbemAuthenticationLevelEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum).</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-218"><span id="Singleton"></span><span id="singleton"></span><span id="SINGLETON"></span>**Singleton**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-219">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-219">Data type: **boolean**</span></span>

<span data-ttu-id="0d2aa-220">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-220">Applies to: classes</span></span>

<span data-ttu-id="0d2aa-221">Definisce una classe che può avere una sola istanza e che non contiene proprietà chiave.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-221">Designates a class that can only have one instance and that does not contain key properties.</span></span>

<span data-ttu-id="0d2aa-222">È consentito solo il valore **true** (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="0d2aa-222">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Statico**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-223"><span id="Static"></span><span id="static"></span><span id="STATIC"></span>**Static**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-224">Tipo di dati: **Boolean**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-224">Data type: **boolean**</span></span>

<span data-ttu-id="0d2aa-225">Si applica a: metodi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-225">Applies to: methods</span></span>

<span data-ttu-id="0d2aa-226">Indica se un metodo può essere chiamato utilizzando la definizione della classe o le relative istanze.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-226">Indicates whether a method can called by using the class definition or its instances.</span></span>

<span data-ttu-id="0d2aa-227">Il metodo non può essere richiamato da un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-227">The method cannot be invoked from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**Sottotipo**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-228"><span id="SubType"></span><span id="subtype"></span><span id="SUBTYPE"></span>**SubType**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-229">Tipo di dati: **VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-229">Data type: **VT\_BSTR**</span></span>

<span data-ttu-id="0d2aa-230">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d2aa-230">Applies to: properties</span></span>

<span data-ttu-id="0d2aa-231">Indica che una proprietà di tipo **CIM \_ DateTime** rappresenta un intervallo di tempo anziché un'ora specifica.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-231">Indicates that a property of type **CIM\_DATETIME** represents a time interval rather than a specific time.</span></span>

<span data-ttu-id="0d2aa-232">Per identificare la proprietà come intervallo, il valore di questo qualificatore deve essere "Interval".</span><span class="sxs-lookup"><span data-stu-id="0d2aa-232">To identify the property as an interval, the value of this qualifier must be "interval".</span></span> <span data-ttu-id="0d2aa-233">Tutti gli altri valori per questo qualificatore sono riservati per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-233">All other values for this qualifier are reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-234"><span id="UUID"></span><span id="uuid"></span>**UUID**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-234"><span id="UUID"></span><span id="uuid"></span>**UUID**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-235">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-235">Data type: **string**</span></span>

<span data-ttu-id="0d2aa-236">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-236">Applies to: classes</span></span>

<span data-ttu-id="0d2aa-237">Identificatore univoco universale applicato alla classe.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-237">Universally unique identifier applied to the class.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-238"><span id="ClassVersion"></span><span id="classversion"></span><span id="CLASSVERSION"></span>**ClassVersion**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-239">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-239">Data type: **string**</span></span>

<span data-ttu-id="0d2aa-240">Si applica a: classi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-240">Applies to: classes</span></span>

<span data-ttu-id="0d2aa-241">Numero di versione dell'oggetto classe.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-241">The version number of the class object.</span></span> <span data-ttu-id="0d2aa-242">Il valore predefinito è **null**.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-242">The default is **NULL**.</span></span> <span data-ttu-id="0d2aa-243">Il numero di versione viene incrementato quando vengono apportate modifiche alla classe.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-243">The version number is incremented when changes are made to the class.</span></span>

</dd> <dt>

<span data-ttu-id="0d2aa-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-244"><span id="WritePrivileges"></span><span id="writeprivileges"></span><span id="WRITEPRIVILEGES"></span>**WritePrivileges**</span></span>
</dt> <dd>

<span data-ttu-id="0d2aa-245">Tipo di dati: **matrice di stringhe**</span><span class="sxs-lookup"><span data-stu-id="0d2aa-245">Data type: **string array**</span></span>

<span data-ttu-id="0d2aa-246">Si applica a: Proprietà</span><span class="sxs-lookup"><span data-stu-id="0d2aa-246">Applies to: properties</span></span>

<span data-ttu-id="0d2aa-247">Set di valori che indica quali privilegi di sistema devono essere disponibili e abilitati per un'operazione di scrittura corretta.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-247">Set of values indicating which system privileges must be available and enabled for a successful write operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0d2aa-248">Commenti</span><span class="sxs-lookup"><span data-stu-id="0d2aa-248">Remarks</span></span>

### <a name="locale-codes"></a><span data-ttu-id="0d2aa-249">Codici delle impostazioni locali</span><span class="sxs-lookup"><span data-stu-id="0d2aa-249">Locale Codes</span></span>

<span data-ttu-id="0d2aa-250">Il formato di un codice delle impostazioni locali è "MS \_ <Three Digit Language ID> ".</span><span class="sxs-lookup"><span data-stu-id="0d2aa-250">A locale code is of the form "MS\_<Three Digit Language ID>".</span></span> <span data-ttu-id="0d2aa-251">Ad esempio, le impostazioni locali inglesi sono MS \_ 409.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-251">For example, English locale is MS\_409.</span></span> <span data-ttu-id="0d2aa-252">Nella tabella seguente sono elencati gli ID della lingua.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-252">The following table lists the language IDs.</span></span>



| <span data-ttu-id="0d2aa-253">Linguaggio</span><span class="sxs-lookup"><span data-stu-id="0d2aa-253">Language</span></span>              | <span data-ttu-id="0d2aa-254">ID lingua (esadecimale)</span><span class="sxs-lookup"><span data-stu-id="0d2aa-254">Language ID (hexadecimal)</span></span> |
|-----------------------|---------------------------|
| <span data-ttu-id="0d2aa-255">Arabo</span><span class="sxs-lookup"><span data-stu-id="0d2aa-255">Arabic</span></span>                | <span data-ttu-id="0d2aa-256">401</span><span class="sxs-lookup"><span data-stu-id="0d2aa-256">401</span></span>                       |
| <span data-ttu-id="0d2aa-257">Portoghese (Brasile)</span><span class="sxs-lookup"><span data-stu-id="0d2aa-257">Portuguese (Brazil)</span></span>   | <span data-ttu-id="0d2aa-258">416</span><span class="sxs-lookup"><span data-stu-id="0d2aa-258">416</span></span>                       |
| <span data-ttu-id="0d2aa-259">Cinese (semplificato)</span><span class="sxs-lookup"><span data-stu-id="0d2aa-259">Chinese (Simplified)</span></span>  | <span data-ttu-id="0d2aa-260">804</span><span class="sxs-lookup"><span data-stu-id="0d2aa-260">804</span></span>                       |
| <span data-ttu-id="0d2aa-261">Cinese (tradizionale)</span><span class="sxs-lookup"><span data-stu-id="0d2aa-261">Chinese (Traditional)</span></span> | <span data-ttu-id="0d2aa-262">404</span><span class="sxs-lookup"><span data-stu-id="0d2aa-262">404</span></span>                       |
| <span data-ttu-id="0d2aa-263">Ceco</span><span class="sxs-lookup"><span data-stu-id="0d2aa-263">Czech</span></span>                 | <span data-ttu-id="0d2aa-264">405</span><span class="sxs-lookup"><span data-stu-id="0d2aa-264">405</span></span>                       |
| <span data-ttu-id="0d2aa-265">Danese</span><span class="sxs-lookup"><span data-stu-id="0d2aa-265">Danish</span></span>                | <span data-ttu-id="0d2aa-266">406</span><span class="sxs-lookup"><span data-stu-id="0d2aa-266">406</span></span>                       |
| <span data-ttu-id="0d2aa-267">Olandese</span><span class="sxs-lookup"><span data-stu-id="0d2aa-267">Dutch</span></span>                 | <span data-ttu-id="0d2aa-268">413</span><span class="sxs-lookup"><span data-stu-id="0d2aa-268">413</span></span>                       |
| <span data-ttu-id="0d2aa-269">Inglese (predefinito)</span><span class="sxs-lookup"><span data-stu-id="0d2aa-269">English (default)</span></span>     | <span data-ttu-id="0d2aa-270">409</span><span class="sxs-lookup"><span data-stu-id="0d2aa-270">409</span></span>                       |
| <span data-ttu-id="0d2aa-271">Finlandese</span><span class="sxs-lookup"><span data-stu-id="0d2aa-271">Finnish</span></span>               | <span data-ttu-id="0d2aa-272">40B</span><span class="sxs-lookup"><span data-stu-id="0d2aa-272">40b</span></span>                       |
| <span data-ttu-id="0d2aa-273">Francese</span><span class="sxs-lookup"><span data-stu-id="0d2aa-273">French</span></span>                | <span data-ttu-id="0d2aa-274">40C</span><span class="sxs-lookup"><span data-stu-id="0d2aa-274">40c</span></span>                       |
| <span data-ttu-id="0d2aa-275">Tedesco</span><span class="sxs-lookup"><span data-stu-id="0d2aa-275">German</span></span>                | <span data-ttu-id="0d2aa-276">407</span><span class="sxs-lookup"><span data-stu-id="0d2aa-276">407</span></span>                       |
| <span data-ttu-id="0d2aa-277">Greco</span><span class="sxs-lookup"><span data-stu-id="0d2aa-277">Greek</span></span>                 | <span data-ttu-id="0d2aa-278">408</span><span class="sxs-lookup"><span data-stu-id="0d2aa-278">408</span></span>                       |
| <span data-ttu-id="0d2aa-279">Ebraico</span><span class="sxs-lookup"><span data-stu-id="0d2aa-279">Hebrew</span></span>                | <span data-ttu-id="0d2aa-280">40D</span><span class="sxs-lookup"><span data-stu-id="0d2aa-280">40d</span></span>                       |
| <span data-ttu-id="0d2aa-281">Ungherese</span><span class="sxs-lookup"><span data-stu-id="0d2aa-281">Hungarian</span></span>             | <span data-ttu-id="0d2aa-282">40E</span><span class="sxs-lookup"><span data-stu-id="0d2aa-282">40e</span></span>                       |
| <span data-ttu-id="0d2aa-283">Italiano</span><span class="sxs-lookup"><span data-stu-id="0d2aa-283">Italian</span></span>               | <span data-ttu-id="0d2aa-284">410</span><span class="sxs-lookup"><span data-stu-id="0d2aa-284">410</span></span>                       |
| <span data-ttu-id="0d2aa-285">Giapponese</span><span class="sxs-lookup"><span data-stu-id="0d2aa-285">Japanese</span></span>              | <span data-ttu-id="0d2aa-286">411</span><span class="sxs-lookup"><span data-stu-id="0d2aa-286">411</span></span>                       |
| <span data-ttu-id="0d2aa-287">Coreano</span><span class="sxs-lookup"><span data-stu-id="0d2aa-287">Korean</span></span>                | <span data-ttu-id="0d2aa-288">412</span><span class="sxs-lookup"><span data-stu-id="0d2aa-288">412</span></span>                       |
| <span data-ttu-id="0d2aa-289">Norvegese</span><span class="sxs-lookup"><span data-stu-id="0d2aa-289">Norwegian</span></span>             | <span data-ttu-id="0d2aa-290">414</span><span class="sxs-lookup"><span data-stu-id="0d2aa-290">414</span></span>                       |
| <span data-ttu-id="0d2aa-291">Polacco</span><span class="sxs-lookup"><span data-stu-id="0d2aa-291">Polish</span></span>                | <span data-ttu-id="0d2aa-292">415</span><span class="sxs-lookup"><span data-stu-id="0d2aa-292">415</span></span>                       |
| <span data-ttu-id="0d2aa-293">Portoghese (Portogallo)</span><span class="sxs-lookup"><span data-stu-id="0d2aa-293">Portuguese (Portugal)</span></span> | <span data-ttu-id="0d2aa-294">816</span><span class="sxs-lookup"><span data-stu-id="0d2aa-294">816</span></span>                       |
| <span data-ttu-id="0d2aa-295">Russo</span><span class="sxs-lookup"><span data-stu-id="0d2aa-295">Russian</span></span>               | <span data-ttu-id="0d2aa-296">419</span><span class="sxs-lookup"><span data-stu-id="0d2aa-296">419</span></span>                       |
| <span data-ttu-id="0d2aa-297">Spagnolo</span><span class="sxs-lookup"><span data-stu-id="0d2aa-297">Spanish</span></span>               | <span data-ttu-id="0d2aa-298">c0a</span><span class="sxs-lookup"><span data-stu-id="0d2aa-298">c0a</span></span>                       |
| <span data-ttu-id="0d2aa-299">Svedese</span><span class="sxs-lookup"><span data-stu-id="0d2aa-299">Swedish</span></span>               | <span data-ttu-id="0d2aa-300">41 quinquies</span><span class="sxs-lookup"><span data-stu-id="0d2aa-300">41D</span></span>                       |
| <span data-ttu-id="0d2aa-301">Turco</span><span class="sxs-lookup"><span data-stu-id="0d2aa-301">Turkish</span></span>               | <span data-ttu-id="0d2aa-302">41F</span><span class="sxs-lookup"><span data-stu-id="0d2aa-302">41f</span></span>                       |



 

### <a name="using-the-bypass_getobject-qualifier"></a><span data-ttu-id="0d2aa-303">Uso del \_ qualificatore GetObject di bypass</span><span class="sxs-lookup"><span data-stu-id="0d2aa-303">Using the Bypass\_GetObject Qualifier</span></span>

<span data-ttu-id="0d2aa-304">L'uso del qualificatore **\_ GetObject di bypass** su un metodo può produrre risultati confusi.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-304">Using the **Bypass\_GetObject** qualifier on a method can produce confusing results.</span></span>

<span data-ttu-id="0d2aa-305">Nell'esempio seguente vengono definite le classi **Shape** e **Circle** .</span><span class="sxs-lookup"><span data-stu-id="0d2aa-305">The following example defines the **Shape** and **Circle** classes.</span></span> <span data-ttu-id="0d2aa-306">Si noti che la classe **Circle** è derivata dalla classe **Shape** .</span><span class="sxs-lookup"><span data-stu-id="0d2aa-306">Note that the **Circle** class is derived from the **Shape** class.</span></span>


```VB
class Shape
{
   string Name;
   uint32 DrawIt();  // - draws an irregular geometric shape
};

class Circle : Shape
{
   uint32 DrawIt();  // - draws a circle
};
```



<span data-ttu-id="0d2aa-307">La chiamata seguente a **ExecMethod** usa un oggetto **Circle** denominato "tocircle" per creare un cerchio.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-307">The following call to **ExecMethod** uses a **Circle** object named "MyCircle" to draw a circle.</span></span>


```VB
ExecMethod("Shape.Name='MyCircle'","DrawIt");
```



<span data-ttu-id="0d2aa-308">Nello scenario precedente, WMI chiama **GetObject**; rileva che "Shape. Name =' il cerchio '" è un **cerchio**; ed esegue l'implementazione **Circle** di **drawit**.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-308">In the previous scenario, WMI calls **GetObject**; discovers that "Shape.Name='MyCircle'" is a **Circle**; and executes the **Circle** implementation of **DrawIt**.</span></span> <span data-ttu-id="0d2aa-309">Tuttavia, se si usa il qualificatore **\_ GetObject di bypass** in **drawit**, WMI non chiama **GetObject**, non rileva che "Shape. Name =' il cerchio '" è un **cerchio** ed esegue l'implementazione della **forma** di **drawit** invece dell'implementazione del **cerchio** di **drawit**.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-309">However, if you use the **Bypass\_GetObject** qualifier on **DrawIt**, WMI does not call **GetObject**, does not discover that "Shape.Name='MyCircle'" is a **Circle**, and executes the **Shape** implementation of **DrawIt** instead of the **Circle** implementation of **DrawIt**.</span></span>

<span data-ttu-id="0d2aa-310">La chiamata seguente a **ExecMethod** richiama sempre l'implementazione corretta di **drawit**.</span><span class="sxs-lookup"><span data-stu-id="0d2aa-310">The following call to **ExecMethod** always invokes the correct implementation of **DrawIt**.</span></span>


```VB
ExecMethod("Circle.Name='MyCircle'","DrawIt");
```



## <a name="requirements"></a><span data-ttu-id="0d2aa-311">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0d2aa-311">Requirements</span></span>



| <span data-ttu-id="0d2aa-312">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d2aa-312">Requirement</span></span> | <span data-ttu-id="0d2aa-313">Valore</span><span class="sxs-lookup"><span data-stu-id="0d2aa-313">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0d2aa-314">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d2aa-314">Minimum supported client</span></span><br/> | <span data-ttu-id="0d2aa-315">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d2aa-315">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0d2aa-316">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0d2aa-316">Minimum supported server</span></span><br/> | <span data-ttu-id="0d2aa-317">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d2aa-317">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d2aa-318">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0d2aa-318">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d2aa-319">Impostazione di descrittori di sicurezza spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="0d2aa-319">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="0d2aa-320">Qualificatori WMI</span><span class="sxs-lookup"><span data-stu-id="0d2aa-320">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="0d2aa-321">Aggiunta di un qualificatore</span><span class="sxs-lookup"><span data-stu-id="0d2aa-321">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

