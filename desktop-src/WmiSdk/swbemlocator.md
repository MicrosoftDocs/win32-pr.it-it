---
description: È possibile usare i metodi dell'oggetto SWbemLocator per ottenere un oggetto SWbemServices che rappresenta una connessione a uno spazio dei nomi in un computer locale o in un computer host remoto.
ms.assetid: 51ea2c01-04e8-4b1c-bc82-ac96ba8b6eee
ms.tgt_platform: multiple
title: Oggetto SWbemLocator (Wbemdisp.h)
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
ms.openlocfilehash: 0e93e9bd0bfb33c495b30afbde47bcb9b007acb4cd00dece42e1a8c3b88e99d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732792"
---
# <a name="swbemlocator-object"></a>Oggetto SWbemLocator

È possibile usare i metodi dell'oggetto **SWbemLocator** per ottenere un [**oggetto SWbemServices**](swbemservices.md) che rappresenta una connessione a uno spazio dei nomi in un computer locale o in un computer host remoto. È quindi possibile usare i metodi **dell'oggetto SWbemServices** per accedere a WMI. Questo oggetto può essere creato dalla chiamata **CREATEObject** di VBScript.

## <a name="members"></a>Membri

**L'oggetto SWbemLocator** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto SWbemLocator** dispone di questi metodi.



| Metodo                                              | Descrizione                                           |
|:----------------------------------------------------|:------------------------------------------------------|
| [**ConnectServer**](swbemlocator-connectserver.md) | Si connette a WMI nel computer specificato.<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto SWbemLocator** ha queste proprietà.



| Proprietà                                                | Tipo di accesso          | Descrizione                                              |
|:--------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [**Sicurezza\_**](swbemlocator-security-.md)<br/> | Sola lettura<br/> | Consente di leggere o modificare le impostazioni di sicurezza.<br/> |



 

## <a name="remarks"></a>Commenti

All'inizio del modello a oggetti della libreria di scripting WMI è disponibile l'oggetto SWbemLocator. SWbemLocator viene usato per stabilire una connessione autenticata a uno spazio dei nomi WMI, così come la funzione VBScript GetObject e il moniker WMI "winmgmts:" vengono usati per stabilire una connessione autenticata a WMI. Tuttavia, SWbemLocator è progettato per affrontare due scenari di scripting specifici che non possono essere eseguiti usando GetObject e il moniker WMI. È necessario usare SWbemLocator se è necessario:

-   Fornire le credenziali utente e password per connettersi a WMI in un computer remoto. Il moniker WMI usato con la funzione GetObject non include un meccanismo per specificare le credenziali. La maggior parte delle attività WMI (incluse tutte quelle eseguite in computer remoti) richiede diritti di amministratore. Se in genere si esegue l'accesso usando un account utente normale anziché un account amministratore, non sarà possibile eseguire la maggior parte delle attività WMI a meno che non si ese venga eseguito lo script con credenziali alternative.
-   Connessione a WMI se si esegue uno script WMI dall'interno di una pagina Web. Non è possibile usare la funzione GetObject quando si eseguono script incorporati in una pagina HTML Internet Explorer non consente l'uso di GetObject per motivi di sicurezza.

È anche possibile usare SWbemLocator per connettersi a WMI se la stringa di connessione WMI usata con GetObject risulta poco chiara o difficile.

Usare CreateObject anziché GetObject per creare un riferimento a SWbemLocator. Per creare il riferimento, è necessario passare alla funzione CreateObject l'identificatore programmatico SWbemLocator (ProgID) "WbemScripting.SWbemLocator", come illustrato nella riga 2 nell'esempio di script seguente. Dopo aver ottenuto un riferimento a un oggetto SWbemLocator, chiamare il metodo ConnectServer per connettersi a WMI e ottenere un riferimento a un oggetto SWbemServices. Questa operazione viene illustrata alla riga 3 dello script seguente.


```VB
strComputer = "."
Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator")
Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
Set colSWbemObjectSet = objSWbemServices.InstancesOf("Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Per eseguire uno script con credenziali alternative, includere il nome utente e la password come parametri aggiuntivi passati a ConnectServer. Ad esempio, questo script viene eseguito con le credenziali di un utente denominato kenmyer, con la password homerj.


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



È anche possibile usare il formato \\ Nome utente di dominio per specificare un nome utente. Ad esempio:

`" fabrikam\kenmyer"`

## <a name="examples"></a>Esempi

L'esempio di PowerShell seguente **usa SWbemLocator** per connettersi a un server.


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
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemLocator<br/>                                                          |
| IID<br/>                      | IID \_ ISWbemLocator<br/>                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Scripting di oggetti API](scripting-api-objects.md)
</dt> </dl>

 

 




