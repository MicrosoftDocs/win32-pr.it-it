---
description: "Metodo Shell.ShellExecute: esegue un'operazione specificata su un file specificato."
ms.assetid: 62E59A1C-51BD-4864-AF09-35FFD49FAB9D
title: Metodo Shell.ShellExecute (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0fd31f0859fff5a1c94d5586f287e4a8980ddc02
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104129"
---
# <a name="shellshellexecute-method"></a>Metodo Shell.ShellExecute

Esegue un'operazione specificata su un file specificato.

## <a name="syntax"></a>Sintassi

Jscript:

```js
iRetVal = Shell.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
);
```

Vbscript:

```vb
iRetVal = Shell.ShellExecute( _
  sFile, _
  [ ByVal vArguments ], _
  [ ByVal vDirectory ], _
  [ ByVal vOperation ], _
  [ ByVal vShow ] _
)
```

VB:

```vb
Shell.ShellExecute( _
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

Stringa **contenente** il nome del file in cui **ShellExecute** eseguirà l'azione specificata da *vOperation*.

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

Tipo: **Variant**

Raccomandazione su come visualizzare inizialmente la finestra dell'applicazione. L'applicazione può ignorare questa raccomandazione. Questo parametro può avere uno dei valori seguenti. Se questo parametro non viene specificato, l'applicazione usa il valore predefinito.



| Valore                                                                                                                               | Significato                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>0</dt> </dl>  | Aprire l'applicazione con una finestra nascosta.<br/>                                                                                                    |
| <dl> <dt></dt> <dt>1</dt> </dl>  | Aprire l'applicazione con una finestra normale. Se la finestra è ridotta a icona o ingrandita, il sistema ripristina le dimensioni e la posizione originali.<br/> |
| <dl> <dt></dt> <dt>2</dt> </dl>  | Aprire l'applicazione con una finestra ridotta a icona.<br/>                                                                                                 |
| <dl> <dt></dt> <dt>3</dt> </dl>  | Aprire l'applicazione con una finestra ingrandita.<br/>                                                                                                 |
| <dl> <dt></dt><dt>4</dt> </dl>  | Aprire l'applicazione con la relativa finestra con le dimensioni e la posizione più recenti. La finestra attiva rimane attiva.<br/>                                  |
| <dl> <dt></dt><dt>5</dt> </dl>  | Aprire l'applicazione con la relativa finestra con le dimensioni e la posizione correnti.<br/>                                                                        |
| <dl> <dt></dt><dt>7</dt> </dl>  | Aprire l'applicazione con una finestra ridotta a icona. La finestra attiva rimane attiva.<br/>                                                               |
| <dl> <dt></dt><dt>10</dt> </dl> | Aprire l'applicazione con la relativa finestra nello stato predefinito specificato dall'applicazione.<br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo metodo equivale all'avvio di uno dei comandi associati al menu di scelta rapida di un file. Ogni comando è rappresentato da una stringa verbo. Il set di verbi supportati varia da file a file. Il verbo più comunemente supportato è "open", che in genere è anche il verbo predefinito. Altri verbi potrebbero essere supportati solo da determinati tipi di file. Per altre informazioni sui verbi shell, vedere [Avvio di applicazioni](launch.md) o Estensione di menu di scelta [rapida.](context.md)

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso **di ShellExecute per** aprire il Blocco note. L'utilizzo è illustrato per JScript e VBScript.

Jscript:


```JScript
function ShellExecuteJS()
{
    var objShell = new ActiveXObject("Shell.Application");
    objShell.ShellExecute("notepad.exe", "", "", "open", 1);
}
```

Vbscript:

```vb
Function ShellExecuteVB()
    Dim objShell
    Set objShell = CreateObject("Shell.Application")
    Call objShell.ShellExecute("notepad.exe", "", "", "open", 1)
End Function
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Solo app desktop windows 2000 Professional e Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
