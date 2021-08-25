---
description: metodo Shell.FindComputer - 'Visualizza la finestra di dialogo Risultati ricerca: Computer. Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specificato."
ms.assetid: 0304b955-afde-4de4-824a-9ec9c9530360 title: Shell.FindComputer method (Shldisp.h) ms.topic: reference ms.date: 05/31/2018 topic_type: 
- APIRef
- kbSyntax api_name: 
- Shell.FindComputer api_type: 
- Com api_location: 
- Shell32.dll
---

# <a name="shellfindcomputer-method"></a>Metodo Shell.FindComputer

Visualizza la **finestra di dialogo Risultati ricerca:** Computer . Nella finestra di dialogo viene visualizzato il risultato della ricerca di un computer specificato.

## <a name="syntax"></a>Sintassi


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Questo metodo non restituisce valori.

### <a name="vb"></a>VB

Questo metodo non restituisce valori.

## <a name="examples"></a>Esempio

L'esempio seguente mostra **FindComputer** in uso. Il risultato di questo codice è identico a quello che si verifica quando si preme il pulsante **Start,** si fa clic su Cerca **,** si fa clic sull'opzione **Stampanti,** computer o persone , quindi si fa clic su Un **computer nella rete**. Viene visualizzato l'utilizzo corretto JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                         |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                                           |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 4.71 o successiva)</dt> </dl> |



 

 




