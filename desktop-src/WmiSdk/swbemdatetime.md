---
description: L'oggetto SWbemDateTime è un oggetto helper per analizzare e Common Information Model valori datetime (CIM).
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: Oggetto SWbemDateTime (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 25f8b04aa8c581d8d7e40ab1d52162d305c97d0d8ce3f7d626cb3d29e7262666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050089"
---
# <a name="swbemdatetime-object"></a>Oggetto SWbemDateTime

**L'oggetto SWbemDateTime** è un oggetto helper per analizzare e Common Information Model valori [datetime](datetime.md) (CIM). Svolge un ruolo simile a [**SWbemObjectPath,**](swbemobjectpath.md)che fornisce assistenza per formattare e interpretare i percorsi degli oggetti. È possibile usare la chiamata [a VBScript CreateObject](/previous-versions//xzysf6hc(v=vs.85)) per creare **l'oggetto SWbemDateTime.**

Un **oggetto SWbemDateTime** può essere inizializzato da e formattato in valori **\_ VT DATE** o **FILETIME** usando i metodi sull'oggetto . Usando le proprietà dell'oggetto , il valore può essere analizzato in anno, mese, giorno, ora, minuti, secondi o microsecondi componente. **L'oggetto SWbemDateTime** può essere formattato in valori locali o Coordinated Universal Time (UTC). Per altre informazioni, vedere [Formato di data e ora.](date-and-time-format.md)

**SWbemDateTime è** l'unico oggetto di scripting Windows Management Instrumentation (WMI) contrassegnato come sicuro per l'inizializzazione e gli script in esecuzione nelle pagine HTML in Internet Explorer.

## <a name="members"></a>Membri

**L'oggetto SWbemDateTime** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto SWbemDateTime** dispone di questi metodi.



| Metodo                                           | Descrizione                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**GetFileTime**](swbemdatetime-getfiletime.md) | Converte una **data e un'ora FILETIME,** espresse come **BSTR,** in un [formato DATETIME](datetime.md) WMI.<br/> |
| [**GetVarDate**](swbemdatetime-getvardate.md)   | Converte un valore di data e ora in formato [DATETIME](datetime.md) WMI in un **valore DATE \_ VT.**<br/>                  |
| [**SetFileTime**](swbemdatetime-setfiletime.md) | Converte un formato [DATETIME](datetime.md) WMI in una data e un'ora **FILETIME,** espresse come **BSTR.**<br/>  |
| [**SetVarDate**](swbemdatetime-setvardate.md)   | Converte una **data e \_ un'ora in** formato DATE VT in un oggetto [DATETIME](datetime.md)WMI.<br/>                        |



 

### <a name="properties"></a>Proprietà

**L'oggetto SWbemDateTime** ha queste proprietà.



| Proprietà                                                                        | Tipo di accesso           | Descrizione                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**Giorno**](swbemdatetime-day.md)<br/>                                     | Lettura/Scrittura<br/> | Componente giorno di un valore [datetime](datetime.md) CIM.<br/>                                                           |
| [**DaySpecified**](swbemdatetime-dayspecified.md)<br/>                   | Lettura/Scrittura<br/> | Indica se il giorno viene specificato o lasciato come carattere jolly.<br/>                                                        |
| [**Hours**](swbemdatetime-hours.md)<br/>                                 | Lettura/Scrittura<br/> | Ore del componente giorno di un valore [datetime](datetime.md) CIM.<br/>                                              |
| [**HoursSpecified**](swbemdatetime-hoursspecified.md)<br/>               | Lettura/Scrittura<br/> | Indica se l'ora viene specificata o lasciata come carattere jolly.<br/>                                                       |
| [**IsInterval**](swbemdatetime-isinterval.md)<br/>                       | Lettura/Scrittura<br/> | Indica che almeno un componente del valore [datetime](datetime.md) CIM rappresenta un intervallo anziché una data.<br/> |
| [**Microseconds**](swbemdatetime-microseconds.md)<br/>                   | Lettura/Scrittura<br/> | Componente dei microsecondi di un valore [datetime](datetime.md) CIM.<br/>                                                  |
| [**MicrosecondiSpecificati**](swbemdatetime-microsecondsspecified.md)<br/> | Lettura/Scrittura<br/> | Indica se il componente microsecondi viene specificato o lasciato come carattere jolly.<br/>                                     |
| [**Minuti**](swbemdatetime-minutes.md)<br/>                             | Lettura/Scrittura<br/> | Componente minuti di un valore [datetime](datetime.md) CIM.<br/>                                                       |
| [**MinutesSpecified**](swbemdatetime-minutesspecified.md)<br/>           | Lettura/Scrittura<br/> | Indica se il componente minuti viene specificato o lasciato come carattere jolly.<br/>                                          |
| [**Mese**](swbemdatetime-month.md)<br/>                                 | Lettura/Scrittura<br/> | Componente relativo al mese di un valore [datetime](datetime.md) CIM.<br/>                                                         |
| [**MonthSpecified**](swbemdatetime-monthspecified.md)<br/>               | Lettura/Scrittura<br/> | Indica se il mese viene specificato o lasciato come carattere jolly.<br/>                                                      |
| [**Secondi**](swbemdatetime-seconds.md)<br/>                             | Lettura/Scrittura<br/> | Componente secondi di un valore [datetime](datetime.md) CIM.<br/>                                                       |
| [**SecondsSpecified**](swbemdatetime-secondsspecified.md)<br/>           | Lettura/Scrittura<br/> | Indica se il componente secondi viene specificato o lasciato come carattere jolly.<br/>                                          |
| [**Utc**](swbemdatetime-utc.md)<br/>                                     | Lettura/Scrittura<br/> | Componente UTC di un valore [datetime](datetime.md) CIM.<br/>                                                           |
| [**UTCSpecified**](swbemdatetime-utcspecified.md)<br/>                   | Lettura/Scrittura<br/> | Indica se il componente UTC viene specificato o lasciato come carattere jolly.<br/>                                              |
| [**Valore**](swbemdatetime-value.md)<br/>                                 | Lettura/Scrittura<br/> | Valore [datetime](datetime.md) CIM completo.<br/>                                                                         |
| [**Year**](swbemdatetime-year.md)<br/>                                   | Lettura/Scrittura<br/> | Componente anno di un valore [datetime](datetime.md) CIM.<br/>                                                          |
| [**YearSpecified**](swbemdatetime-yearspecified.md)<br/>                 | Lettura/Scrittura<br/> | Indica se l'anno viene specificato o lasciato come carattere jolly.<br/>                                                |



 

## <a name="remarks"></a>Commenti

WMI registra i timestamp nel formato UTC (Universal Time Coordinate). L'ora UTC non è il formato utilizzato dalla maggior parte degli sviluppatori e degli amministratori IT. Di conseguenza, un problema comune è determinare come convertire l'ora UTC in un elemento più leggibile. Per altre informazioni su come usare l'ora UTC, vedere [Wmi Tasks: Dates and Times](wmi-tasks--dates-and-times.md) (Attività WMI: date e ore) e Working with Dates and Times using WMI (Uso di date e ore con [WMI).](/previous-versions/tn-archive/ee198928(v=technet.10)) Per altre informazioni, è anche possibile leggere i post di blog [It s About Time (Oh, and About Dates, Too)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) e How Can I Subtract a Specified Number of Days from a UTC Value? (Come è possibile sottrarre un numero specificato di giorni da un valore [UTC?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) ) per altre informazioni.

Qualsiasi campo numerico può avere un valore jolly se la [**proprietà IsInterval**](swbemdatetime-isinterval.md) è impostata su **FALSE.** I campi con valori jolly contengono asterischi nell'intero campo.

Ogni proprietà, ad esempio [**Day,**](swbemdatetime-day.md)ha un valore booleano specificato corrispondente, ad [**esempio DaySpecified.**](swbemdatetime-dayspecified.md) Quando **DaySpecified** è **FALSE,** il valore viene interpretato come un intervallo anziché come un numero compreso tra 01 e 31. Se viene usato un intervallo in un punto qualsiasi del valore [datetime](datetime.md) CIM, [**anche IsInterval**](swbemdatetime-isinterval.md) viene impostato su **TRUE.** Il valore predefinito è che un valore datetime CIM deve contenere una data anziché uno o più intervalli.

Ad esempio, se [**SWbemDateTime.DaySpecified**](swbemdatetime-dayspecified.md) è **TRUE,** [**SWbemDateTime.Value**](swbemdatetime-value.md) include il valore corrente [**di SWbemDateTime.Day**](swbemdatetime-day.md), in caso contrario è un valore con caratteri jolly. In entrambi i casi, la proprietà [**IsInterval**](swbemdatetime-isinterval.md) **è FALSE.**

## <a name="examples"></a>Esempio

Nell'esempio di codice di script seguente viene illustrato come usare un **oggetto SWbemDateTime** per analizzare un valore di proprietà datetime letto dal repository WMI, la **proprietà InstallDate** in [**Win32 \_ OperatingSystem**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



L'esempio seguente illustra come creare un **oggetto SWbemDateTime,** archiviare un valore di data nell'oggetto , visualizzare la data come locale e Coordinated Universal Time (UTC) e archiviare il valore in una classe e in una proprietà appena create. Per altre informazioni sulla costante **wbemCimtypeDatetime**, vedere [WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



Nell'esempio di codice di script seguente viene illustrato come usare un **oggetto SWbemDateTime** per modificare un valore di intervallo in una proprietà letta dal repository WMI.


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



Nell'esempio di codice di script seguente viene illustrato come usare un **oggetto SWbemDate** per leggere un **valore FILETIME.**


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



Il codice di PowerShell seguente crea un'istanza di un oggetto SWbemDateTime, recupera la data di installazione del sistema operativo e converte la data in un formato diverso


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



Il codice di PowerShell seguente converte il codice in un formato pronto per essere utilizzato da un provider CIM.


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemDateTime<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemDateTime<br/>                                                          |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[WbemCimtypeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[Datetime](datetime.md)
</dt> <dt>

[Scripting di oggetti API](scripting-api-objects.md)
</dt> </dl>

 

