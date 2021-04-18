---
description: Le prestazioni delle chiamate semisincrono sono in genere appropriate per la maggior parte delle situazioni.
ms.assetid: f665fc60-68bd-495d-a441-e3a9473f9d89
ms.tgt_platform: multiple
title: Impostazione della sicurezza per una chiamata asincrona in VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 972947e0cb4f5d385e4d2d27b7c14298771ac4e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318524"
---
# <a name="setting-security-on-an-asynchronous-call-in-vbscript"></a>Impostazione della sicurezza per una chiamata asincrona in VBScript

Le prestazioni delle chiamate [*semisincrono*](gloss-s.md) sono in genere appropriate per la maggior parte delle situazioni. Le chiamate asincrone non sono in genere una procedura consigliata per gli script. Tuttavia, se è necessario effettuare chiamate asincrone, è possibile impostare un valore del registro di sistema in modo da forzare WMI a eseguire controlli di accesso sulle chiamate asincrone.


Il valore del registro di sistema **HKEY \_ Local \_ Machine** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **UnsecAppAccessControlDefault** controlla se WMI controlla la presenza di un livello di autenticazione accettabile per la restituzione di dati per una chiamata asincrona. Il callback può essere restituito a un livello di autenticazione inferiore rispetto a quello della chiamata asincrona originale. Per impostazione predefinita, questo valore è impostato su zero, in modo che i callback non vengano controllati. Per proteggere le chiamate asincrone nello scripting, è necessario impostare la chiave del registro di sistema su 1 (uno).

Gli script possono usare i metodi [**GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) e [**SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov) dell'oggetto registro di sistema [**WMI StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) per modificare l'impostazione del valore del registro di sistema **UnsecAppAccessControlDefault** . Per ulteriori informazioni sui livelli di autenticazione e di rappresentazione necessari per l'accesso remoto, vedere la pagina relativa [alla connessione a WMI in un computer remoto](connecting-to-wmi-on-a-remote-computer.md).

## <a name="to-set-asynchronous-call-security-in-vbscript"></a>Per impostare la sicurezza delle chiamate asincrone in VBScript

Nell'esempio di codice VBScript riportato di seguito viene illustrato come modificare il valore del registro di sistema per controllare l'autenticazione WMI dei callback.

Lo script modifica il valore di **UnsecAppAccessControlDefault** da zero a uno oppure se il valore è già impostato, da uno a zero. Il valore predefinito è zero in un sistema appena installato. Una volta impostato il flag, l'impostazione viene mantenute durante il riavvio o il riavvio di WMI.

Lo script usa un oggetto [**SWbemMethod. InParameters**](swbemmethod-inparameters.md) e [**SWbemObject.ExeCMethod**](swbemobject-execmethod-.md) per chiamare [**WMI StdRegProv. GetStringValue**](/previous-versions/windows/desktop/regprov/getstringvalue-method-in-class-stdregprov) e [**WMI StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov). Per ulteriori informazioni sull'impostazione dei valori in un oggetto **InParameters** , vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md). Per un esempio di una chiamata al registro di sistema tramite [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx), vedere [**WMI StdRegProv. SetStringValue**](/previous-versions/windows/desktop/regprov/setstringvalue-method-in-class-stdregprov).


```VB
' Registry key value in hex
Const hklm = &h800000002  
' Subkey string 
Const Subkey = "software\\microsoft\\wbem\\cimom" 
' Asynchronous access control
Const sValueName = "UnsecAppAccessControlDefault" 

' Obtain registry object
Set objReg = GetObject("winmgmts:root\default:StdRegProv") 

' Get the initial value of the asynchronous 
'   access control registry key
' Use an InParameters object to set up the 
'   parameters for the ExecMethod call
' For more information see Constructing InParameters Objects 
'   topic and SWbemObject.ExecMethod_ topic

Set InParams = objReg.methods_("GetStringValue").InParameters.SpawnInstance_
InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName

' Get return value from OutParameters object returned by ExecMethod. 
' For more information see Parsing OutParameters Objects topic

Set OutParams = objReg.Execmethod_("GetStringValue",InParams)

If (OutParams.ReturnValue <> 0) then
   Wscript.Echo "GetStringValue returned " & OutParams.ReturnValue
   Wscript.Quit 1
End If

Svalue = OutParams.sValue
If (sValue = 0) Then
   AccessControl = "WMI not performing asynch access control"
Else 
   AccessControl = "WMI performing asynch access control"  
End If
Wscript.Echo sValueName & " = " _
    & sValue & VBNewLine & AccessControl

' Change asynchronous access control registry key value
Set InParams = objReg.methods_("SetStringValue").InParameters.SpawnInstance_

InParams.hDefKey = hklm
InParams.sSubKeyName = Subkey
InParams.sValueName = sValueName
InParams.sValue = sValue XOR 1

Set OutParams = objReg.ExecMethod_("SetStringValue",InParams)

If (OutParams.Returnvalue <> 0) Then
    Wscript.Echo "SetStringValue returned " & OutParams.Returnvalue
    Wscript.Quit 1
End If

Wscript.Echo SValueName & " changed to " & (sValue XOR 1)
```



 

 
