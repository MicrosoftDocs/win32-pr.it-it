---
description: È possibile ottenere o modificare i dati del registro di sistema utilizzando la classe WMI WMI StdRegProv e i relativi metodi.
ms.assetid: 7cba9dcb-741b-4118-9769-8830c6dc0752
ms.tgt_platform: multiple
title: Recupero dei dati del registro di sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f5468a577acedeccf4396607147428d9160b4d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305574"
---
# <a name="obtaining-registry-data"></a><span data-ttu-id="3a3d1-103">Recupero dei dati del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="3a3d1-103">Obtaining Registry Data</span></span>

<span data-ttu-id="3a3d1-104">È possibile ottenere o modificare i dati del registro di sistema utilizzando la classe WMI [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) e i relativi metodi.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-104">You can obtain or modify registry data by using the WMI [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class and its methods.</span></span> <span data-ttu-id="3a3d1-105">Quando si usa l'utilità Regedit per visualizzare e modificare i valori del registro di sistema nel computer locale, **WMI StdRegProv** consente di usare uno script o un'applicazione per automatizzare tali attività nel computer locale e nei computer remoti.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-105">While use the Regedit utility to view and change registry values on the local computer, **StdRegProv** allows you to use a script or application to automate such activities on the local computer and remote computers.</span></span>

<span data-ttu-id="3a3d1-106">[**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contiene i metodi per eseguire le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3a3d1-106">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) contains methods to do the following:</span></span>

-   <span data-ttu-id="3a3d1-107">Verificare le autorizzazioni di accesso per un utente</span><span class="sxs-lookup"><span data-stu-id="3a3d1-107">Verify the access permissions for a user</span></span>
-   <span data-ttu-id="3a3d1-108">Creare, enumerare ed eliminare chiavi del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="3a3d1-108">Create, enumerate, and delete registry keys</span></span>
-   <span data-ttu-id="3a3d1-109">Creare, enumerare ed eliminare sottochiavi o valori denominati</span><span class="sxs-lookup"><span data-stu-id="3a3d1-109">Create, enumerate, and delete subkeys or named values</span></span>
-   <span data-ttu-id="3a3d1-110">Lettura, scrittura ed eliminazione dei valori dei dati</span><span class="sxs-lookup"><span data-stu-id="3a3d1-110">Read, write, and delete data values</span></span>

<span data-ttu-id="3a3d1-111">I dati del registro di sistema sono organizzati in base ad alberi, chiavi e sottochiavi annidati sotto una chiave di primo livello.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-111">Registry data is organized by subtrees, keys, and subkeys nested under a top level key.</span></span> <span data-ttu-id="3a3d1-112">I valori dei dati effettivi sono denominati voci o valori denominati.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-112">The actual data values are called entries or named values.</span></span>

<span data-ttu-id="3a3d1-113">Le sottostrutture includono quanto segue:</span><span class="sxs-lookup"><span data-stu-id="3a3d1-113">The subtrees include the following:</span></span>

-   <span data-ttu-id="3a3d1-114">**HKEY \_ \_Radice delle classi** (abbreviata come **HKCR**)</span><span class="sxs-lookup"><span data-stu-id="3a3d1-114">**HKEY\_CLASSES\_ROOT** (abbreviated as **HKCR**)</span></span>
-   <span data-ttu-id="3a3d1-115">**HKEY \_ \_utente corrente** (**HKCU**)</span><span class="sxs-lookup"><span data-stu-id="3a3d1-115">**HKEY\_CURRENT\_USER** (**HKCU**)</span></span>
-   <span data-ttu-id="3a3d1-116">**HKEY \_ \_computer locale** (**HKLM**)</span><span class="sxs-lookup"><span data-stu-id="3a3d1-116">**HKEY\_LOCAL\_MACHINE** (**HKLM**)</span></span>
-   <span data-ttu-id="3a3d1-117">**\_utenti HKEY**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-117">**HKEY\_USERS**</span></span>
-   <span data-ttu-id="3a3d1-118">**HKEY \_ \_ configurazione corrente**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-118">**HKEY\_CURRENT\_CONFIG**</span></span>

<span data-ttu-id="3a3d1-119">Ad esempio, nella voce del registro di sistema **HKEY** \\ **software** \\ **Microsoft** \\ **DirectX** \\ **InstalledVersion**, il sottoalbero HKEY è **software**, le sottochiavi sono **Microsoft** e **DirectX** e la voce del valore denominato è **InstalledVersion**.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-119">For example, in the registry entry **HKEY**\\**SOFTWARE**\\**Microsoft**\\**DirectX**\\**InstalledVersion**, the HKEY subtree is **SOFTWARE**; the subkeys are **Microsoft** and **DirectX**; and the named value entry is **InstalledVersion**.</span></span>

<span data-ttu-id="3a3d1-120">Un [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) si verifica quando viene apportata una modifica a una chiave specifica, ma la voce non identifica il modo in cui i valori cambiano, né questo evento verrà attivato da modifiche al di sotto della chiave specificata.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-120">A [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent) occurs when a change to a specific key occurs, but the entry does not identify how the values change nor will this event be triggered by changes below the specified key.</span></span> <span data-ttu-id="3a3d1-121">Per identificare le modifiche in un punto qualsiasi di una struttura di chiavi gerarchica, utilizzare [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), che non restituisce valori specifici o modifiche chiave che si verificano.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-121">To identify changes anywhere in a hierarchical key structure, use the [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent), which does not return specific values or key changes that occur.</span></span> <span data-ttu-id="3a3d1-122">Per ottenere una modifica del valore di una voce specifica, usare [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent)e quindi leggere la voce per ottenere un valore baseline.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-122">To obtain a specific entry value change, use the [**RegistryValueChangeEvent**](/previous-versions/windows/desktop/regprov/registryvaluechangeevent), and then read the entry to obtain a baseline value.</span></span>

<span data-ttu-id="3a3d1-123">[**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) dispone solo di metodi che possono essere chiamati da C++ o script, che è diverso dalla struttura della classe Win32.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-123">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) only has methods that can be called from C++ or script, which is different from the Win32 class structure.</span></span>

<span data-ttu-id="3a3d1-124">Nell'esempio di codice riportato di seguito viene illustrato come utilizzare il metodo [**WMI StdRegProv. enumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) per elencare tutte le sottochiavi software Microsoft presenti nella chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-124">The following code example shows how to use the [**StdRegProv.EnumKey**](/previous-versions/windows/desktop/regprov/enumkey-method-in-class-stdregprov) method to list all of the Microsoft software subkeys under the registry key.</span></span>

<span data-ttu-id="3a3d1-125">**HKEY \_ SOFTWARE del \_ computer locale** \\  \\ **Microsoft**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650
$strKeyPath = &quot;SOFTWARE\Microsoft&quot;

$objReg = [WMIClass]&quot;root\default:StdRegProv&quot;

$arrSubKeys = $objReg.EnumKey($HKEY_LOCAL_MACHINE, $strKeyPath)
foreach ($subKey in ($arrSubKeys.sNames))
{
    $subKey
}
```





<span data-ttu-id="3a3d1-126">[**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) dispone di metodi diversi per la lettura dei diversi tipi di dati del valore della voce del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-126">[**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) has different methods for reading the various registry entry value data types.</span></span> <span data-ttu-id="3a3d1-127">Se la voce contiene valori sconosciuti, è possibile chiamare [**WMI StdRegProv. EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) per elencarli.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-127">If the entry has unknown values, then you can call [**StdRegProv.EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) to list them.</span></span> <span data-ttu-id="3a3d1-128">La tabella seguente elenca la corrispondenza tra i metodi **WMI StdRegProv** e i tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-128">The following table lists the correspondence between **StdRegProv** methods and the data types.</span></span>



| <span data-ttu-id="3a3d1-129">Metodo</span><span class="sxs-lookup"><span data-stu-id="3a3d1-129">Method</span></span>                                                                                  | <span data-ttu-id="3a3d1-130">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3a3d1-130">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="3a3d1-131">**GetBinaryValue**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-131">**GetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/getbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="3a3d1-132">**REG \_ binario**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-132">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="3a3d1-133">**GetDWORDValue**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-133">**GetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/getdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="3a3d1-134">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-134">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="3a3d1-135">**GetExpandedStringValue**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-135">**GetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="3a3d1-136">**REG \_ Espandi \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-136">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="3a3d1-137">**GetMultiStringValue**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-137">**GetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="3a3d1-138">**REG \_ - \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-138">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="3a3d1-139">**GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-139">**GetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="3a3d1-140">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-140">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="3a3d1-141">La tabella seguente elenca i metodi corrispondenti per la creazione di nuove chiavi o valori o la modifica di quelli esistenti.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-141">The following table lists the corresponding methods for creating new keys or values, or changing existing ones.</span></span>



| <span data-ttu-id="3a3d1-142">Metodo</span><span class="sxs-lookup"><span data-stu-id="3a3d1-142">Method</span></span>                                                                                  | <span data-ttu-id="3a3d1-143">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3a3d1-143">Data Type</span></span>           |
|-----------------------------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="3a3d1-144">**SetBinaryValue**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-144">**SetBinaryValue**</span></span>](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov)                 | <span data-ttu-id="3a3d1-145">**REG \_ binario**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-145">**REG\_BINARY**</span></span>     |
| [<span data-ttu-id="3a3d1-146">**SetDWORDValue**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-146">**SetDWORDValue**</span></span>](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov)                   | <span data-ttu-id="3a3d1-147">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-147">**REG\_DWORD**</span></span>      |
| [<span data-ttu-id="3a3d1-148">**SetExpandedStringValue**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-148">**SetExpandedStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) | <span data-ttu-id="3a3d1-149">**REG \_ Espandi \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-149">**REG\_EXPAND\_SZ**</span></span> |
| [<span data-ttu-id="3a3d1-150">**SetMultiStringValue**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-150">**SetMultiStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)       | <span data-ttu-id="3a3d1-151">**REG \_ - \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-151">**REG\_MULTI\_SZ**</span></span>  |
| [<span data-ttu-id="3a3d1-152">**SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-152">**SetStringValue**</span></span>](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov)                 | <span data-ttu-id="3a3d1-153">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="3a3d1-153">**REG\_SZ**</span></span>         |



 

<span data-ttu-id="3a3d1-154">Nell'esempio seguente viene illustrato come leggere l'elenco di origini per il registro eventi di sistema dalla chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-154">The following example shows how to read the list of sources for the system event log from the registry key.</span></span>

<span data-ttu-id="3a3d1-155">**HKEY \_ Sistema \_ del** registro eventi di sistema del computer locale \\  \\  \\  \\  \\ **sistema** registro eventi</span><span class="sxs-lookup"><span data-stu-id="3a3d1-155">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**Current Control Set**\\**Services**\\**Eventlog**\\**System**</span></span>

<span data-ttu-id="3a3d1-156">Si noti che gli elementi nel valore multistringa vengono considerati come una raccolta o una matrice.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-156">Note that the items in the multistring value are treated as a collection or array.</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set objReg=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\Microsoft"
objReg.EnumKey HKEY_LOCAL_MACHINE, strKeyPath, arrSubKeys

For Each subkey In arrSubKeys
Wscript.Echo subkey
    
Next
```



<span data-ttu-id="3a3d1-157">Il provider del registro di sistema è ospitato in LocalService, non in LocalSystem.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-157">The registry provider is hosted in LocalService—not the LocalSystem.</span></span> <span data-ttu-id="3a3d1-158">Per questo motivo, non è possibile ottenere informazioni in modalità remota dal sottoalbero **HKEY \_ \_ utente corrente** .</span><span class="sxs-lookup"><span data-stu-id="3a3d1-158">Therefore, obtaining information remotely from the subtree **HKEY\_CURRENT\_USER** is not possible.</span></span> <span data-ttu-id="3a3d1-159">Tuttavia, gli script eseguiti nel computer locale possono comunque accedere **all' \_ \_ utente corrente di HKEY**.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-159">However, scripts run on the local computer can still access **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="3a3d1-160">È possibile impostare il modello di hosting su LocalSystem in un computer remoto, ma si tratta di un rischio per la sicurezza perché il registro di sistema nel computer remoto è vulnerabile ad accesso ostile.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-160">You can set the hosting model to LocalSystem on a remote machine, but that is a security risk because the registry on the remote machine is vulnerable to hostile access.</span></span> <span data-ttu-id="3a3d1-161">Per altre informazioni, vedere [hosting e sicurezza del provider](provider-hosting-and-security.md).</span><span class="sxs-lookup"><span data-stu-id="3a3d1-161">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3a3d1-162">Esempio</span><span class="sxs-lookup"><span data-stu-id="3a3d1-162">Examples</span></span>

<span data-ttu-id="3a3d1-163">L'esempio di codice VBScript [Read a Binary Registry Value](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) in TechNet Gallery USA WMI per leggere un valore binario del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="3a3d1-163">The [Read a Binary Registry Value](https://Gallery.TechNet.Microsoft.Com/b0724cb2-36ed-4d0d-8b8f-428d0e3d0b82) VBScript code example on TechNet Gallery uses WMI to read a binary registry value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a3d1-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3a3d1-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a3d1-165">Attività WMI: Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="3a3d1-165">WMI Tasks: Registry</span></span>](wmi-tasks--registry.md)
</dt> </dl>

 

 
