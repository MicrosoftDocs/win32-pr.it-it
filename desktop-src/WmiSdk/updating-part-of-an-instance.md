---
description: Occasionalmente, potrebbe essere necessario aggiornare solo parte di un'istanza.
ms.assetid: c92bf8f9-9cac-4cf0-a45d-f60aee5a9ec2
ms.tgt_platform: multiple
title: Aggiornamento di una parte di un'istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eaf58bfc151358a2b4f282815769d1b19c068f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309757"
---
# <a name="updating-part-of-an-instance"></a><span data-ttu-id="00863-103">Aggiornamento di una parte di un'istanza</span><span class="sxs-lookup"><span data-stu-id="00863-103">Updating Part of an Instance</span></span>

<span data-ttu-id="00863-104">Occasionalmente, potrebbe essere necessario aggiornare solo parte di un'istanza.</span><span class="sxs-lookup"><span data-stu-id="00863-104">Occasionally, you may want to update only part of an instance.</span></span> <span data-ttu-id="00863-105">Ad esempio, alcune istanze hanno un numero elevato di proprietà.</span><span class="sxs-lookup"><span data-stu-id="00863-105">For example, some instances have a large number of properties.</span></span> <span data-ttu-id="00863-106">Se è necessario aggiornare un numero elevato di istanze, è possibile ridurre le prestazioni del sistema.</span><span class="sxs-lookup"><span data-stu-id="00863-106">If you had to update a large number of these instances, you may reduce system performance.</span></span> <span data-ttu-id="00863-107">Pertanto, è possibile scegliere di aggiornare solo una parte dell'istanza di e quindi ridurre la quantità di informazioni che è necessario inviare e recuperare da e in WMI.</span><span class="sxs-lookup"><span data-stu-id="00863-107">Therefore, you can choose to update only part of the instance, and thus reduce the amount of information you must send and retrieve to and from WMI.</span></span> <span data-ttu-id="00863-108">Tuttavia, WMI non supporta direttamente le operazioni di istanza parziale, né la maggior parte dei provider.</span><span class="sxs-lookup"><span data-stu-id="00863-108">However, WMI does not directly support partial-instance operations, nor do most providers.</span></span> <span data-ttu-id="00863-109">Pertanto, se si scrive un'applicazione che usa operazioni a istanza parziale, prepararsi per le chiamate a non riuscire con **il \_ provider WBEM e \_ \_ non \_ in grado** di supportare il codice di errore **WBEM \_ e \_ non \_ supportato** in C++.</span><span class="sxs-lookup"><span data-stu-id="00863-109">Therefore, if you write an application that uses partial-instance operations, be prepared for your calls to fail with either the **WBEM\_E\_PROVIDER\_NOT\_CAPABLE** or **WBEM\_E\_NOT\_SUPPORTED** error code in C++.</span></span> <span data-ttu-id="00863-110">Nei linguaggi di scripting i codici di errore sono **wbemErrProviderNotCapable** o **wbemErrNotSupported**.</span><span class="sxs-lookup"><span data-stu-id="00863-110">In scripting languages the error codes are either **wbemErrProviderNotCapable** or **wbemErrNotSupported**.</span></span>

<span data-ttu-id="00863-111">Nello scripting questa operazione è necessaria solo per aiutare le prestazioni quando si aggiornano una o due proprietà scrivibili in un numero molto elevato di oggetti in un'organizzazione.</span><span class="sxs-lookup"><span data-stu-id="00863-111">In scripting, this operation is only necessary to aid performance when updating one or two writeable properties in a very large number of objects over an enterprise.</span></span> <span data-ttu-id="00863-112">In caso contrario, le normali chiamate VBScript a [**SWbemObject \_ . Put**](swbemobject-put-.md) o [**SWbemObject \_ . PutAsync**](swbemobject-putasync-.md), mentre sembrano scrivere l'intero oggetto, aggiornano in realtà solo le proprietà che il provider ha abilitato per la scrittura.</span><span class="sxs-lookup"><span data-stu-id="00863-112">Otherwise, the normal VBScript calls to [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md), while seeming to write the entire object, are actually only updating the properties which the provider has write-enabled.</span></span>

<span data-ttu-id="00863-113">Nella procedura seguente viene descritto come richiedere un aggiornamento parziale dell'istanza tramite PowerShell.</span><span class="sxs-lookup"><span data-stu-id="00863-113">The following procedure describes how to request a partial-instance update using PowerShell.</span></span>

<span data-ttu-id="00863-114">**Per richiedere un aggiornamento parziale dell'istanza tramite PowerShell**</span><span class="sxs-lookup"><span data-stu-id="00863-114">**To request a partial-instance update using PowerShell**</span></span>

1.  <span data-ttu-id="00863-115">Recuperare il percorso dell'oggetto che si desidera aggiornare.</span><span class="sxs-lookup"><span data-stu-id="00863-115">Retrieve the path of the object you wish to update.</span></span>

    <span data-ttu-id="00863-116">È possibile descrivere il percorso manualmente, altrimenti eseguire una query sull'oggetto e recuperare la proprietà **\_ \_ path** .</span><span class="sxs-lookup"><span data-stu-id="00863-116">You can describe the path either manually, or else query the object and then retrieve the **\_\_Path** property.</span></span>

    ```PowerShell
    $myWMIDrivePath = (get-wmiObject Win32_LogicalDisk -filter "Name = 'C:'").__Path
    #or
    $myWmiDrivePath = \\myComputer\root\cimv2:Win32_LogicalDisk.DeviceID="C:"
    ```

    

2.  <span data-ttu-id="00863-117">Configurare una tabella hash che elenca i nomi delle proprietà da aggiornare e usare questa tabella hash in una chiamata a [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="00863-117">Set up a hash table listing the names of the properties to be updated, and use this hash table in a call to [Set-WmiInstance](/powershell/module/microsoft.powershell.management/set-wmiinstance?view=powershell-5.1&preserve-view=true).</span></span>

    ```PowerShell
    $newDriveName = @{VolumeName = "OSDisk"}
    Set-WmiInstance -Path $myWMIDrivePath -Arguments $newDriveName
    ```

    

<span data-ttu-id="00863-118">Nella procedura seguente viene descritto come richiedere un aggiornamento parziale dell'istanza tramite C#.</span><span class="sxs-lookup"><span data-stu-id="00863-118">The following procedure describes how to request a partial-instance update using C#.</span></span>

> [!Note]  
> <span data-ttu-id="00863-119">**System. Management** era lo spazio dei nomi .NET originale utilizzato per accedere a WMI. Tuttavia, le API in questo spazio dei nomi sono in genere più lente e non vengono ridimensionate rispetto alle controparti **Microsoft. Management. Infrastructure** più moderne.</span><span class="sxs-lookup"><span data-stu-id="00863-119">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="00863-120">**Per richiedere un aggiornamento parziale dell'istanza tramite C #**</span><span class="sxs-lookup"><span data-stu-id="00863-120">**To request a partial-instance update using C#**</span></span>

1.  <span data-ttu-id="00863-121">Creare un nuovo oggetto [ManagementObject](/dotnet/api/system.management.managementobject) che rappresenta l'istanza specifica da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="00863-121">Create a new [ManagementObject](/dotnet/api/system.management.managementobject) object that represents the specific instance to update.</span></span>

    ```PowerShell
    using System.Management;
    ...
    ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
    ```

    

2.  <span data-ttu-id="00863-122">Impostare il valore della proprietà con una chiamata a [ManagementObject. sepropertyvalue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).</span><span class="sxs-lookup"><span data-stu-id="00863-122">Set the property value with a call to [ManagementObject.SetPropertyValue](/dotnet/api/system.management.managementbaseobject.setpropertyvalue#System_Management_ManagementBaseObject_SetPropertyValue_System_String_System_Object_).</span></span>

    ```CSharp
    myDisk.SetPropertyValue("VolumeName", "OSDisk");
    ```

    

<span data-ttu-id="00863-123">Nella procedura seguente viene descritto come richiedere un aggiornamento parziale dell'istanza tramite VBScript.</span><span class="sxs-lookup"><span data-stu-id="00863-123">The following procedure describes how to request a partial-instance update using VBScript.</span></span>

<span data-ttu-id="00863-124">**Per richiedere un aggiornamento parziale dell'istanza tramite VBScript**</span><span class="sxs-lookup"><span data-stu-id="00863-124">**To request a partial-instance update using VBScript**</span></span>

1.  <span data-ttu-id="00863-125">Creare un oggetto contesto [**SWbemNamedValueSet**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="00863-125">Create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object.</span></span>

    ```VB
    Set objwbemNamedValueSet = CreateObject ("WbemScripting.SWbemNamedValueSet")
    ```

    

2.  <span data-ttu-id="00863-126">Aggiungere i valori di estensione PUT " \_ \_ put \_ Extensions" e " \_ \_ put \_ ext \_ client \_ Request" all'oggetto context usando il metodo [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) .</span><span class="sxs-lookup"><span data-stu-id="00863-126">Add the Put extension values "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" to the context object using the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method.</span></span>

    ```VB
    objwbemNamedValueSet.Add "__PUT_EXTENSIONS", True
    objwbemNamedValueSet.Add "__PUT_EXT_CLIENT_REQUEST", True
    ```

    

3.  <span data-ttu-id="00863-127">Configurare una matrice in cui sono elencati i nomi delle proprietà da aggiornare e aggiungere questa matrice all'oggetto contesto [**SWbemNamedValueSet**](swbemnamedvalueset.md) con il valore di estensione PUT " \_ \_ put \_ ext \_ Properties".</span><span class="sxs-lookup"><span data-stu-id="00863-127">Set up an array listing the names of the properties to be updated and add this array to the [**SWbemNamedValueSet**](swbemnamedvalueset.md) context object with the Put extension value "\_\_PUT\_EXT\_PROPERTIES".</span></span>

    ```VB
    arProperties = Array("propertyname1", "propertyname2") 
    objwbemNamedValueSet.Add "__PUT_EXT_PROPERTIES", arProperties
    ```

    

4.  <span data-ttu-id="00863-128">Impostare il parametro *iFlags* della chiamata [**SWbemObject. put \_**](swbemobject-put-.md) su **wbemChangeFlagUpdateOnly**.</span><span class="sxs-lookup"><span data-stu-id="00863-128">Set the *iFlags* parameter of the [**SWbemObject.Put\_**](swbemobject-put-.md) call to **wbemChangeFlagUpdateOnly**.</span></span> <span data-ttu-id="00863-129">Senza questo flag la chiamata avrà esito negativo con un contesto non valido.</span><span class="sxs-lookup"><span data-stu-id="00863-129">Without this flag the call will fail with an invalid context.</span></span>

5.  <span data-ttu-id="00863-130">Passare il flag e l'oggetto di contesto al provider nel parametro *objwbemNamedValueSet* di [**SWbemObject. put \_**](swbemobject-put-.md) o [**SWbemObject. PutAsync \_**](swbemobject-putasync-.md).</span><span class="sxs-lookup"><span data-stu-id="00863-130">Pass your flag and context object to the provider in the *objwbemNamedValueSet* parameter of either [**SWbemObject.Put\_**](swbemobject-put-.md) or [**SWbemObject.PutAsync\_**](swbemobject-putasync-.md).</span></span>

    ```VB
    call objSystem.put_( wbemChangeFlagUpdateOnly, objwbemNamedValueSet)
    ```

    

<span data-ttu-id="00863-131">Nella procedura riportata di seguito viene descritto come richiedere un aggiornamento parziale dell'istanza mediante C++.</span><span class="sxs-lookup"><span data-stu-id="00863-131">The following procedure describes how to request a partial-instance update using C++.</span></span>

<span data-ttu-id="00863-132">**Per richiedere un aggiornamento parziale dell'istanza con C++**</span><span class="sxs-lookup"><span data-stu-id="00863-132">**To request a partial-instance update using C++**</span></span>

1.  <span data-ttu-id="00863-133">Creare un oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con una chiamata a [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="00863-133">Create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="00863-134">Un oggetto context è un oggetto utilizzato da WMI per passare ulteriori informazioni a un provider WMI.</span><span class="sxs-lookup"><span data-stu-id="00863-134">A context object is an object that WMI uses to pass in more information to a WMI provider.</span></span> <span data-ttu-id="00863-135">In questo caso, si usa l'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) per indicare al provider di accettare gli aggiornamenti parziali dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="00863-135">In this case, you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object to instruct the provider to accept partial-instance updates.</span></span>

2.  <span data-ttu-id="00863-136">Aggiungere i \_ \_ \_ valori denominati "put Extensions" e " \_ \_ put \_ ext \_ client \_ Request" all'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con una chiamata a [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span><span class="sxs-lookup"><span data-stu-id="00863-136">Add the "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST" named values to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="00863-137">La tabella seguente elenca il significato di " \_ \_ put \_ Extensions" e " \_ \_ put \_ ext \_ client \_ Request".</span><span class="sxs-lookup"><span data-stu-id="00863-137">The following table lists the meaning of "\_\_PUT\_EXTENSIONS" and "\_\_PUT\_EXT\_CLIENT\_REQUEST".</span></span>

    

    | <span data-ttu-id="00863-138">Valore denominato</span><span class="sxs-lookup"><span data-stu-id="00863-138">Named value</span></span>                     | <span data-ttu-id="00863-139">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00863-139">Description</span></span>                                                                                                                                                                                                                                             |
    |---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="00863-140">" \_ \_ Inserisci \_ estensioni"</span><span class="sxs-lookup"><span data-stu-id="00863-140">"\_\_PUT\_EXTENSIONS"</span></span>           | <span data-ttu-id="00863-141">**VT \_ BOOL** impostato su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="00863-141">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="00863-142">Valore che indica che sono stati specificati uno o più valori di contesto.</span><span class="sxs-lookup"><span data-stu-id="00863-142">A value indicating that one or more of the other context values has been specified.</span></span> <span data-ttu-id="00863-143">Questo consente un rapido controllo dell'oggetto contesto all'interno del provider per determinare se vengono utilizzati gli aggiornamenti parziali dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="00863-143">This allows a quick check of the context object inside the provider to determine if partial-instance updates are being used.</span></span> |
    | <span data-ttu-id="00863-144">" \_ \_ Inserisci \_ \_ richiesta client ext \_ "</span><span class="sxs-lookup"><span data-stu-id="00863-144">"\_\_PUT\_EXT\_CLIENT\_REQUEST"</span></span> | <span data-ttu-id="00863-145">**VT \_ BOOL** impostato su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="00863-145">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="00863-146">Impostato dal client durante la richiesta iniziale.</span><span class="sxs-lookup"><span data-stu-id="00863-146">Set by the client during the initial request.</span></span> <span data-ttu-id="00863-147">Questo valore viene utilizzato per evitare errori di rientranza.</span><span class="sxs-lookup"><span data-stu-id="00863-147">This value is used to prevent reentrancy errors.</span></span>                                                                                                                   |

    

     

3.  <span data-ttu-id="00863-148">Aggiungere le \_ \_ \_ proprietà put ext \_ strict \_ null, \_ \_ put \_ ext \_ Properties o \_ \_ put \_ ext \_ Atomic in qualsiasi combinazione, in base alle esigenze, all'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) con un'altra chiamata a [**IWbemContext:: SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span><span class="sxs-lookup"><span data-stu-id="00863-148">Add the \_\_PUT\_EXT\_STRICT\_NULLS, \_\_PUT\_EXT\_PROPERTIES, or \_\_PUT\_EXT\_ATOMIC in any combination as needed to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with another call to [**IWbemContext::SetValue**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemcontext-setvalue).</span></span>

    <span data-ttu-id="00863-149">Nella tabella seguente viene elencato il significato dei valori denominati.</span><span class="sxs-lookup"><span data-stu-id="00863-149">The following table lists the meaning of the named values.</span></span>

    

    | <span data-ttu-id="00863-150">Valore denominato</span><span class="sxs-lookup"><span data-stu-id="00863-150">Named value</span></span>                   | <span data-ttu-id="00863-151">Descrizione</span><span class="sxs-lookup"><span data-stu-id="00863-151">Description</span></span>                                                                                                                                                                                                                                   |
    |-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="00863-152">" \_ \_ put \_ ext \_ strict \_ nulls"</span><span class="sxs-lookup"><span data-stu-id="00863-152">"\_\_PUT\_EXT\_STRICT\_NULLS"</span></span> | <span data-ttu-id="00863-153">**VT \_ BOOL** impostato su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="00863-153">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="00863-154">Indica che il client ha intenzionalmente impostato le proprietà su **VT \_ null** e prevede che l'operazione di scrittura abbia esito positivo.</span><span class="sxs-lookup"><span data-stu-id="00863-154">Indicates that the client has intentionally set properties to **VT\_NULL** and expects the write operation to succeed.</span></span> <span data-ttu-id="00863-155">Se il provider non è in grado di impostare i valori su **null**, è necessario segnalare un errore.</span><span class="sxs-lookup"><span data-stu-id="00863-155">If the provider cannot set the values to **NULL**, an error should be reported.</span></span> |
    | <span data-ttu-id="00863-156">" \_ \_ put \_ ext \_ Properties"</span><span class="sxs-lookup"><span data-stu-id="00863-156">"\_\_PUT\_EXT\_PROPERTIES"</span></span>    | <span data-ttu-id="00863-157">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) di stringhe contenente un elenco di nomi di proprietà da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="00863-157">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of strings containing a list of property names to be updated.</span></span> <span data-ttu-id="00863-158">Può essere usato da solo o in combinazione con " \_ \_ put \_ ext \_ Properties".</span><span class="sxs-lookup"><span data-stu-id="00863-158">May be used alone or in combination with "\_\_PUT\_EXT\_PROPERTIES".</span></span> <span data-ttu-id="00863-159">I valori si trovano nell'istanza di in fase di scrittura.</span><span class="sxs-lookup"><span data-stu-id="00863-159">The values are in the instance being written.</span></span>                           |
    | <span data-ttu-id="00863-160">" \_ \_ put \_ ext \_ Atomic"</span><span class="sxs-lookup"><span data-stu-id="00863-160">"\_\_PUT\_EXT\_ATOMIC"</span></span>        | <span data-ttu-id="00863-161">**VT \_ BOOL** impostato su **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="00863-161">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="00863-162">Indica che tutti gli aggiornamenti devono avere esito positivo simultaneo (semantica atomica) o che il provider deve essere ripristinato.</span><span class="sxs-lookup"><span data-stu-id="00863-162">Indicates that all updates must succeed simultaneously (atomic semantics) or the provider must revert back.</span></span> <span data-ttu-id="00863-163">Non è possibile avere esito positivo parziale.</span><span class="sxs-lookup"><span data-stu-id="00863-163">There can be no partial success.</span></span> <span data-ttu-id="00863-164">Può essere usato da solo o in combinazione con altri flag.</span><span class="sxs-lookup"><span data-stu-id="00863-164">May be used alone or in combination with other flags.</span></span>     |

    

     

4.  <span data-ttu-id="00863-165">Impostare il parametro *iFlags* solo per l' **\_ \_ aggiornamento \_ del flag WBEM**.</span><span class="sxs-lookup"><span data-stu-id="00863-165">Set the *iFlags* parameter to **WBEM\_FLAG\_UPDATE\_ONLY**.</span></span> <span data-ttu-id="00863-166">Senza questo flag la chiamata avrà esito negativo con un contesto non valido.</span><span class="sxs-lookup"><span data-stu-id="00863-166">Without this flag the call will fail with an invalid context.</span></span>
5.  <span data-ttu-id="00863-167">Passare l'oggetto contesto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) in qualsiasi chiamata [**IWbemServices::P utinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) o [**IWbemServices::P utinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) nel parametro *pctX* .</span><span class="sxs-lookup"><span data-stu-id="00863-167">Pass the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) context object into any calls [**IWbemServices::PutInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance) or [**IWbemServices::PutInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync) in the *pCtx* parameter.</span></span>

    <span data-ttu-id="00863-168">Il passaggio dell'oggetto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) indica al provider di consentire aggiornamenti parziali dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="00863-168">Passing the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object instructs the provider to allow partial-instance updates.</span></span> <span data-ttu-id="00863-169">In un aggiornamento dell'istanza completa, è necessario impostare *pctX* su **null**.</span><span class="sxs-lookup"><span data-stu-id="00863-169">In a full-instance update, you would set *pCtx* to **NULL**.</span></span>

    <span data-ttu-id="00863-170">Il provider può scrivere eventuali proprietà necessarie se l'oggetto contesto presente nella chiamata non contiene " \_ \_ put \_ Extensions".</span><span class="sxs-lookup"><span data-stu-id="00863-170">The provider may write any necessary properties if the context object present in the call does not contain "\_\_PUT\_EXTENSIONS".</span></span> <span data-ttu-id="00863-171">Se \_ \_ \_ nell'oggetto context è presente "put Extensions", per WMI è necessario che il provider rispetti la semantica dell'operazione in modo esatto. in caso contrario, la chiamata non riesce.</span><span class="sxs-lookup"><span data-stu-id="00863-171">If "\_\_PUT\_EXTENSIONS" is present in the context object, WMI requires the provider to either obey the semantics of the operation exactly or else fail the call.</span></span> <span data-ttu-id="00863-172">Per ulteriori informazioni, vedere [gestione dei messaggi di accesso negato in un provider](impersonating-a-client.md).</span><span class="sxs-lookup"><span data-stu-id="00863-172">For more information, see [Handling Access Denied Messages in a Provider](impersonating-a-client.md).</span></span>

 

 
