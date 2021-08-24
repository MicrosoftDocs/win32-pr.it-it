---
description: 'Metodo Shell.GetSystemInformation: recupera le informazioni di sistema.'
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Metodo Shell.GetSystemInformation (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.GetSystemInformation
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 23ad48c673fb0c5925e796f77bd43c77f3abd0afd4511864a5b840214861f792
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660651"
---
# <a name="shellgetsysteminformation-method"></a>Metodo Shell.GetSystemInformation

Recupera le informazioni di sistema.

## <a name="syntax"></a>Sintassi


```JScript
retVal = Shell.GetSystemInformation(
  sName
)
```


```VB

Shell.GetSystemInformation( _
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

**Windows Vista e versioni successive.** Livello del processore. Restituisce 3, 4 o 5, rispettivamente per processori x386, x486 e Pentium.

ProcessorSpeed

**Integer**

Velocità del processore, in megahertz (MHz).

ProcessorArchitecture

**Integer**

Architettura del processore. Per informazioni dettagliate, vedere la descrizione del **membro wProcessorArchitecture** della [**struttura SYSTEM \_ INFO.**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)

PhysicalMemoryInstalled

**Integer**

Quantità di memoria fisica installata, in byte.

Gli elementi seguenti sono validi solo in Windows XP.

IsOS \_ Professional

**Boolean**

Impostare su **true se** il sistema operativo è Windows XP Professional Edition; in caso contrario, **false.**

IsOS \_ Personal

**Boolean**

Impostare su **true se** il sistema operativo è Windows XP Home Edition; in caso contrario, **false.**

Quanto segue è valido solo in Windows XP e versioni successive.

IsOS \_ DomainMember

**Boolean**

Impostare su **true** se il computer è membro di un dominio; in caso contrario, **false.**



 

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Gli esempi seguenti illustrano l'uso **di GetSystemInformation** per JScript e VBScript.

JScript:


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
| Client minimo supportato<br/> | Windows 2000 Professional, Windows solo app \[ desktop XP\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5.0 o successiva)</dt> </dl> |



 

 
