---
title: Compilatore di messaggi (MC.exe)
description: Usato per compilare manifesti di strumentazione e file di testo dei messaggi.
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- EventLog del compilatore di messaggi (MC.exe)
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 1ba213a1d7047b61ba7ba875adf9c281726eaae123ae018aea9920050b201644
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470941"
---
# <a name="message-compiler-mcexe"></a>Compilatore di messaggi (MC.exe)

Usato per compilare manifesti di strumentazione e file di testo dei messaggi. Il compilatore genera i file di risorse del messaggio a cui si collega l'applicazione.

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [Argomenti comuni ai file di testo dei messaggi e ai file manifesto](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [Argomenti specifici dei file manifesto](#arguments-specific-to-manifest-files)
-   [Argomenti specifici per la generazione di codice che il provider userebbe per registrare gli eventi](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [Argomenti specifici per i file di testo dei messaggi](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a>Argomenti comuni ai file di testo dei messaggi e ai file manifesto

<dl> <dt>

<span id="-_"></span>**-?**
</dt> <dd>

Visualizza le informazioni sull'utilizzo per il compilatore di messaggi.

</dd> <dt>

<span id="-c"></span><span id="-C"></span>**-c**
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore abbia impostato il bit del cliente (bit 28) in tutti gli ID messaggio. Per informazioni sul bit del cliente, vedere winerror.h.

</dd> <dt>

<span id="-cp"></span><span id="-CP"></span>**Codifica -cp** 
</dt> <dd>

Usare questo argomento per specificare la codifica dei caratteri usata per tutti i file di testo generati. I nomi validi includono "ansi" (impostazione predefinita), "utf-8" e "utf-16". Le codifiche Unicode aggiungeranno un byte order mark.

</dd> <dt>

<span id="-e_extension"></span><span id="-E_EXTENSION"></span>**Estensione -e** 
</dt> <dd>

Usare questo argomento per specificare l'estensione da utilizzare per il file di intestazione. È possibile specificare fino a un'estensione di tre caratteri, senza includere il punto. Il valore predefinito è .h.

</dd> <dt>

<span id="-h_path"></span><span id="-H_PATH"></span>**-h** *percorso*
</dt> <dd>

Usare questo argomento per specificare la cartella in cui si vuole che il compilatore inseri il file di intestazione generato. Il valore predefinito è la directory corrente.

</dd> <dt>

<span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *lunghezza*
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore generi un avviso se il messaggio supera *i caratteri di* lunghezza.

</dd> <dt>

<span id="-r_path"></span><span id="-R_PATH"></span>**-r** *path*
</dt> <dd>

Usare questo argomento per specificare la cartella in cui si vuole che il compilatore inseri lo script del compilatore di risorse generato (file RC) e i file bin generati (risorse binarie) inclusi nello script del compilatore di risorse. Il valore predefinito è la directory corrente.

</dd> <dt>

<span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *nome*
</dt> <dd>

Usare questo argomento per eseguire l'override del nome di base predefinito utilizzato dal compilatore per i file generati. Per impostazione predefinita, viene utilizzato il nome di base del file di input *del* nome file.

</dd> <dt>

<span id="filename"></span><span id="FILENAME"></span>*Filename*
</dt> <dd>

File manifesto di strumentazione o file di testo del messaggio. Il file deve esistere nella directory corrente. È possibile specificare un file manifesto, un file di testo del messaggio o entrambi. Il nome file deve includere l'estensione . La convenzione è l'uso di un'estensione man per i file manifesto e di un'estensione mc per i file di testo dei messaggi.

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a>Argomenti specifici dei file manifesto

<dl> <dt>

<span id="-s_path"></span><span id="-S_PATH"></span>**-s** *percorso*
</dt> <dd>

Usare questo argomento per creare una baseline della strumentazione. Specificare il percorso della cartella che contiene i file manifesto della baseline. Per le versioni successive, usare quindi l'argomento **-t** per verificare la presenza di problemi di compatibilità nel nuovo manifesto rispetto alla baseline.

**Prima di MC versione 1.12.7051:** Non disponibile

</dd> <dt>

<span id="-t_path"></span><span id="-T_PATH"></span>**-t** *percorso*
</dt> <dd>

Usare questo argomento quando si crea una nuova versione del manifesto e si vuole verificarne la compatibilità dell'applicazione rispetto alla baseline creata usando **l'argomento -s.** Il percorso deve puntare alla cartella che contiene . File BIN creati dall'operazione di base (vedere **l'opzione -s).**

**Prima di MC versione 1.12.7051:** Non disponibile

</dd> <dt>

<span id="-w_path"></span><span id="-W_PATH"></span>**-w** *percorso*
</dt> <dd>

Il compilatore ignora questo argomento e convalida automaticamente il manifesto.

**Prima di MC versione 1.12.7051:** Usare questo argomento per specificare la cartella che contiene il file di schema Eventman.xsd, che il compilatore usa per convalidare il manifesto. L Windows SDK include il file di schema Eventman.xsd nella \\ cartella Include. Se non si specifica questo argomento, il compilatore non convalida il manifesto.

</dd> <dt>

<span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**Percorso -W** 
</dt> <dd>

Questo argomento viene ignorato dal compilatore.

**Prima di MC versione 1.12.7051:** Usare questo argomento per specificare la cartella che contiene il Winmeta.xml file. Il Winmeta.xml file contiene i tipi di input e output riconosciuti, nonché i canali, i livelli e i codici opcode predefiniti. L Windows SDK include il file Winmeta.xml nella \\ cartella Include.

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a>Argomenti specifici per la generazione di codice che il provider userebbe per registrare gli eventi

È possibile usare gli argomenti del compilatore seguenti per generare codice in modalità kernel o in modalità utente che è possibile usare per registrare gli eventi. È anche possibile richiedere che il compilatore generi codice per supportare la scrittura di eventi nei computer prima Windows Vista. Se l'applicazione è scritta in C#, il compilatore può generare una classe C# che è possibile usare per registrare gli eventi. Questi argomenti sono disponibili a partire da MC versione 1.12.7051 fornita con la versione Windows 7 di Window SDK.

<dl> <dt>

<span id="-co"></span><span id="-CO"></span>**-co**
</dt> <dd>

Usare questo argomento per fare in modo che il servizio di registrazione chiami la funzione definita dall'utente per ogni evento registrato (la funzione viene chiamata dopo la registrazione dell'evento). La funzione definita dall'utente deve avere la firma seguente.


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



È anche necessario includere la direttiva seguente nel codice.

`#define MCGEN_CALLOUT pFnUserFunction`

È consigliabile mantenere il più breve possibile l'implementazione per evitare problemi di registrazione. il servizio non logerà più gli eventi finché la funzione non viene restituita.

È possibile usare questo argomento con **l'argomento -km** o **-um.**

</dd> <dt>

<span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**Spazio dei nomi -cs** 
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore generi una classe C# basata sulla classe [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) di .NET 3.5.

</dd> <dt>

<span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**Spazio dei nomi -css** 
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore generi una classe C# statica basata sulla classe [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) di .NET 3.5.

</dd> <dt>

<span id="-km"></span><span id="-KM"></span>**-km**
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore generi il codice in modalità kernel che verrà utilizzato per registrare gli eventi definiti nel manifesto.

</dd> <dt>

<span id="-mof"></span><span id="-MOF"></span>**-mof**
</dt> <dd>

Deprecato. Usare questo argomento per fare in modo che il compilatore generi codice che è possibile usare per registrare gli eventi nei computer prima di Windows Vista. Questa opzione crea anche un file MOF che contiene le classi MOF per ogni evento definito nel manifesto. Per registrare le classi nel file MOF in modo che i consumer possano decodificare gli eventi, usare il compilatore MOF (Mofcomp.exe). Per informazioni dettagliate sull'uso del compilatore MOF, [vedere Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).

Per usare questa opzione, è necessario rispettare le restrizioni seguenti:

-   Ogni definizione di evento deve includere gli attributi task e opcode
-   Ogni attività deve includere l'attributo eventGuid
-   I dati del modello a cui fa riferimento l'evento non possono contenere:
    -   Elementi di dati che specificano i tipi di input win:Binary o win:SYSTEMTIME
    -   Strutture
    -   Matrici con dimensioni variabili; È tuttavia possibile specificare matrici a lunghezza fissa
    -   I tipi di dati string non possono specificare l'attributo length

È necessario usare questo argomento con **l'argomento -um**, **-cs**, **-css** o **-km**

</dd> <dt>

<span id="-p_prefix"></span><span id="-P_PREFIX"></span>**Prefisso -p** 
</dt> <dd>

Usare questo argomento per eseguire l'override del prefisso predefinito utilizzato dal compilatore per i nomi delle macro e dei metodi di registrazione. Il prefisso predefinito è "EventWrite". Per la stringa viene fatta distinzione tra maiuscole e minuscole.

È possibile usare questo argomento con **l'argomento -um**, **-cs**, **-css** o **-km.**

</dd> <dt>

<span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**Prefisso -P** 
</dt> <dd>

Usare questo argomento per rimuovere i caratteri dall'inizio del nome simbolico specificato per l'evento. Il confronto viene eseguito senza distinzione tra maiuscole e minuscole. Il compilatore usa il nome simbolico per formare i nomi delle macro di registrazione e i nomi dei metodi.

Il nome predefinito per una macro di registrazione è EventWrite *SymbolName*, dove *SymbolName* è il nome simbolico specificato per l'evento. Ad esempio, se si imposta l'attributo symbol dell'evento su PrinterConnection, il nome della macro sarà EventWritePrinterConnection. Per rimuovere Printer dal nome, usare **-P** **Printer**, che determina EventWriteConnection.

È possibile usare questo argomento con **l'argomento -um**, **-cs**, **-css** o **-km.**

</dd> <dt>

<span id="-um"></span><span id="-UM"></span>**-um**
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore generi il codice in modalità utente da usare per registrare gli eventi definiti nel manifesto.

</dd> </dl>

Per fare in modo che il compilatore generi il codice di registrazione, è necessario specificare l'argomento **-um**, **-cs**, **-css** o **-km.** Questi argomenti si escludono a vicenda.

Per specificare dove inserire i file con estensione h, cs e mof generati dal compilatore, usare **l'argomento -h.** Se non si specifica **l'argomento -h,** i file vengono inseriti nella cartella corrente.

Per specificare dove inserire il file RC e i file binari (che contengono le risorse di metadati) generati dal compilatore, usare **l'argomento -r.** Se non si specifica **l'argomento -r,** i file vengono inseriti nella cartella corrente.

Il compilatore usa il nome di base del file di input come nome di base dei file generati. Per specificare un nome di base, usare **l'argomento -z.**

### <a name="arguments-specific-to-message-text-files"></a>Argomenti specifici dei file di testo dei messaggi

<dl> <dt>

<span id="-a"></span><span id="-A"></span>**-a**
</dt> <dd>

Usare questo argomento per specificare che il file di *input* del nome file contiene contenuto nella tabella codici ANSI Windows predefinita del sistema (CP_ACP). Questo è il valore predefinito. Usare **-u** per Unicode. Se il file di input contiene un BOM, questo argomento verrà ignorato.

</dd> <dt>

<span id="-A"></span><span id="-a"></span>**-A**
</dt> <dd>

Deprecato. Usare questo argomento per specificare che i messaggi nel file bin di output devono essere ANSI.

</dd> <dt>

<span id="-b"></span><span id="-B"></span>**-b**
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore usi il nome di base *del* file di input del nome del file con estensione bin. L'impostazione predefinita è l'uso di "MSG".

</dd> <dt>

<span id="-d"></span><span id="-D"></span>**-d**
</dt> <dd>

Usare questo argomento per usare valori decimali per le costanti Severity e Facility nel file di intestazione anziché valori esadecimali.

</dd> <dt>

<span id="-n"></span><span id="-N"></span>**-n**
</dt> <dd>

Utilizzare questo argomento per specificare che i messaggi terminano immediatamente dopo il corpo del messaggio. L'impostazione predefinita è terminare il corpo del messaggio con un CR/LF.

</dd> <dt>

<span id="-o"></span><span id="-O"></span>**-o**
</dt> <dd>

Usare questo argomento per fare in modo che il compilatore generi un file di intestazione OLE2 **usando definizioni HRESULT** anziché codici di stato. L'uso dei codici di stato è l'impostazione predefinita.

</dd> <dt>

<span id="-u"></span><span id="-U"></span>**-u**
</dt> <dd>

Usare questo argomento per specificare che il file di input *del* nome file contiene contenuto UTF-16LE. Il valore predefinito è contenuto ANSI. Se il file di input contiene un BOM, questo argomento verrà ignorato.

</dd> <dt>

<span id="-U"></span><span id="-u"></span>**-U**
</dt> <dd>

Usare questo argomento per specificare che i messaggi nel file bin di output devono essere Unicode. Questo è il valore predefinito.

</dd> <dt>

<span id="-v"></span><span id="-V"></span>**-v**
</dt> <dd>

Usare questo argomento per generare output dettagliato.

</dd> <dt>

<span id="-x_path"></span><span id="-X_PATH"></span>**-x** *path*
</dt> <dd>

Usare questo argomento per specificare la cartella in cui il compilatore deve inserire il file di inclusione C con estensione dbg. Il file con estensione dbg esegue il mapping degli ID messaggio ai relativi nomi simbolici.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli **argomenti -A** **e -mof** sono deprecati e verranno rimossi in futuro.

Il compilatore accetta come input un file manifesto (con estensione man) o un file di testo del messaggio (con estensione mc) e genera i file seguenti:

-   *filename*.h

    File di intestazione C/C++ che contiene i descrittori di evento, il GUID del provider e i nomi dei simboli a cui si fa riferimento nell'applicazione.

-   *nome file* TEMP.bin

    File di risorse binario che contiene i metadati del provider e dell'evento. Si tratta della risorsa modello, che è identificato dal suffisso TEMP del nome di base del file.

-   Msg00001.bin

    Un file di risorse binario per ogni lingua specificata (ad esempio, se il manifesto contiene stringhe di messaggio in en-US e fr-FR, il compilatore genererà Msg00001.bin e Msg00002.bin).

-   *filename*.rc

    Script del compilatore di risorse che contiene le istruzioni per includere ogni file con estensione bin come risorsa.

Per gli argomenti che accettano un percorso, il percorso può essere assoluto, relativo o UNC e può contenere variabili di ambiente.

**Prima di MC versione 1.12.7051:** Il compilatore non consente percorsi relativi o variabili di ambiente.

L Windows SDK include il compilatore (mc.exe) nella \\ cartella Bin.

## <a name="examples"></a>Esempio

L'esempio seguente compila un manifesto usando le impostazioni predefinite del compilatore.

``` syntax
mc spooler.man
```

L'esempio seguente compila il manifesto e inserisce l'intestazione e i file di risorse nelle cartelle specificate.

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a>Requisiti

| Requisito | Valore |
|--------------------------|-------------------------------------------------|
| Client minimo supportato | Windows 2000 Professional \[solo app desktop\] |
| Server minimo supportato | Windows 2000 Server \[solo app desktop\]       |
