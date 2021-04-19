---
description: Rappresenta un processo di stampa generato da un'applicazione Windows. Qualsiasi unità di lavoro generata dal comando stampa di un'applicazione in esecuzione in un computer in cui è in esecuzione un sistema operativo Windows è un discendente o un membro di questa classe.
ms.assetid: d884acba-e1b2-4d24-9b55-15d175a163d9
ms.tgt_platform: multiple
title: Classe Win32_PrintJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrintJob
- Win32_PrintJob.Caption
- Win32_PrintJob.Description
- Win32_PrintJob.InstallDate
- Win32_PrintJob.Name
- Win32_PrintJob.Status
- Win32_PrintJob.ElapsedTime
- Win32_PrintJob.JobStatus
- Win32_PrintJob.Notify
- Win32_PrintJob.Owner
- Win32_PrintJob.Priority
- Win32_PrintJob.StartTime
- Win32_PrintJob.TimeSubmitted
- Win32_PrintJob.UntilTime
- Win32_PrintJob.Color
- Win32_PrintJob.DataType
- Win32_PrintJob.Document
- Win32_PrintJob.DriverName
- Win32_PrintJob.HostPrintQueue
- Win32_PrintJob.JobId
- Win32_PrintJob.PagesPrinted
- Win32_PrintJob.PaperLength
- Win32_PrintJob.PaperSize
- Win32_PrintJob.PaperWidth
- Win32_PrintJob.Parameters
- Win32_PrintJob.PrintProcessor
- Win32_PrintJob.Size
- Win32_PrintJob.StatusMask
- Win32_PrintJob.TotalPages
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10f56034161a9313eed1b7d302ab790d153c0ee6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305090"
---
# <a name="win32_printjob-class"></a>Win32 \_ PrintJob (classe)

La [classe WMI](../wmisdk/retrieving-a-class.md) **\_ PrintJob Win32** rappresenta un processo di stampa generato da un'applicazione Windows. Qualsiasi unità di lavoro generata dal comando stampa di un'applicazione in esecuzione in un computer in cui è in esecuzione un sistema operativo Windows è un discendente o un membro di questa classe.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate. Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.

## <a name="syntax"></a>Sintassi

``` syntax
class Win32_PrintJob : CIM_Job
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  datetime ElapsedTime;
  string   JobStatus;
  string   Notify;
  string   Owner;
  uint32   Priority;
  datetime StartTime;
  datetime TimeSubmitted;
  datetime UntilTime;
  string   Color;
  string   DataType;
  string   Document;
  string   DriverName;
  string   HostPrintQueue;
  uint32   JobId;
  uint32   PagesPrinted;
  uint32   PaperLength;
  string   PaperSize;
  uint32   PaperWidth;
  string   Parameters;
  string   PrintProcessor;
  uint32   Size;
  uint32   StatusMask;
  uint32   TotalPages;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ PrintJob** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ PrintJob** presenta questi metodi.



| Metodo                                                  | Descrizione                       |
|:--------------------------------------------------------|:----------------------------------|
| [**Sospendere**](pause-method-in-class-win32-printjob.md)   | Sospende un processo di stampa.<br/>    |
| [**Riprendi**](resume-method-in-class-win32-printjob.md) | Continua un processo di stampa.<br/> |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ PrintJob** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Colore**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa che indica se il documento è stampato in colore o monocromatico. Alcune stampanti a colori sono in grado di stampare utilizzando il vero nero anziché una combinazione di giallo, ciano e magenta. Il vero nero crea in genere testo più scuro e più nitido per i documenti. Questa opzione è utile solo per le stampanti a colori che supportano la stampa true nero.

I valori possibili sono:

<dl><span id="_Color_"></span><span id="_color_"></span><span id="_COLOR_"></span><dt>

**Colore**
</dt><span id="_Monochrome_"></span><span id="_monochrome_"></span><span id="_MONOCHROME_"></span><dt>

**Monocromatico**
</dt> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Formato dei dati per il processo di stampa. In questo modo viene indicato al driver della stampante di tradurre i dati (testo generico, PostScript o PCL) prima della stampa o di stampare in un formato non elaborato (per grafica e immagini).

Esempio: "testo"

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")
</dt> </dl>

Descrizione testuale dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Documento**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del processo di stampa. L'utente Visualizza questo nome quando Visualizza i documenti in attesa di essere stampati.

Esempio: "Microsoft Word-Review.doc"

</dd> <dt>

**DriverName**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del driver della stampante utilizzato per il processo di stampa.

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Periodo di tempo durante il quale il processo è stato eseguito.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> <dt>

**HostPrintQueue**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del computer in cui viene creato il processo di stampa.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. DMTF \| ComponentID \| 001,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data di installazione ")
</dt> </dl>

Indica quando l'oggetto è stato installato. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**JobId**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero dell'identificatore del processo. Viene usato da altri metodi come handle per un processo di spooling alla stampante.

</dd> <dt>

**Stato processo**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Stringa in formato libero che rappresenta lo stato del processo.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Etichetta con cui l'oggetto è noto. Quando è sottoclassata, è possibile eseguire l'override di questa proprietà in modo che sia una proprietà chiave.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Notificare**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

L'utente riceve una notifica al completamento o all'esito negativo del processo.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> <dt>

**Proprietario**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Utente che ha inviato il processo.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> <dt>

**PagesPrinted**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di pagine stampate. Questo valore può essere 0 (zero) se il processo di stampa non contiene informazioni di delimitazione della pagina.

</dd> <dt>

**PaperLength**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) (decimi di millimetro)
</dt> </dl>

Lunghezza del documento.

Esempio: 2794

</dd> <dt>

**PaperSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dimensioni del foglio utilizzato per stampare il processo. Il valore è uno dei formati di carta possibili per la stampante specificata nella proprietà **PaperSizesSupported** della classe [**\_ Printer Win32**](win32-printer.md) .

</dd> <dt>

**PaperWidth**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) (decimi di millimetro)
</dt> </dl>

Larghezza del foglio.

Esempio: 2159

</dd> <dt>

**Parametri**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Parametri facoltativi da inviare al processore di stampa. Per ulteriori informazioni, vedere la proprietà **PrintProcessor** .

</dd> <dt>

**PrintProcessor**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Servizio processore di stampa utilizzato per elaborare il processo di stampa. Un processore di stampanti funziona insieme al driver della stampante per fornire una conversione aggiuntiva dei dati della stampante per la stampante e può essere usato anche per fornire opzioni speciali, ad esempio una pagina del titolo per il processo.

</dd> <dt>

**Priorità**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Importanza dell'esecuzione di un processo.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> <dt>

**Dimensioni**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**unità**](../wmisdk/standard-qualifiers.md) (byte)
</dt> </dl>

Dimensioni del processo di stampa.

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di inizio del processo.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Stringa che indica lo stato corrente dell'oggetto. È possibile definire lo stato operativo e non operativo. Lo stato operativo può includere "OK", "danneggiato" e "errore predazione". "Predator fail" indica che un elemento funziona correttamente, ma sta stimando un errore, ad esempio un'unità disco rigido abilitata per SMART.

Lo stato non operativo può includere "Error", "starting", "stoping" e "Service". Il "servizio" può essere applicato durante il mirroring del disco, ovvero la riattivazione, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Sono inclusi i valori seguenti:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Errore** ("errore")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

Ridotto **("danneggiato"** )


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** ("sconosciuto")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Errore di predazione** ("Predator fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Avvio** di ("avvio")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Arresto** in corso ("arresto")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Servizio** ("servizio")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sottolineato** (sottolineato)


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**Noncover** ("noncover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Nessun contatto** ("nessun contatto")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Comunicazione persa** ("comunicazione persa")


</dt> <dd></dd> </dl>

</dd> <dt>

**StatusMask**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Bitmap dei possibili stati correlati a questo processo di stampa.

<dt>

1 (0x1)
</dt> <dd>

Paused

</dd> <dt>

2 (0x2)
</dt> <dd>

Errore

</dd> <dt>

4 (0x4)
</dt> <dd>

Deleting

</dd> <dt>

8 (0x8)
</dt> <dd>

Spooling

</dd> <dt>

16 (0x10)
</dt> <dd>

Stampa

</dd> <dt>

32 (0x20)
</dt> <dd>

Offline

</dd> <dt>

64 (0x40)
</dt> <dd>

Carta

</dd> <dt>

128 (0x80)
</dt> <dd>

Stampato

</dd> <dt>

256 (0x100)
</dt> <dd>

Eliminata

</dd> <dt>

512 (0x200)
</dt> <dd>

\_DevQ bloccati

</dd> <dt>

1024 (0x400)
</dt> <dd>

\_Req intervento dell'utente \_

</dd> <dt>

2048 (0x800)
</dt> <dd>

Riavvio

</dd> </dl>

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora di invio del processo.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> <dt>

**TotalPages**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero di pagine necessarie per completare il processo. Questo valore può essere 0 (zero) se il processo di stampa non contiene informazioni di delimitazione della pagina.

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Ora in cui il processo non è valido o deve essere arrestato.

Questa proprietà viene ereditata [**dal \_ processo CIM**](cim-job.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

La classe **Win32 \_ PrintJob** è derivata dal [**\_ processo CIM**](cim-job.md).

## <a name="examples"></a>Esempio

Nell'esempio di codice VBScript seguente viene descritto come recuperare le statistiche dei processi di stampa dalle istanze di **Win32 \_ PrintJob**.


```VB
Set PrintJobSet = GetObject("winmgmts:").InstancesOf ("Win32_PrintJob")

If (PrintJobSet.Count = 0) Then WScript.Echo "No print jobs!"
for each PrintJob in PrintJobSet
 WScript.Echo PrintJob.Name
 WScript.Echo PrintJob.JobId
 WScript.Echo PrintJob.Status
 WScript.Echo PrintJob.TotalPages
 Wscript.Echo ""
next
```



Nell'esempio di codice Perl seguente viene descritto come recuperare le statistiche dei processi di stampa dalle istanze di **Win32 \_ PrintJob**.


```
use strict;
use Win32::OLE;

close (STDERR);

my ($PrintJobset, $PrintJob);
eval {$PrintJobset = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}")->
 InstancesOf ("Win32_PrintJob") };
if (!$@ && defined $PrintJobset)
{
 if ($PrintJobset->{Count} == 0 ) 
 {
  print "\nNo print jobs!\n";
 }

 foreach $PrintJob (in $PrintJobset)
 {
  print $PrintJob->{Name} , "\n";
  print $PrintJob->{JobId} , "\n";
  print $PrintJob->{Status} , "\n";
  print $PrintJob->{TotalPages} , "\n";
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
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

[**\_Processo CIM**](./cim-job.md)
</dt> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> </dl>

 

 
