---
description: Il \_ Metodo ExecMethod dell'oggetto SWbemObject esegue un metodo esportato da un provider di metodi.
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: Metodo SWbemObject.ExecMethod_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130983"
---
# <a name="swbemobjectexecmethod_-method"></a>Metodo cMethod SWbemObject.Exe\_

Il **metodo \_ ExecMethod** dell'oggetto [**SWbemObject**](swbemobject.md) esegue un metodo esportato da un provider di metodi.

Questo metodo viene sospeso mentre viene eseguito il metodo che viene inviato al provider appropriato. Le informazioni e lo stato vengono quindi restituiti. Il provider anziché WMI implementa il metodo.

Per una spiegazione di questa sintassi, vedere [convenzioni dei documenti per l'API di scripting](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintassi


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*strMethodName* \[ in\]
</dt> <dd>

Obbligatorio. Nome del metodo per l'oggetto.

</dd> <dt>

*objwbemInParams* \[ in, facoltativo\]
</dt> <dd>

Si tratta di un oggetto [**SWbemObject**](swbemobject.md) che contiene i parametri di input per il metodo in esecuzione. Per impostazione predefinita, questo parametro non è definito. Per altre informazioni, vedere [creazione di oggetti InParameters e analisi di oggetti OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ in, facoltativo\]
</dt> <dd>

Riservato e deve essere impostato su 0 (zero) se specificato.

</dd> <dt>

*objwbemNamedValueSet* \[ in, facoltativo\]
</dt> <dd>

In genere, non è definito. In caso contrario, si tratta di un oggetto [**SWbemNamedValueSet**](swbemnamedvalueset.md) i cui elementi rappresentano le informazioni sul contesto che possono essere utilizzate dal provider che sta servendo la richiesta. Un provider che supporta o richiede tali informazioni deve documentare i nomi dei valori riconosciuti, il tipo di dati del valore, i valori consentiti e la semantica.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, viene restituito un oggetto [**SWbemObject**](swbemobject.md) . L'oggetto restituito contiene i parametri out e il valore restituito per il metodo in esecuzione.

## <a name="error-codes"></a>Codici di errore

Dopo il completamento del metodo **ExecMethod \_** , l'oggetto **Err** può contenere uno dei codici di errore elencati di seguito.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Errore non specificato.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

La classe specificata non è valida.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Parametro specificato non valido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Memoria insufficiente per completare l'operazione.

</dd> <dt>

**wbemErrInvalidMethod** -2147749934 (0x8004102E)
</dt> <dd>

Il metodo richiesto non è disponibile.

</dd> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

L'utente corrente non è autorizzato a eseguire il metodo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo metodo è simile a [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), ma opera direttamente sull'oggetto il cui metodo deve essere eseguito. Nell'esempio di codice seguente, ad esempio, viene chiamato il metodo del provider [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) nel [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) e viene utilizzato l' [accesso diretto](manipulating-class-and-instance-information.md).


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



Questa versione chiama **SWbemObject.ExecMethod \_** per eseguire il metodo [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



Usare **SWbemObject.ExecMethod \_** come alternativa all'accesso diretto per l'esecuzione di un [*metodo del provider*](gloss-p.md) nei casi in cui non è possibile eseguire direttamente un metodo. Ad esempio, è possibile usare **SWbemObject.ExecMethod \_** con un linguaggio di scripting che non supporta i parametri di output se il metodo ha parametri out. In caso contrario, la modalità consigliata per richiamare un metodo consiste nell'utilizzare l'accesso diretto.

-   Il **SWbemObject.Exemetodo \_ cMethod** presuppone che l'oggetto rappresentato da [**SWbemObject**](swbemobject.md) contenga il metodo da eseguire. Al contrario, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) richiede un percorso dell'oggetto. Usare **SWbemObject.ExecMethod \_** se è già stato ottenuto l'oggetto di cui si vuole eseguire il metodo.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato il metodo [**ExecMethod**](swbemservices-execmethod.md) . Lo script crea un [**oggetto \_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) che rappresenta un processo che esegue blocco note. Per ulteriori informazioni su uno script che illustra le stesse operazioni eseguite in modo asincrono, vedere [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md). Per un esempio di utilizzo dell'accesso diretto, vedere [**creare un metodo nella classe \_ processo Win32**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) . Per un esempio della stessa operazione usando un oggetto [**SWbemServices**](swbemservices.md) , vedere **SWbemServices.ExecMethod**.


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMOBJECT CLSID<br/>                                                           |
| IID<br/>                      | \_ISWBEMOBJECT IID<br/>                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> </dl>

 

