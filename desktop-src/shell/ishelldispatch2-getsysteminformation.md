---
description: 'Metodo IShellDispatch2.GetSystemInformation: recupera le informazioni di sistema.'
ms.assetid: 57c066e3-080f-4ecc-b56e-877f0569e901
title: Metodo IShellDispatch2.GetSystemInformation (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a81ac091dc1905c1cbcd2c41575c907ce957e60c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117109"
---
# <a name="ishelldispatch2getsysteminformation-method"></a>Metodo IShellDispatch2.GetSystemInformation

Recupera le informazioni di sistema.

## <a name="syntax"></a>Sintassi


```JScript
retVal = IShellDispatch2.GetSystemInformation(
  sName
)
```


```VB

IShellDispatch2.GetSystemInformation( _
  ByVal sName As BSTR _
) As Variant
```





## <a name="parameters"></a>Parametri

<dl> <dt>

*sName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Valore **String** che specifica le informazioni di sistema richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **Variante**

Restituisce il valore delle informazioni di sistema richieste. Il tipo restituito dipende dalle informazioni di sistema richieste. Vedere la sezione Osservazioni per informazioni dettagliate.

### <a name="vb"></a>VB

Tipo: **Variante**

Restituisce il valore delle informazioni di sistema richieste. Il tipo restituito dipende dalle informazioni di sistema richieste. Vedere la sezione Osservazioni per informazioni dettagliate.

## <a name="remarks"></a>Commenti

Questo metodo viene implementato e accessibile tramite il [**metodo Shell.GetSystemInformation.**](./shell-getsysteminformation.md)

Questo metodo può essere usato per richiedere molti valori di informazioni di sistema. Nella tabella seguente viene specificato *il valore sName* usato per richiedere le informazioni e il tipo associato del valore restituito.



*sName*

Tipo restituito

Descrizione

DirectoryServiceAvailable

**Boolean**

Impostare su **true se** il servizio directory è disponibile. in caso contrario, **false.**

DoubleClickTime

**Integer**

Tempo di doppio clic, in millisecondi.

ProcessorLevel

**Integer**

**Windows Vista e versioni successive.** Livello del processore. Restituisce rispettivamente 3, 4 o 5 per i processori x386, x486 e Pentium.

ProcessorSpeed

**Integer**

Velocità del processore, in megahertz (MHz).

ProcessorArchitecture

**Integer**

Architettura del processore. Per informazioni dettagliate, vedere la discussione sul **membro wProcessorArchitecture** della [**struttura SYSTEM \_ INFO.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)

PhysicalMemoryInstalled

**Integer**

Quantità di memoria fisica installata, in byte.

Gli elementi seguenti sono validi solo in Windows XP.

IsOS \_ Professional

**Boolean**

Impostare su **true se** il sistema operativo è Windows XP Professional Edition; in caso contrario, **false**.

IsOS \_ Personal

**Boolean**

Impostare su **true se** il sistema operativo è Windows XP Home Edition; in caso contrario, **false**.

Quanto segue è valido solo in Windows XP e versioni successive.

Membro di dominio IsOS \_

**Boolean**

Impostare su **true se** il computer è membro di un dominio. in caso contrario, **false**.



 

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso **di GetSystemInformation** per JScript e VBScript.

Jscript:


```JScript
<script language="JavaScript">
    function fnGetSystemInformationJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var vReturn;

        vReturn = objShell.GetSystemInformation("ProcessorLevel");
        document.write(vReturn);
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnGetSystemInformationVB()
        dim objShell
        dim vReturn

        set objShell = CreateObject("shell.application")

        vReturn = objShell.GetSystemInformation("ProcessorLevel")
        document.write(vReturn)

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional, solo app desktop di Windows XP \[\]<br/>                                        |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
