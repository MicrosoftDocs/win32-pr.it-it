---
description: Recupera le informazioni di sistema.
ms.assetid: 94C10DD6-FE49-4dd4-AEED-69B73A75EDEF
title: Metodo Shell. GetSystemInformation (shldisp. h)
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
ms.openlocfilehash: 2ad7a865ba6ac5b62bc8a9b5ac105c0ef166d574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980626"
---
# <a name="shellgetsysteminformation-method"></a>Shell. GetSystemInformation, metodo

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

*sName* \[ in\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

**Stringa** che specifica le informazioni di sistema richieste.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

### <a name="jscript"></a>JScript

Tipo: **Variant**

Restituisce il valore delle informazioni di sistema richieste. Il tipo restituito dipende dalle informazioni di sistema richieste. Vedere la sezione Osservazioni per informazioni dettagliate.

### <a name="vb"></a>VB

Tipo: **Variant**

Restituisce il valore delle informazioni di sistema richieste. Il tipo restituito dipende dalle informazioni di sistema richieste. Vedere la sezione Osservazioni per informazioni dettagliate.

## <a name="remarks"></a>Commenti

Questo metodo può essere utilizzato per richiedere molti valori di informazioni di sistema. La tabella seguente fornisce il valore *sName* usato per richiedere le informazioni e il tipo associato del valore restituito.



*sName*

Tipo restituito

Descrizione

DirectoryServiceAvailable

**Boolean**

Impostare su **true** se il servizio directory è disponibile; in caso contrario, **false**.

DoubleClickTime

**Integer**

Tempo doppio clic, in millisecondi.

ProcessorLevel

**Integer**

**Windows Vista e versioni successive**. Livello del processore. Restituisce 3, 4 o 5 per i processori a livello di x386, x486 e Pentium, rispettivamente.

ProcessorSpeed

**Integer**

Velocità del processore, in megahertz (MHz).

ProcessorArchitecture

**Integer**

Architettura del processore. Per informazioni dettagliate, vedere la descrizione del membro **wProcessorArchitecture** della struttura [**delle \_ informazioni di sistema**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) .

PhysicalMemoryInstalled

**Integer**

Quantità di memoria fisica installata, in byte.

Gli elementi seguenti sono validi solo in Windows XP.

\_Professional IsOS

**Boolean**

Impostare su **true** se il sistema operativo è Windows XP Professional Edition; in caso contrario, **false**.

\_Personale IsOS

**Boolean**

Impostare su **true** se il sistema operativo è Windows XP Home Edition; in caso contrario, **false**.

Il codice seguente è valido solo in Windows XP e versioni successive.

\_DomainMember IsOS

**Boolean**

Impostare su **true** se il computer è membro di un dominio. in caso contrario, **false**.



 

Questo metodo non è attualmente disponibile in Microsoft Visual Basic.

## <a name="examples"></a>Esempio

Negli esempi seguenti viene illustrato l'utilizzo di **GetSystemInformation** per JScript e VBScript.

JScript


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



VBScript


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
| Client minimo supportato<br/> | Windows 2000 Professional, \[ solo app desktop Windows XP\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versione 5,0 o successiva)</dt> </dl> |



 

 
