---
title: Compilatore di messaggi (MC.exe)
description: Utilizzato per compilare manifesti di strumentazione e file di testo del messaggio.
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- Log eventi del compilatore di messaggi (MC.exe)
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 5eb852dcbb13800705db0a0f19d912de899f9b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524241"
---
# <a name="message-compiler-mcexe"></a>Compilatore di messaggi (MC.exe)

Utilizzato per compilare manifesti di strumentazione e file di testo del messaggio. Il compilatore genera i file di risorse dei messaggi a cui è collegata l'applicazione.

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [Argomenti comuni a entrambi i file di testo dei messaggi e i file manifesto](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [Argomenti specifici dei file manifesto](#arguments-specific-to-manifest-files)
-   [Argomenti specifici della generazione di codice che il provider utilizzerebbe per registrare gli eventi](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [Argomenti specifici dei file di testo del messaggio](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a>Argomenti comuni a entrambi i file di testo dei messaggi e i file manifesto

<dl> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Visualizza le informazioni sull'utilizzo del compilatore di messaggi.

</dd> <dt>

<span id="-c"></span><span id="-C"></span>**-c**
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore imposti il bit Customer (bit 28) in tutti gli ID messaggio. Per informazioni sul bit del cliente, vedere Winerror. h.

</dd> <dt>

<span id="-cp"></span><span id="-CP"></span>**-** *codifica* CP
</dt> <dd>

Utilizzare questo argomento per specificare la codifica dei caratteri utilizzata per tutti i file di testo generati. I nomi validi includono "ANSI" (impostazione predefinita), "UTF-8" e "UTF-16". Con le codifiche Unicode viene aggiunto un byte order mark.

</dd> <dt>

<span id="-e_extension"></span><span id="-E_EXTENSION"></span>*estensione* **-e**
</dt> <dd>

Utilizzare questo argomento per specificare l'estensione da utilizzare per il file di intestazione. È possibile specificare fino a un'estensione di tre caratteri, escluso il punto. Il valore predefinito è. h.

</dd> <dt>

<span id="-h_path"></span><span id="-H_PATH"></span>**-h** *percorso*
</dt> <dd>

Utilizzare questo argomento per specificare la cartella in cui si desidera che il compilatore inserisca il file di intestazione generato. Il valore predefinito è la directory corrente.

</dd> <dt>

<span id="-m_length"></span><span id="-M_LENGTH"></span>*lunghezza* **-m**
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore generi un avviso se il messaggio supera i caratteri di *lunghezza* .

</dd> <dt>

<span id="-r_path"></span><span id="-R_PATH"></span>**-r** *percorso*
</dt> <dd>

Usare questo argomento per specificare la cartella in cui si vuole che il compilatore inserisca lo script del compilatore di risorse generato (file RC) e i file. bin generati (risorse binarie) inclusi nello script del compilatore di risorse. Il valore predefinito è la directory corrente.

</dd> <dt>

<span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *nome*
</dt> <dd>

Utilizzare questo argomento per eseguire l'override del nome di base predefinito utilizzato dal compilatore per i file generati. Per impostazione predefinita, viene utilizzato il nome di base del file di input del *nome* file.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*filename*
</dt> <dd>

Il file manifesto di strumentazione o il file di testo del messaggio. Il file deve essere presente nella directory corrente. È possibile specificare un file manifesto, un file di testo del messaggio o entrambi. Il nome del file deve includere l'estensione. La convenzione prevede l'uso di un'estensione. Man per i file manifesto e di un'estensione MC per i file di testo del messaggio.

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a>Argomenti specifici dei file manifesto

<dl> <dt>

<span id="-s_path"></span><span id="-S_PATH"></span>**-s** *percorso*
</dt> <dd>

Usare questo argomento per creare una linea di base della strumentazione. Specificare il percorso della cartella che contiene i file manifesto di base. Per le versioni successive, si userà quindi l'argomento **-t** per verificare il nuovo manifesto rispetto alla linea di base per i problemi di compatibilità.

**Prima della versione MC 1.12.7051:** Non disponibile

</dd> <dt>

<span id="-t_path"></span><span id="-T_PATH"></span>**-t** *percorso*
</dt> <dd>

Usare questo argomento quando si crea una nuova versione del manifesto e si vuole controllare la compatibilità delle applicazioni con la linea di base creata con l'argomento **-s** . Il percorso deve puntare alla cartella che contiene. File BIN creati dall'operazione di base (vedere l'opzione **-s** ).

**Prima della versione MC 1.12.7051:** Non disponibile

</dd> <dt>

<span id="-w_path"></span><span id="-W_PATH"></span>**-w** *percorso*
</dt> <dd>

Il compilatore ignora questo argomento e convalida automaticamente il manifesto.

**Prima della versione MC 1.12.7051:** Utilizzare questo argomento per specificare la cartella che contiene il file di schema EventName. xsd, utilizzato dal compilatore per convalidare il manifesto. Il Windows SDK include il file di schema EventName. xsd nella \\ cartella di inclusione. Se non si specifica questo argomento, il compilatore non convalida il manifesto.

</dd> <dt>

<span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *percorso*
</dt> <dd>

Il compilatore ignora questo argomento.

**Prima della versione MC 1.12.7051:** Utilizzare questo argomento per specificare la cartella che contiene il file di Winmeta.xml. Il file di Winmeta.xml contiene i tipi di input e output riconosciuti, nonché i canali, i livelli e i codici operativi predefiniti. Il Windows SDK include il file di Winmeta.xml nella \\ cartella di inclusione.

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a>Argomenti specifici della generazione di codice che il provider utilizzerebbe per registrare gli eventi

È possibile utilizzare gli argomenti del compilatore seguenti per generare codice in modalità kernel o utente che è possibile utilizzare per registrare gli eventi. È inoltre possibile richiedere al compilatore di generare codice per supportare la scrittura di eventi nei computer precedenti a Windows Vista. Se l'applicazione è scritta in C#, il compilatore può generare una classe C# che può essere usata per registrare gli eventi. Questi argomenti sono disponibili a partire dalla versione MC 1.12.7051 fornita con la versione Windows 7 di Window SDK.

<dl> <dt>

<span id="-co"></span><span id="-CO"></span>**-Co**
</dt> <dd>

Usare questo argomento per fare in modo che il servizio di registrazione chiami la funzione definita dall'utente per ogni evento registrato (la funzione viene chiamata dopo che l'evento è stato registrato). La funzione definita dall'utente deve avere la firma seguente.


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



È inoltre necessario includere la direttiva seguente nel codice.

`#define MCGEN_CALLOUT pFnUserFunction`

Per evitare problemi di registrazione, è consigliabile tenere l'implementazione più breve possibile. il servizio non registrerà più gli eventi fino a quando la funzione non restituisce.

È possibile usare questo argomento con l'argomento **-km** o **-um** .

</dd> <dt>

<span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs (** *spazio dei nomi* )
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore generi una classe C# basata sulla classe [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) di .NET 3,5.

</dd> <dt>

<span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-** *spazio dei nomi* CSS
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore generi una classe C# statica basata sulla classe [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) di .NET 3,5.

</dd> <dt>

<span id="-km"></span><span id="-KM"></span>**-km**
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore generi il codice in modalità kernel da usare per registrare gli eventi definiti nel manifesto.

</dd> <dt>

<span id="-mof"></span><span id="-MOF"></span>**-MOF**
</dt> <dd>

Deprecato. Utilizzare questo argomento per fare in modo che il compilatore generi codice che è possibile utilizzare per registrare gli eventi nei computer precedenti a Windows Vista. Questa opzione crea anche un file MOF che contiene le classi MOF per ogni evento definito nel manifesto. Per registrare le classi nel file MOF in modo che i consumer possano decodificare gli eventi, usare il compilatore MOF (Mofcomp.exe). Per informazioni dettagliate sull'uso del compilatore MOF, vedere [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).

Per usare questa opzione, è necessario rispettare le restrizioni seguenti:

-   Ogni definizione di evento deve includere gli attributi Task e OpCode
-   Ogni attività deve includere l'attributo eventGuid
-   I dati del modello a cui fa riferimento l'evento non possono contenere:
    -   Elementi di dati che specificano i tipi di input Win: Binary o Win: SYSTEMTIME
    -   Strutture
    -   Matrici di dimensioni variabili; è tuttavia possibile specificare matrici a lunghezza fissa
    -   I tipi di dati stringa non possono specificare l'attributo length

È necessario utilizzare questo argomento con l'argomento **-um**, **-CS**, **-CSS** o **-km**

</dd> <dt>

<span id="-p_prefix"></span><span id="-P_PREFIX"></span>*prefisso* **-p**
</dt> <dd>

Utilizzare questo argomento per sostituire il prefisso predefinito utilizzato dal compilatore per i nomi delle macro di registrazione e i nomi dei metodi. Il prefisso predefinito è "EventWrite". Per la stringa viene fatta distinzione tra maiuscole e minuscole.

È possibile utilizzare questo argomento con l'argomento **-um**, **-CS**, **-CSS** o **-km** .

</dd> <dt>

<span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>*Prefisso* **-P**
</dt> <dd>

Usare questo argomento per rimuovere i caratteri dall'inizio del nome simbolico specificato per l'evento. Il confronto viene eseguito senza distinzione tra maiuscole e minuscole. Il compilatore usa il nome simbolico per formare i nomi delle macro di registrazione e i nomi dei metodi.

Il nome predefinito di una macro di registrazione è EventWrite *symbolName*, dove *symbolName* è il nome simbolico specificato per l'evento. Se, ad esempio, si imposta l'attributo symbol dell'evento su PrinterConnection, il nome della macro sarà EventWritePrinterConnection. Per rimuovere la stampante dal nome, usare **-P** **Printer**, che restituisce EventWriteConnection.

È possibile utilizzare questo argomento con l'argomento **-um**, **-CS**, **-CSS** o **-km** .

</dd> <dt>

<span id="-um"></span><span id="-UM"></span>**-um**
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore generi il codice in modalità utente da usare per registrare gli eventi definiti nel manifesto.

</dd> </dl>

Per fare in modo che il compilatore generi il codice di registrazione, è necessario specificare l'argomento **-um**, **-CS**, **-CSS** o **-km** ; questi argomenti si escludono a vicenda.

Per specificare dove inserire i file con estensione h, CS e MOF generati dal compilatore, usare l'argomento **-h** . Se non si specifica l'argomento **-h** , i file vengono inseriti nella cartella corrente.

Per specificare dove inserire il file RC e i file binari (contenenti le risorse di metadati) generati dal compilatore, usare l'argomento **-r** . Se non si specifica l'argomento **-r** , i file vengono inseriti nella cartella corrente.

Il compilatore usa il nome di base del file di input come nome di base dei file generati. Per specificare un nome di base, usare l'argomento **-z** .

### <a name="arguments-specific-to-message-text-files"></a>Argomenti specifici dei file di testo del messaggio

<dl> <dt>

<span id="-a"></span><span id="-A"></span>**-a**
</dt> <dd>

Usare questo argomento per specificare che il file di input del *nome* file contiene contenuto nella tabella codici ANSI predefinita di sistema (CP_ACP). Questo è il valore predefinito. Usare **-u** per Unicode. Se il file di input contiene un BOM, questo argomento verrà ignorato.

</dd> <dt>

<span id="-A"></span><span id="-a"></span>**-A**
</dt> <dd>

Deprecato. Utilizzare questo argomento per specificare che i messaggi nel file. bin di output devono essere ANSI.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>**-b**
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore usi il nome di base del file di input del *nome* file per i nomi di file con estensione bin. Per impostazione predefinita, viene usato "MSG".

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Utilizzare questo argomento per utilizzare valori decimali per le costanti di gravità e di funzione nel file di intestazione anziché valori esadecimali.

</dd> <dt>

<span id="-n"></span><span id="-N"></span>**-n**
</dt> <dd>

Utilizzare questo argomento per specificare che i messaggi terminano immediatamente dopo il corpo del messaggio. Per impostazione predefinita, il corpo del messaggio viene terminato con CR/LF.

</dd> <dt>

<span id="-o"></span><span id="-O"></span>**-o**
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore generi un file di intestazione OLE2 usando le definizioni **HRESULT** anziché i codici di stato. L'utilizzo dei codici di stato è il valore predefinito.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>**-u**
</dt> <dd>

Usare questo argomento per specificare che il file di input del *nome* file contiene contenuto UTF-16LE. Il valore predefinito è contenuto ANSI. Se il file di input contiene un BOM, questo argomento verrà ignorato.

</dd> <dt>

<span id="-U"></span><span id="-u"></span>**-U**
</dt> <dd>

Utilizzare questo argomento per specificare che i messaggi nel file. bin di output devono essere Unicode. Questo è il valore predefinito.

</dd> <dt>

<span id="-v"></span><span id="-V"></span>**-v**
</dt> <dd>

Usare questo argomento per generare l'output dettagliato.

</dd> <dt>

<span id="-x_path"></span><span id="-X_PATH"></span>**-x** *percorso*
</dt> <dd>

Utilizzare questo argomento per specificare la cartella in cui si desidera che il compilatore inserisca il file di inclusione. dbg C. Il file con estensione DBG esegue il mapping degli ID messaggio ai nomi simbolici.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli argomenti **-A** e **-MOF** sono deprecati e verranno rimossi in futuro.

Il compilatore accetta come input un file manifesto (. Man) o un file di testo del messaggio (. MC) e genera i file seguenti:

-   *nomefile*. h

    Un file di intestazione C/C++ che contiene i descrittori di evento, il GUID del provider e i nomi dei simboli a cui si fa riferimento nell'applicazione.

-   *nome file* TEMP. bin

    Un file di risorse binario che contiene i metadati dell'evento e del provider. Si tratta della risorsa modello, che è contraddistinta dal suffisso temporaneo del nome di base del file.

-   Msg00001. bin

    Un file di risorse binario per ogni lingua specificata (ad esempio, se il manifesto contiene stringhe di messaggio in en-US e fr-FR, il compilatore genererà Msg00001. bin e Msg00002. bin).

-   *nomefile*. RC

    Uno script del compilatore di risorse che contiene le istruzioni per includere ogni file con estensione bin come risorsa.

Per gli argomenti che accettano un percorso, il percorso può essere un percorso assoluto, relativo o UNC e può contenere variabili di ambiente.

**Prima della versione MC 1.12.7051:** Il compilatore non consente percorsi relativi o variabili di ambiente.

Il Windows SDK include il compilatore (mc.exe) nella \\ cartella bin.

## <a name="examples"></a>Esempio

Nell'esempio seguente viene compilato un manifesto usando le impostazioni predefinite del compilatore.

``` syntax
mc spooler.man
```

Nell'esempio seguente viene compilato il manifesto e vengono posizionati i file di intestazione e di risorse nelle cartelle specificate.

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------------|
| Client minimo supportato | Windows 2000 Professional \[solo app desktop\] |
| Server minimo supportato | Windows 2000 Server \[solo app desktop\]       |
