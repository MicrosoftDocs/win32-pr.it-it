---
description: È possibile utilizzare i metodi dell'oggetto SWbemLocator per ottenere un oggetto SWbemServices che rappresenta una connessione a uno spazio dei nomi in un computer locale o in un computer host remoto.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Oggetto SWbemLocator (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator
- ISWbemLocator
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 964b040fa5046aa619dc08df92838dca343ba9b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313174"
---
# <a name="swbemlocator-object"></a>Oggetto SWbemLocator

È possibile utilizzare i metodi dell'oggetto **SWbemLocator** per ottenere un oggetto [**SWbemServices**](swbemservices.md) che rappresenta una connessione a uno spazio dei nomi in un computer locale o in un computer host remoto. È quindi possibile utilizzare i metodi dell'oggetto **SWbemServices** per accedere a WMI. Questo oggetto può essere creato dalla chiamata **CreateObject** di VBScript.

## <a name="members"></a>Membri

L'oggetto **SWbemLocator** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SWbemLocator** dispone di questi metodi.



| Metodo                                              | Descrizione                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [**ConnectServer**](swbemlocator-connectserver.md) | Stabilisce la connessione a WMI nel computer specificato.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **SWbemLocator** dispone di queste proprietà.



| Proprietà                                                | Tipo di accesso          | Descrizione                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Sicurezza\_**](swbemlocator-security-.md)<br/> | Sola lettura<br/> | Utilizzato per leggere o modificare le impostazioni di sicurezza.<br/> |



 

## <a name="remarks"></a>Commenti

Nella parte superiore del modello a oggetti della libreria di scripting WMI è l'oggetto SWbemLocator. SWbemLocator viene utilizzato per stabilire una connessione autenticata a uno spazio dei nomi WMI, molto come la funzione GetObject di VBScript e il moniker WMI "winmgmts:" vengono utilizzati per stabilire una connessione autenticata a WMI. Tuttavia, SWbemLocator è progettato per risolvere due scenari di scripting specifici che non possono essere eseguiti tramite GetObject e il moniker WMI. È necessario usare SWbemLocator se è necessario:

-   Fornire le credenziali utente e password per la connessione a WMI in un computer remoto. Il moniker WMI utilizzato con la funzione GetObject non include un meccanismo per specificare le credenziali. Per la maggior parte delle attività WMI, incluse tutte quelle eseguite su computer remoti, sono necessari i diritti di amministratore. Se in genere si accede con un account utente normale invece che con un account amministratore, non sarà possibile eseguire la maggior parte delle attività WMI, a meno che non si esegua lo script con credenziali alternative.
-   Connettersi a WMI se si esegue uno script WMI dall'interno di una pagina Web. Non è possibile usare la funzione GetObject quando si eseguono script incorporati all'interno di una pagina HTML perché Internet Explorer non consente l'uso di GetObject per motivi di sicurezza.

Inoltre, è possibile utilizzare SWbemLocator per connettersi a WMI se si individua la stringa di connessione WMI utilizzata con la funzionalità GetObject confusa o complessa.

Usare CreateObject anziché GetObject per creare un riferimento a SWbemLocator. Per creare il riferimento, è necessario passare la funzione CreateObject SWbemLocator programmatical Identifier (ProgID) "WbemScripting. SWbemLocator", come illustrato nella riga 2 dello script di esempio seguente. Dopo aver ottenuto un riferimento a un oggetto SWbemLocator, chiamare il metodo ConnectServer per connettersi a WMI e ottenere un riferimento a un oggetto SWbemServices. Questa operazione viene illustrata nella riga 3 dello script seguente.


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Per eseguire uno script con credenziali alternative, includere il nome utente e la password come parametri aggiuntivi passati a ConnectServer. Ad esempio, questo script viene eseguito con le credenziali di un utente denominato kenmyer, con la password HomerJ.


```VB
strComputer = "atl-dc-01"
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer _
    (strComputer, "root\cimv2", "kenmyer", "homerj")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



È anche possibile usare il \\ formato del nome utente di dominio per specificare un nome utente. Ad esempio:

`" fabrikam\kenmyer"`

## <a name="examples"></a>Esempi

L'esempio di PowerShell seguente usa **SWbemLocator** per connettersi a un server.


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMLOCATOR CLSID<br/>                                                          |
| IID<br/>                      | \_ISWBEMLOCATOR IID<br/>                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Oggetti API di scripting](scripting-api-objects.md)
</dt> </dl>

 

 




