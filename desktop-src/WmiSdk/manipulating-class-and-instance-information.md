---
description: WMI offre un'ampia gamma di tecniche per recuperare e modificare le informazioni di classe e istanza WMI, usando Microsoft PowerShell, Visual&\# 160; Basic Scripting Edition (VBScript) e C++.
ms.assetid: 682cbe12-1487-4681-8d2f-4caf21cb068a
ms.tgt_platform: multiple
title: Modifica delle informazioni sulle classi e sulle istanze
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 86e3e84deae73e206f41e9ea25e02b5d11373f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317549"
---
# <a name="manipulating-class-and-instance-information"></a>Modifica delle informazioni sulle classi e sulle istanze

WMI offre un'ampia gamma di tecniche per recuperare e modificare le informazioni di classe e istanza WMI, usando Microsoft PowerShell, Visual Basic Scripting Edition (VBScript) e C++.

Nella tabella seguente sono elencati gli argomenti che illustrano le tecniche per recuperare e modificare le informazioni sulle istanze e le classi WMI.



| Argomento                                                                                  | Descrizione                                                                                                                                                                       |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Recupero dei dati della classe o dell'istanza WMI](retrieving-class-or-instance-data.md)         | Recuperare e impostare i dati da e nel repository di informazioni WMI.                                                                                                                 |
| [Modifica di una proprietà dell'istanza](modifying-an-instance-property.md)                   | Modificare le informazioni nell'istanza dopo che è stata recuperata.                                                                                                                     |
| [Modifica dell'ereditarietà di un'istanza](changing-the-inheritance-of-an-instance.md) | Modificare la classe padre di un'istanza.                                                                                                                                           |
| [Modifica di un metodo](modifying-a-method.md)                                           | Modificare i parametri di un'istanza.                                                                                                                                             |
| [Enumerazione di WMI](enumerating-wmi.md)                                                 | Enumerazione degli oggetti WMI.                                                                                                                                                            |
| [Esecuzione di query su WMI](querying-wmi.md)                                                       | Eseguire query su oggetti WMI.                                                                                                                                                                |
| [Chiamata a un metodo](calling-a-method.md)                                               | Usare i metodi associati creati da Microsoft o da altri sviluppatori di terze parti per modificare ulteriormente gli oggetti WMI, altrimenti influiscono direttamente sull'oggetto rappresentato dall'oggetto WMI. |
| [Accesso a una raccolta](accessing-a-collection.md)                                   | Enumerare le raccolte nello script.                                                                                                                                                  |



 

## <a name="manipulating-data-using-vbscript"></a>Manipolazione dei dati tramite VBScript

È possibile utilizzare l'accesso diretto per accedere alle proprietà WMI di una classe o di un'istanza WMI direttamente in un [**SWbemObject**](swbemobject.md), anziché tramite la [raccolta](accessing-a-collection.md) di proprietà di tale oggetto. È inoltre possibile eseguire metodi su tale oggetto nello stile nativo del linguaggio di programmazione anziché utilizzare la chiamata [**cMethodSWbemServices.Exe**](swbemservices-execmethod.md) . Ad esempio, il metodo [**create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) nel [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) aveva tre parametri in Windows 2000 ma ha quattro parametri in Windows Server 2003.

Utilizzando l'accesso diretto, è possibile considerare proprietà e metodi WMI come se fossero proprietà e metodi di automazione di [**SWbemObject**](swbemobject.md).

Nell'esempio seguente viene illustrato come è possibile accedere a una proprietà.


```VB
VolumeName = MyDisk.Properties_("VolumeName")
```



Nell'esempio seguente viene illustrato come è possibile accedere a una proprietà quando si dispone di accesso diretto.


```VB
VolumeName = MyDisk.VolumeName
```



È inoltre accettabile il concatenamento di oggetti.

Nell'esempio seguente viene illustrato come accedere a una proprietà di un oggetto incorporato in un altro oggetto.


```VB
value = MyComputer.MyDisk.VolumeName
```



Nell'esempio seguente viene illustrato come accedere a una proprietà con la notazione di indice di matrice.


```VB
valueOfElement = MyDisk.MyArrayProperty(3)
```



Nell'esempio di codice VBScript seguente viene illustrato come generare un'istanza dei parametri di input nel [**Metodo Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) nella classe [**di \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) come [**SWbemObject**](swbemobject.md), inserire le proprietà di input e quindi eseguire il metodo **create** utilizzando [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).

La proprietà [**SWbemObject. \_ Methods**](swbemobject-methods-.md) restituisce una raccolta [**SWbemMethodSet**](swbemmethodset.md) dei metodi di [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) . I membri del set di metodi sono oggetti [**SWbemMethod**](swbemmethod.md) e [**SWbemMethod. InParameters**](swbemmethod-inparameters.md) restituisce i parametri di input per il metodo [**create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) . Il parametro di input della *riga* di comando obbligatorio è impostato su "calc.exe". Il metodo viene quindi eseguito da [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), causando l'avvio di un processo di calc.exe.


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set obj = Services.Get("Win32_Process")
Set objIns = obj.Methods_("Create").InParameters.SpawnInstance_
objIns.CommandLine = "calc.exe"
Set objOut = Services.ExecMethod("Win32_Process", "Create", objIns)
MsgBox "Return value = " & objOut.returnvalue & VBCRLF & "Process ID = " & objOut.processid
```



Nell'esempio di codice seguente viene illustrato come eseguire l'operazione precedente utilizzando l'accesso diretto.


```VB
set Services = GetObject("winmgmts:root\cimv2")
Set Obj = Services.Get("Win32_Process")
returnvalue = Obj.create("calc.exe",,,processid)
MsgBox "Return value = " & returnvalue & VBCRLF & "Process ID = " & processid
```



Per ulteriori informazioni, vedere [chiamata di un metodo del provider](calling-a-provider-method.md) e creazione di [script con SWbemObject](scripting-with-swbemobject.md).

 

 
