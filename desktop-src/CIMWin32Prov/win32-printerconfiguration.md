---
description: La \_ classe WMI PrinterConfiguration Win32 rappresenta la configurazione per un dispositivo stampante. Sono incluse funzionalità quali la risoluzione, il colore, i tipi di carattere e l'orientamento.
ms.assetid: b6649da0-ecb0-4ed1-979c-5005837eb474
ms.tgt_platform: multiple
title: Classe Win32_PrinterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterConfiguration
- Win32_PrinterConfiguration.Caption
- Win32_PrinterConfiguration.Description
- Win32_PrinterConfiguration.SettingID
- Win32_PrinterConfiguration.BitsPerPel
- Win32_PrinterConfiguration.Collate
- Win32_PrinterConfiguration.Color
- Win32_PrinterConfiguration.Copies
- Win32_PrinterConfiguration.DeviceName
- Win32_PrinterConfiguration.DisplayFlags
- Win32_PrinterConfiguration.DisplayFrequency
- Win32_PrinterConfiguration.DitherType
- Win32_PrinterConfiguration.DriverVersion
- Win32_PrinterConfiguration.Duplex
- Win32_PrinterConfiguration.FormName
- Win32_PrinterConfiguration.HorizontalResolution
- Win32_PrinterConfiguration.ICMIntent
- Win32_PrinterConfiguration.ICMMethod
- Win32_PrinterConfiguration.LogPixels
- Win32_PrinterConfiguration.MediaType
- Win32_PrinterConfiguration.Name
- Win32_PrinterConfiguration.Orientation
- Win32_PrinterConfiguration.PaperLength
- Win32_PrinterConfiguration.PaperSize
- Win32_PrinterConfiguration.PaperWidth
- Win32_PrinterConfiguration.PelsHeight
- Win32_PrinterConfiguration.PelsWidth
- Win32_PrinterConfiguration.PrintQuality
- Win32_PrinterConfiguration.Scale
- Win32_PrinterConfiguration.SpecificationVersion
- Win32_PrinterConfiguration.TTOption
- Win32_PrinterConfiguration.VerticalResolution
- Win32_PrinterConfiguration.XResolution
- Win32_PrinterConfiguration.YResolution
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1927144484dbf427358735fc9d8ed66da56f3d8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966261"
---
# <a name="win32_printerconfiguration-class"></a>Win32 \_ PrinterConfiguration (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PrinterConfiguration Win32** rappresenta la configurazione per un dispositivo stampante. Sono incluse funzionalità quali la risoluzione, il colore, i tipi di carattere e l'orientamento.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_PrinterConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  uint32  BitsPerPel;
  boolean Collate;
  uint32  Color;
  uint32  Copies;
  string  DeviceName;
  uint32  DisplayFlags;
  uint32  DisplayFrequency;
  uint32  DitherType;
  uint32  DriverVersion;
  boolean Duplex;
  string  FormName;
  uint32  HorizontalResolution;
  uint32  ICMIntent;
  uint32  ICMMethod;
  uint32  LogPixels;
  uint32  MediaType;
  string  Name;
  uint32  Orientation;
  uint32  PaperLength;
  string  PaperSize;
  uint32  PaperWidth;
  uint32  PelsHeight;
  uint32  PelsWidth;
  uint32  PrintQuality;
  uint32  Scale;
  uint32  SpecificationVersion;
  uint32  TTOption;
  uint32  VerticalResolution;
  uint32  XResolution;
  uint32  YResolution;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ PrinterConfiguration** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ PrinterConfiguration** dispone di queste proprietà.

<dl> <dt>

**BitsPerPel**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Numero di bit utilizzati per rappresentare il colore in questa configurazione (bit per pixel). Questa proprietà è obsoleta. Usare invece le proprietà nelle classi [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) per determinare il modo in cui viene rappresentato il colore.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**Fascicola**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, le pagine stampate devono essere confrontate. Per eseguire l'ordinamento è necessario stampare l'intero documento prima di stampare la copia successiva, anziché stampare ogni pagina del documento per il numero di volte necessario.

Questa proprietà viene ignorata a meno che il driver della stampante non indichi il supporto per le regole di confronto.

</dd> <dt>

**Colore**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Colore del documento. Alcune stampanti a colori hanno la possibilità di stampare usando il vero nero anziché una combinazione di cyan, magenta e Yellow (CMY). In genere viene creato un testo più scuro e più nitido per i documenti. Questa opzione è utile solo per le stampanti a colori che supportano la stampa true nero.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Monocromatico (vero nero)

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Colore

</dd> </dl>

</dd> <dt>

**Copie**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di copie da stampare. Il driver della stampante deve supportare la stampa di copie a più pagine.

Esempio: 2

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione testuale dell'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**DeviceName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome descrittivo della stampante. Questo nome è univoco per il tipo di stampante e può essere troncato a causa delle limitazioni della stringa da cui è derivato.

Esempio: "PCL/HP LaserJet"

</dd> <dt>

**DisplayFlags**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se il dispositivo di visualizzazione è colorato o monocromatico e se il tipo di analisi non è interlacciato o interlacciato. Questa proprietà è obsoleta. Usare invece le proprietà di visualizzazione, ad esempio la proprietà **DisplayType** della classe **\_ DesktopMonitor Win32** .

</dd> <dt>

**DisplayFrequency**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Visualizza la frequenza di aggiornamento verticale. La frequenza di aggiornamento per un monitoraggio è il numero di volte in cui lo schermo viene ridisegnato al secondo (frequenza). Questa proprietà è obsoleta. Usare invece le proprietà nella classe [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)o [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) .

</dd> <dt>

**DitherType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di dithering della stampante. Questa proprietà può assumere valori predefiniti da 1 a 5 o da 6 a 256 per i valori definiti dal driver. Il rethering dell'arte linea è un metodo speciale che produce bordi ben definiti tra le scalature di nero, bianco e grigio. Non è adatta per le immagini che includono la graduazione continua in intensità e tonalità, ad esempio le fotografie analizzate.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Nessuna retinatura

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Pennello grossolano

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Pennello fine

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Linea artistica

</dd> <dt>

<span id="5"></span>

<span id="5"></span>**5**


</dt> <dd>

Gradazioni di grigio

</dd> </dl>

</dd> <dt>

**DriverVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di versione del driver della stampante basato su Windows. I numeri di versione vengono creati e gestiti dal produttore del driver.

</dd> <dt>

**Duplex**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Se **true**, la stampa viene eseguita su entrambi i lati. Se **false**, la stampa viene eseguita su un solo lato del supporto.

</dd> <dt>

**Nomemodulo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Non supportata.

</dd> <dt>

**HorizontalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) (punti per pollice)
</dt> </dl>

Risoluzione di stampa espressa in punti per pollice lungo l'asse x (larghezza) del processo di stampa (simile alla proprietà **XResolution** obsoleta). Questo valore viene impostato solo quando la proprietà **PrintQuality** di questa classe è positiva.

</dd> <dt>

**ICMIntent**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Valore specifico di uno dei tre possibili metodi di corrispondenza dei colori (detti Intent) che devono essere utilizzati per impostazione predefinita. Le applicazioni ICM stabiliscono gli Intent usando le funzioni ICM. Questa proprietà può assumere valori predefiniti compresi tra 1 e 3 o i valori definiti dal driver da 4 a 256. Le applicazioni non ICM possono utilizzare questo valore per determinare il modo in cui la stampante gestisce i processi di stampa dei colori.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Saturazione

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Si confronti

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Colore esatto

</dd> </dl>

</dd> <dt>

**ICMMethod**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Modalità di gestione di ICM. Per un'applicazione non ICM, questa proprietà determina se ICM è abilitato o disabilitato. Per le applicazioni ICM, il sistema esamina questa proprietà per determinare quale parte del sistema del computer gestisce il supporto ICM.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Disabled

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Windows

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Driver di dispositivo

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Dispositivo

</dd> </dl>

</dd> <dt>

**LogPixels**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Numero di pixel per pollice logico. Questa proprietà obsoleta è valida solo con i dispositivi che funzionano con pixel, che esclude i dispositivi come le stampanti. Non esiste alcun valore sostitutivo applicabile alle stampanti.

</dd> <dt>

**MediaType**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Tipo di supporto su cui stampa la stampante. La proprietà può essere impostata su un valore predefinito o su un valore definito dal driver maggiore o uguale a 256.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Standard

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Trasparenza

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**3**


</dt> <dd>

Lucido

</dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Key**](../wmisdk/standard-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome della stampante a cui è associata questa configurazione. Questo valore corrisponde alla proprietà **Name** dell'istanza della [**\_ stampante Win32**](win32-printer.md) associata.

</dd> <dt>

**Orientamento**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Orientamento di stampa del documento.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Verticale

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Orizzontale

</dd> </dl>

</dd> <dt>

**PaperLength**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) (decimi di millimetro)
</dt> </dl>

Lunghezza del documento. Per determinare le dimensioni del foglio in pollici, dividere il valore per 254.

Esempio: 2794

</dd> <dt>

**PaperSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni del foglio. Le dimensioni possibili si trovano nella proprietà **PaperSizesSupported** della classe [**\_ Printer Win32**](win32-printer.md) associata.

Esempio: "a4 o Letter".

</dd> <dt>

**PaperWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) (decimi di millimetro)
</dt> </dl>

Larghezza del foglio. Per determinare le dimensioni del foglio in pollici, dividere il valore per 254.

Esempio: 2159

</dd> <dt>

**PelsHeight**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Questa proprietà non è supportata.

</dd> <dt>

**PelsWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Questa proprietà non è supportata.

</dd> <dt>

**PrintQuality**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Uno dei quattro livelli di qualità del processo di stampa. Se viene specificato un valore positivo, la qualità viene misurata in punti per pollice.

<dt>

<span id="-1"></span>

<span id="-1"></span>**-1**


</dt> <dd>

Bozza

</dd> <dt>

<span id="-2"></span>

<span id="-2"></span>**2**


</dt> <dd>

Basso

</dd> <dt>

<span id="-3"></span>

<span id="-3"></span>**-3**


</dt> <dd>

Medio

</dd> <dt>

<span id="-4"></span>

<span id="-4"></span>**-4**


</dt> <dd>

Alto

</dd> </dl>

</dd> <dt>

**Ridimensiona**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) (percentuale)
</dt> </dl>

Fattore di ridimensionamento dell'output stampato. Una scala 75, ad esempio, riduce l'output di stampa a 3/4 l'altezza e la larghezza originali.

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificatore con cui è noto l'oggetto corrente.

Questa proprietà viene ereditata [**dall' \_ impostazione CIM**](cim-setting.md).

</dd> <dt>

**SpecificationVersion**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di versione dei dati di inizializzazione per il dispositivo associato alla stampante basata su Windows.

</dd> <dt>

**TTOption**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica la modalità di stampa di tipi di carattere TrueType.

<dt>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>

<span id="Bitmap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap** (1)


</dt> <dd>

Stampa i tipi di carattere TrueType come grafici. Si tratta dell'azione predefinita per le stampanti a matrice di punti.

</dd> <dt>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>

<span id="Download"></span><span id="download"></span><span id="DOWNLOAD"></span>**Download** (2)


</dt> <dd>

Scarica i tipi di carattere TrueType come caratteri soft. Si tratta dell'azione predefinita per le stampanti che utilizzano il linguaggio di controllo della stampante (PCL).

</dd> <dt>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>

<span id="Substitute"></span><span id="substitute"></span><span id="SUBSTITUTE"></span>**Sostituisci** (3)


</dt> <dd>

Sostituisce i tipi di carattere del dispositivo per i tipi di carattere TrueType. Si tratta dell'azione predefinita per le stampanti PostScript.

</dd> </dl>

</dd> <dt>

**VerticalResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) (punti per pollice)
</dt> </dl>

Risoluzione di stampa lungo l'asse y (altezza) del processo di stampa, simile alla proprietà **YResolution** obsoleta. Questo valore viene impostato solo quando la proprietà **PrintQuality** di questa classe è positiva.

</dd> <dt>

**XResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Questa proprietà è obsoleta. In alternativa, usare la proprietà **HorizontalResolution** .

</dd> <dt>

**YResolution**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **deprecato**](../wmisdk/standard-wmi-qualifiers.md)
</dt> </dl>

Questa proprietà è obsoleta. In alternativa, usare la proprietà **VerticalResolution** .

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ PrinterConfiguration** deriva dall' [**\_ impostazione CIM**](cim-setting.md).

**Overview**

Prima di poter determinare come distribuire e utilizzare al meglio le risorse di stampa, è necessario disporre di una conoscenza approfondita di tali risorse. Ad esempio, il reparto A può avere solo tre stampanti rispetto a cinque stampanti nel reparto B. Tuttavia, se le stampanti nel reparto A possono stampare 20 pagine al minuto e le stampanti nel reparto B possono stampare solo 5 pagine al minuto, gli utenti nel reparto A hanno effettivamente una maggiore capacità di stampa. Se non si conoscono le funzionalità dettagliate di queste stampanti, è possibile che si concluda erroneamente che un reparto A è breve sulla capacità di stampa e quindi si acquistano altre stampanti che finiscono inutilizzate.

WMI include due classi, [**\_ Printer Win32**](win32-printer.md) e **Win32 \_ PrinterConfiguration**, che possono essere utilizzate per restituire informazioni dettagliate su tutte le stampanti installate in un computer.

## <a name="examples"></a>Esempio

Nell'esempio di codice seguente vengono recuperate le informazioni sulla stampante.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colInstalledPrinters = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_PrinterConfiguration")
For Each objPrinter in colInstalledPrinters
 Wscript.Echo "Name: " & objPrinter.Name
 Wscript.Echo "Collate: " & objPrinter.Collate
 Wscript.Echo "Copies: " & objPrinter.Copies
 Wscript.Echo "Driver Version: " & objPrinter.DriverVersion
 Wscript.Echo "Duplex: " & objPrinter.Duplex
 Wscript.Echo "Horizontal Resolution: " & _
 objPrinter.HorizontalResolution
 If objPrinter.Orientation = 1 Then
 strOrientation = "Portrait"
 Else
 strOrientation = "Landscape"
 End If
 Wscript.Echo "Orientation : " & strOrientation
 Wscript.Echo "Paper Length: " & objPrinter.PaperLength / 254
 Wscript.Echo "Paper Width: " & objPrinter.PaperWidth / 254
 Wscript.Echo "Print Quality: " & objPrinter.PrintQuality
 Wscript.Echo "Scale: " & objPrinter.Scale
 Wscript.Echo "Specification Version: " & _
 objPrinter.SpecificationVersion
 If objPrinter.TTOption = 1 Then
 strTTOption = "Print TrueType fonts as graphics."
 ElseIf objPrinter.TTOption = 2 Then
 strTTOption = "Download TrueType fonts as soft fonts."
 Else
 strTTOption = "Substitute device fonts for TrueType fonts."
 End If
 Wscript.Echo "True Type Option: " & strTTOption
 Wscript.Echo "Vertical Resolution: " & objPrinter.VerticalResolution
Next
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                      |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                                |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Impostazione CIM**](./cim-setting.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
