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
# <a name="changing-registry-data"></a>Modifica dei dati del registro di sistema

La classe del [provider del registro di sistema](/previous-versions/windows/desktop/regprov/system-registry-provider) [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) per WMI dispone di metodi che eseguono le operazioni seguenti:

-   Creare o eliminare chiavi del registro di sistema.

    Usare [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) o [**DeleteKey**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov).

-   Creare o eliminare i valori denominati, chiamati voci quando sono sotto chiavi.

    Usare il nome di un nuovo valore e [**SetBinaryValue**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov), [**SetDWORDValue**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov), [**SetExpandedStringValue**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov), [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)o [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) per creare un valore denominato. Usare [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) per eliminare un valore denominato.

-   Modificare i valori denominati.

    Usare il nome di un valore e i metodi set (identificati nell'elemento puntato precedente) per modificare i valori denominati esistenti in una chiave. È necessario essere a conoscenza del nome di un valore per modificarlo. Se non si conoscono i nomi di valore in una chiave, utilizzare il metodo [**EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) per ottenere i nomi.

Le sezioni seguenti sono illustrate in questo argomento:

-   [Creazione di una chiave del registro di sistema tramite VBScript](#creating-a-registry-key-using-vbscript)
-   [Creazione di un valore denominato del registro di sistema tramite PowerShell e VBScript](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a>Creazione di una chiave del registro di sistema tramite VBScript

Poiché il registro di sistema è il database di configurazione centrale per il sistema operativo, le applicazioni e i servizi, prestare attenzione quando si scrivono le modifiche ai valori del registro di sistema o si eliminano le chiavi.

> [!Note]  
> Non è possibile monitorare la sottochiave **\_ \_ radice delle classi HKEY** dell' **\_ utente corrente di HKEY \_ (HKCU)**. Il **monitoraggio \_ degli utenti di HKEY** non è consigliato perché le sottochiavi vengono visualizzate e scompaiono durante il caricamento degli hive.

 

Negli esempi di codice seguenti viene illustrato come creare una nuova chiave del registro di sistema e una sottochiave.


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





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a>Creazione di un valore denominato del registro di sistema tramite PowerShell e VBScript

Nell'esempio di codice riportato di seguito viene illustrato come creare un valore denominato denominato **MultiStringValue** nella chiave **HKEY \_ locale \_** del \\ **software** \\ **myKey** \\ della **sottochiave** creata dallo script precedente. Lo script chiama [**WMI StdRegProv. SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) per scrivere valori stringa in un nuovo valore denominato.


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

Utilizzando WMI, non è possibile impostare la sicurezza dell'accesso su una chiave del registro di sistema. Tuttavia, il metodo [**WMI StdRegProv. CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) Confronta le impostazioni di sicurezza dell'utente corrente con il descrittore di sicurezza su una chiave del registro di sistema per determinare se l'utente dispone di un'autorizzazione specifica, ad esempio il **valore del \_ set \_ di chiavi**.
