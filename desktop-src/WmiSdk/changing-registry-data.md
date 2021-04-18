---
description: 'La classe del provider del registro di sistema WMI StdRegProv per WMI dispone di metodi che eseguono le operazioni seguenti:'
ms.assetid: d42248b3-2f96-4771-aee9-a0db139b149e
ms.tgt_platform: multiple
title: Modifica dei dati del registro di sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b51f3f18eb718dab7c79f31a4b2188dd7afa529
ms.sourcegitcommit: 3d9eb6638763fee8b87c378657458f814182e36c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320431"
---
# <a name="changing-registry-data"></a><span data-ttu-id="4db04-103">Modifica dei dati del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="4db04-103">Changing Registry Data</span></span>

<span data-ttu-id="4db04-104">La classe del [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) per WMI dispone di metodi che eseguono le operazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="4db04-104">The [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) class [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) for WMI has methods that do the following:</span></span>

-   <span data-ttu-id="4db04-105">Creare o eliminare chiavi del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4db04-105">Create or delete registry keys.</span></span>

    <span data-ttu-id="4db04-106">Usare [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) o [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).</span><span class="sxs-lookup"><span data-stu-id="4db04-106">Use [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) or [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).</span></span>

-   <span data-ttu-id="4db04-107">Creare o eliminare i valori denominati, chiamati voci quando sono sotto chiavi.</span><span class="sxs-lookup"><span data-stu-id="4db04-107">Create or delete named values, which are called entries when they are under keys.</span></span>

    <span data-ttu-id="4db04-108">Usare il nome di un nuovo valore e [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)o [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) per creare un valore denominato.</span><span class="sxs-lookup"><span data-stu-id="4db04-108">Use the name of a new value and [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov), or [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) to create a named value.</span></span> <span data-ttu-id="4db04-109">Usare [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) per eliminare un valore denominato.</span><span class="sxs-lookup"><span data-stu-id="4db04-109">Use [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) to delete a named value.</span></span>

-   <span data-ttu-id="4db04-110">Modificare i valori denominati.</span><span class="sxs-lookup"><span data-stu-id="4db04-110">Change named values.</span></span>

    <span data-ttu-id="4db04-111">Usare il nome di un valore e i metodi set (identificati nell'elemento puntato precedente) per modificare i valori denominati esistenti in una chiave.</span><span class="sxs-lookup"><span data-stu-id="4db04-111">Use the name of a value and the Set methods (identified in the previous bulleted item) to change existing named values under a key.</span></span> <span data-ttu-id="4db04-112">È necessario essere a conoscenza del nome di un valore per modificarlo.</span><span class="sxs-lookup"><span data-stu-id="4db04-112">You must know the name of a value to change it.</span></span> <span data-ttu-id="4db04-113">Se non si conoscono i nomi di valore in una chiave, utilizzare il metodo [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) per ottenere i nomi.</span><span class="sxs-lookup"><span data-stu-id="4db04-113">If you do not know the value names under a key, use the [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) method to obtain the names.</span></span>

<span data-ttu-id="4db04-114">Le sezioni seguenti sono illustrate in questo argomento:</span><span class="sxs-lookup"><span data-stu-id="4db04-114">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="4db04-115">Creazione di una chiave del registro di sistema tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="4db04-115">Creating a Registry Key Using VBScript</span></span>](#creating-a-registry-key-using-vbscript)
-   [<span data-ttu-id="4db04-116">Creazione di un valore denominato del registro di sistema tramite PowerShell e VBScript</span><span class="sxs-lookup"><span data-stu-id="4db04-116">Creating a Named Registry Value Using PowerShell and VBScript</span></span>](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a><span data-ttu-id="4db04-117">Creazione di una chiave del registro di sistema tramite VBScript</span><span class="sxs-lookup"><span data-stu-id="4db04-117">Creating a Registry Key Using VBScript</span></span>

<span data-ttu-id="4db04-118">Poiché il registro di sistema è il database di configurazione centrale per il sistema operativo, le applicazioni e i servizi, prestare attenzione quando si scrivono le modifiche ai valori del registro di sistema o si eliminano le chiavi.</span><span class="sxs-lookup"><span data-stu-id="4db04-118">Because the registry is the central configuration database for the operating system, applications, and services, use caution when you write changes to registry values or delete keys.</span></span>

> [!Note]  
> <span data-ttu-id="4db04-119">Non è possibile monitorare la sottochiave **\_ \_ radice delle classi HKEY** dell' **\_ utente corrente di HKEY \_ (HKCU)**.</span><span class="sxs-lookup"><span data-stu-id="4db04-119">You cannot monitor the **HKEY\_CLASSES\_ROOT** subkey of **HKEY\_CURRENT\_USER(HKCU)**.</span></span> <span data-ttu-id="4db04-120">Il **monitoraggio \_ degli utenti di HKEY** non è consigliato perché le sottochiavi vengono visualizzate e scompaiono durante il caricamento degli hive.</span><span class="sxs-lookup"><span data-stu-id="4db04-120">Monitoring **HKEY\_USERS** is not recommended because the subkeys appear and disappear as hives are loaded.</span></span>

 

<span data-ttu-id="4db04-121">Negli esempi di codice seguenti viene illustrato come creare una nuova chiave del registro di sistema e una sottochiave.</span><span class="sxs-lookup"><span data-stu-id="4db04-121">The following code examples show how to create a new registry key and a subkey.</span></span>


```VB
HKEY_LOCAL_MACHINE = &H80000002
strComputer = "."

Set ObjRegistry = GetObject("winmgmts:{impersonationLevel = impersonate}!\\" & strComputer & "\root\default:StdRegProv")

strPath = "SOFTWARE\MyKey\MySubKey"

Return = objRegistry.CreateKey(HKEY_LOCAL_MACHINE, strPath)

If Return <> 0 Then
    WScript.Echo "The operation failed." & Err.Number
    WScript.Quit
Else
    wScript.Echo "New registry key created" & VBCRLF & "HKLM\SOFTWARE\MYKey\"

End If
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.CreateKey($HKEY_LOCAL_MACHINE, $strPath)
```





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a><span data-ttu-id="4db04-122">Creazione di un valore denominato del registro di sistema tramite PowerShell e VBScript</span><span class="sxs-lookup"><span data-stu-id="4db04-122">Creating a Named Registry Value Using PowerShell and VBScript</span></span>

<span data-ttu-id="4db04-123">Nell'esempio di codice riportato di seguito viene illustrato come creare un valore denominato denominato **MultiStringValue** nella chiave **HKEY \_ locale \_** del \\ **software** \\ **myKey** \\ della **sottochiave** creata dallo script precedente.</span><span class="sxs-lookup"><span data-stu-id="4db04-123">The following code example shows how to create a named value called **MultiStringValue** under the **HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**MyKey**\\**MySubKey** key that the previous script creates.</span></span> <span data-ttu-id="4db04-124">Lo script chiama [**WMI StdRegProv. SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) per scrivere valori stringa in un nuovo valore denominato.</span><span class="sxs-lookup"><span data-stu-id="4db04-124">The script calls [**StdRegProv.SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) to write string values to a new named value.</span></span>


```VB
const HKEY_LOCAL_MACHINE = &H80000002 
strComputer = "."

Set objRegistry = _
    GetObject("winmgmts:{impersonationLevel=impersonate}!\\" _ 
    & strComputer & "\root\default:StdRegProv")

strKeyPath = "SOFTWARE\MyKey\MySubKey"
strValueName = "MultiStringValue"
arrStringValues = Array("one", "two","three", "four")

objRegistry.SetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues

' Read the values that were just written
objRegistry.GetMultiStringValue HKEY_LOCAL_MACHINE, strKeyPath,_
    strValueName, arrStringValues   

For Each strValue in arrStringValues
    WScript.Echo strValue 
Next
```


```PowerShell

$HKEY_LOCAL_MACHINE = 2147483650 
$strComputer = "."
$strPath = "SOFTWARE\MyKey\MySubKey"

$strValueName = "MultiStringValue"
$arrStringValues = @("one", "two","three", "four")

$reg = [wmiclass]"\\$strComputer\root\default:StdRegprov"

[void]$reg.SetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName, $arrStringValues)

$multiValues = $reg.GetMultiStringValue($HKEY_LOCAL_MACHINE, $strKeyPath, $strValueName)
$multiValues.sValue
```

<span data-ttu-id="4db04-125">Utilizzando WMI, non è possibile impostare la sicurezza dell'accesso su una chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="4db04-125">Using WMI, you cannot set access security on a registry key.</span></span> <span data-ttu-id="4db04-126">Tuttavia, il metodo [**WMI StdRegProv. CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) Confronta le impostazioni di sicurezza dell'utente corrente con il descrittore di sicurezza su una chiave del registro di sistema per determinare se l'utente dispone di un'autorizzazione specifica, ad esempio il **valore del \_ set \_ di chiavi**.</span><span class="sxs-lookup"><span data-stu-id="4db04-126">However, the [**StdRegProv.CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) method compares the security settings of the current user to the security descriptor on a registry key to determine if the user has a specific permission, such as **KEY\_SET\_VALUE**.</span></span>
