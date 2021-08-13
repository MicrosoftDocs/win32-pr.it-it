---
description: 'La classe StdRegProv del provider del Registro di sistema per WMI dispone di metodi che consentono di eseguire le operazioni seguenti:'
ms.assetid: d42248b3-2f96-4771-aee9-a0db139b149e
ms.tgt_platform: multiple
title: Modifica dei dati del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 32258fb64e075889a6e423e2b6a3fa2e7b0fdeb0ee5a80e2f45436674ba79c4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118556946"
---
# <a name="changing-registry-data"></a>Modifica dei dati del Registro di sistema

La classe [**StdRegProv del**](/previous-versions/windows/desktop/regprov/stdregprov) [provider](/previous-versions/windows/desktop/regprov/system-registry-provider) del Registro di sistema per WMI dispone di metodi che consentono di eseguire le operazioni seguenti:

-   Creare o eliminare chiavi del Registro di sistema.

    Usare [**CreateKey**](/previous-versions/windows/desktop/regprov/createkey-method-in-class-stdregprov) o [**DeleteKey.**](/previous-versions/windows/desktop/regprov/deletekey-method-in-class-stdregprov)

-   Creare o eliminare valori denominati, detti voci quando si tratta di chiavi.

    Usare il nome di un nuovo valore e [**SetBinaryValue,**](/previous-versions/windows/desktop/regprov/setbinaryvalue-method-in-class-stdregprov) [**SetDWORDValue,**](/previous-versions/windows/desktop/regprov/setdwordvalue-method-in-class-stdregprov) [**SetExpandedStringValue,**](/previous-versions/windows/desktop/regprov/setexpandedstringvalue-method-in-class-stdregprov) [**SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov)o [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) per creare un valore denominato. Usare [**DeleteValue**](/previous-versions/windows/desktop/regprov/deletevalue-method-in-class-stdregprov) per eliminare un valore denominato.

-   Modificare i valori denominati.

    Usare il nome di un valore e i metodi Set (identificati nell'elemento puntato precedente) per modificare i valori denominati esistenti in una chiave. È necessario conoscere il nome di un valore per modificarlo. Se non si conoscono i nomi dei valori in una chiave, usare il [**metodo EnumValues**](/previous-versions/windows/desktop/regprov/enumvalues-method-in-class-stdregprov) per ottenere i nomi.

In questo argomento vengono illustrate le sezioni seguenti:

-   [Creazione di una chiave del Registro di sistema tramite VBScript](#creating-a-registry-key-using-vbscript)
-   [Creazione di un valore del Registro di sistema denominato tramite PowerShell e VBScript](#creating-a-named-registry-value-using-powershell-and-vbscript)

## <a name="creating-a-registry-key-using-vbscript"></a>Creazione di una chiave del Registro di sistema tramite VBScript

Poiché il Registro di sistema è il database di configurazione centrale per il sistema operativo, le applicazioni e i servizi, prestare attenzione quando si scrivono modifiche ai valori del Registro di sistema o si eliminano chiavi.

> [!Note]  
> Non è possibile monitorare **la sottochiave \_ HKEY CLASSES \_ ROOT** di **HKEY \_ CURRENT \_ USER(HKCU)**. Il **monitoraggio di HKEY \_ USERS** non è consigliato perché le sottochiavi vengono visualizzate e scompaiono durante il caricamento degli hive.

 

Gli esempi di codice seguenti illustrano come creare una nuova chiave del Registro di sistema e una sottochiave.


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





## <a name="creating-a-named-registry-value-using-powershell-and-vbscript"></a>Creazione di un valore del Registro di sistema denominato tramite PowerShell e VBScript

L'esempio di codice seguente illustra come creare un valore denominato **MultiStringValue** sotto la chiave **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\  \\ **MyKey MySubKey** creata nello script precedente. Lo script chiama [**StdRegProv.SetMultiStringValue**](/previous-versions/windows/desktop/regprov/setmultistringvalue-method-in-class-stdregprov) per scrivere valori stringa in un nuovo valore denominato.


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

Tramite WMI, non è possibile impostare la sicurezza di accesso su una chiave del Registro di sistema. Tuttavia, il metodo [**StdRegProv.CheckAccess**](/previous-versions/windows/desktop/regprov/checkaccess-method-in-class-stdregprov) confronta le impostazioni di sicurezza dell'utente corrente con il descrittore di sicurezza in una chiave del Registro di sistema per determinare se l'utente dispone di un'autorizzazione specifica, ad esempio **KEY SET \_ \_ VALUE.**
