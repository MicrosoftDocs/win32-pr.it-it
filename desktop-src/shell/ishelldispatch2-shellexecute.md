---
description: "Metodo IShellDispatch2.ShellExecute: esegue un'operazione specificata su un file specificato."
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: Metodo IShellDispatch2.ShellExecute (Shldisp.h)
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
ms.openlocfilehash: 8e524ea4a4422e92068d432a91165dfeb97155cfba1d5e6bd9a06ed75b7550cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721036"
---
# <a name="ishelldispatch2shellexecute-method"></a>Metodo IShellDispatch2.ShellExecute

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

*sFile* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** contenente il nome del file in cui **ShellExecute** eseguirà l'azione specificata da *vOperation*.

</dd> <dt>

*vArguments* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variante**

Stringa contenente i valori dei parametri per l'operazione.

</dd> <dt>

*vDirectory* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variante**

Percorso completo della directory che contiene il file specificato da *sFile*. Se questo parametro non viene specificato, viene utilizzata la directory di lavoro corrente.

</dd> <dt>

*vOperation* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variante**

L'operazione da eseguire. Questo valore è impostato su una delle stringhe di verbi supportate dal file. Per una descrizione dei verbi, vedere la sezione Osservazioni. Se questo parametro non viene specificato, viene eseguita l'operazione predefinita.

</dd> <dt>

*vShow* \[ in, facoltativo\]
</dt> <dd>

Tipo: **Variante**

Raccomandazione su come visualizzare inizialmente la finestra dell'applicazione. L'applicazione può ignorare questa raccomandazione. Questo parametro può avere uno dei valori seguenti. Se questo parametro non viene specificato, l'applicazione usa il valore predefinito.



| Valore                                                                                                                               | Significato                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt> <dt>0</dt> </dl>  | Aprire l'applicazione con una finestra nascosta.<br/>                                                                                                    |
| <dl> <dt></dt> <dt>1</dt> </dl>  | Aprire l'applicazione con una finestra normale. Se la finestra è ridotta a icona o ingrandita, il sistema la ripristina alle dimensioni e alla posizione originali.<br/> |
| <dl> <dt></dt> <dt>2</dt> </dl>  | Aprire l'applicazione con una finestra ridotta a icona.<br/>                                                                                                 |
| <dl> <dt></dt> <dt>3</dt> </dl>  | Aprire l'applicazione con una finestra ingrandita.<br/>                                                                                                 |
| <dl> <dt></dt><dt>4</dt> </dl>  | Aprire l'applicazione con la relativa finestra con le dimensioni e la posizione più recenti. La finestra attiva rimane attiva.<br/>                                  |
| <dl> <dt></dt><dt>5</dt> </dl>  | Aprire l'applicazione con la relativa finestra con le dimensioni e la posizione correnti.<br/>                                                                        |
| <dl> <dt></dt> <dt>7</dt> </dl>  | Aprire l'applicazione con una finestra ridotta a icona. La finestra attiva rimane attiva.<br/>                                                               |
| <dl> <dt></dt><dt>10</dt> </dl> | Aprire l'applicazione con la relativa finestra nello stato predefinito specificato dall'applicazione.<br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il [**metodo Shell.ShellExecute.**](./shell-shellexecute.md)

Questo metodo equivale all'avvio di uno dei comandi associati al menu di scelta rapida di un file. Ogni comando è rappresentato da una stringa verbo. Il set di verbi supportati varia da file a file. Il verbo più comunemente supportato è "open", che in genere è anche il verbo predefinito. Altri verbi potrebbero essere supportati solo da determinati tipi di file. Per altre informazioni sui verbi shell, vedere [Avvio di applicazioni](launch.md) o Estensione di menu di scelta [rapida.](context.md)

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso **di ShellExecute per** aprire Blocco note. L'utilizzo viene visualizzato per JScript e VBScript.

JScript:


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



Vbscript:


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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app desktop XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
