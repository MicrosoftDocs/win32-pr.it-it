---
description: Esegue un'operazione specificata su un file specificato.
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: Metodo IShellDispatch2. ShellExecute (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: ed5a8a2732f8ca358a0582d1da23aa7ffa7a98df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978023"
---
# <a name="ishelldispatch2shellexecute-method"></a>IShellDispatch2. ShellExecute, metodo

Esegue un'operazione specificata su un file specificato.

## <a name="syntax"></a>Sintassi


```JScript
iRetVal = IShellDispatch2.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
)
```


```VB

IShellDispatch2.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*sfile* \[ in\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Stringa** che contiene il nome del file in cui **ShellExecute** eseguirà l'azione specificata da *vOperation*.

</dd> <dt>

*vArguments* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

Stringa che contiene i valori dei parametri per l'operazione.

</dd> <dt>

*vDirectory* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

Percorso completo della directory che contiene il file specificato da *sfile*. Se questo parametro non viene specificato, viene utilizzata la directory di lavoro corrente.

</dd> <dt>

*vOperation* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

L'operazione da eseguire. Questo valore è impostato su una delle stringhe dei verbi supportate dal file. Per informazioni sui verbi, vedere la sezione Osservazioni. Se questo parametro non viene specificato, viene eseguita l'operazione predefinita.

</dd> <dt>

*vShow* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variant**

Indicazione relativa alla modalità di visualizzazione iniziale della finestra dell'applicazione. Questa raccomandazione può essere ignorata dall'applicazione. Questo parametro può avere uno dei valori seguenti. Se questo parametro non viene specificato, l'applicazione utilizzerà il relativo valore predefinito.



| Valore                                                                                                                               | Significato                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>0</dt> </dl>  | Aprire l'applicazione con una finestra nascosta.<br/>                                                                                                    |
| <dl> <dt></dt> <dt>1</dt> </dl>  | Aprire l'applicazione con una finestra normale. Se la finestra è ridotta a icona o ingrandita, il sistema ripristina le dimensioni e la posizione originali.<br/> |
| <dl> <dt></dt> <dt>2</dt> </dl>  | Aprire l'applicazione con una finestra ridotta a icona.<br/>                                                                                                 |
| <dl> <dt></dt> <dt>3</dt> </dl>  | Aprire l'applicazione con una finestra ingrandita.<br/>                                                                                                 |
| <dl> <dt></dt><dt>4</dt> </dl>  | Aprire l'applicazione con la relativa finestra con le dimensioni e la posizione più recenti. La finestra attiva rimane attiva.<br/>                                  |
| <dl> <dt></dt><dt>5</dt> </dl>  | Aprire l'applicazione con la relativa finestra in corrispondenza delle dimensioni e della posizione correnti.<br/>                                                                        |
| <dl> <dt></dt><dt>7</dt> </dl>  | Aprire l'applicazione con una finestra ridotta a icona. La finestra attiva rimane attiva.<br/>                                                               |
| <dl> <dt></dt><dt>10</dt> </dl> | Aprire l'applicazione con la relativa finestra nello stato predefinito specificato dall'applicazione.<br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il metodo [**Shell. ShellExecute**](./shell-shellexecute.md) .

Questo metodo equivale a avviare uno dei comandi associati al menu di scelta rapida di un file. Ogni comando è rappresentato da una stringa verbo. Il set di verbi supportati varia da file a file. Il verbo più comunemente supportato è "Open", che è in genere anche il verbo predefinito. Altri verbi possono essere supportati solo da determinati tipi di file. Per ulteriori informazioni sui verbi della shell, vedere [avvio di applicazioni](launch.md) o [estensione dei menu di scelta rapida](context.md).

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo di **ShellExecute** per aprire il blocco note. L'utilizzo viene visualizzato per JScript e VBScript.

JScript


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellExecuteVB()
        dim objShell

        set objShell = CreateObject("shell.application")

        objShell.ShellExecute "notepad.exe", "", "", "open", 1

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



 

 
