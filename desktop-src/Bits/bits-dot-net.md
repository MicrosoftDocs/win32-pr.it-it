---
title: Uso di BITS da .NET tramite DLL di riferimento
description: Gli esempi seguenti illustrano come chiamare nell'interfaccia COM BITS da un programma .NET
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: 00f7d6287d86dd1816d7e4b0a7c6e18c9ae4916c5c85b01d0280758cf9d00b5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529151"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a>Chiamata a BITS da .NET e C# tramite DLL di riferimento

Un modo per chiamare le classi COM BITS da un programma .NET è creare un file DLL di riferimento a partire dai file [IDL](/windows/desktop/Midl/midl-start-page) BITS (Interface Definition Language) in Windows SDK, usando gli strumenti [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) e [TLBIMP.](/dotnet/framework/tools/tlbimp-exe-type-library-importer) La DLL di riferimento è un set di wrapper di classi per le classi COM BITS. È quindi possibile usare le classi wrapper direttamente da .NET.

Un'alternativa all'uso di DLL di riferimento create automaticamente consiste nell'usare un wrapper BITS .NET di terze parti da GitHub [e](https://github.com/) [NuGet](https://www.nuget.org/). Questi wrapper hanno spesso uno stile di programmazione .NET più naturale, ma potrebbero essere in ritardo rispetto alle modifiche e agli aggiornamenti nelle interfacce BITS.

## <a name="creating-the-reference-dlls"></a>Creazione delle DLL di riferimento
### <a name="bits-idl-files"></a>File IDL BITS

Si inizierà con il set di file IDL BITS. Si tratta di file che definiscono completamente l'interfaccia COM BITS. I file si trovano nella directory **Windows Kits** e sono denominati bits *version*.idl (ad esempio, bits10_2.idl) ad eccezione del file versione 1.0 che è solo Bits.idl. Quando vengono create nuove versioni di BITS, vengono creati anche nuovi file IDL BITS.

È anche possibile modificare una copia dei file IDL BITS dell'SDK per usare funzionalità BITS che non vengono convertite automaticamente in equivalenti .NET. Le possibili modifiche ai file IDL vengono illustrate più avanti.

I file IDL BITS includono diversi altri file IDL per riferimento. Nidificano anche, in modo che, se si usa una versione, includa tutte le versioni inferiori.

Per ogni versione di BITS che si vuole usare come destinazione nel programma è necessaria una DLL di riferimento per tale versione. Ad esempio, se si vuole scrivere un programma che funziona su BITS 1.5 e versione precedente, ma con funzionalità aggiuntive quando è presente BITS 10.2, è necessario convertire entrambi i file bits1_5.idl e bits10_2.idl.


### <a name="midl-and-tlbimp-utilities"></a>Utilità MIDL e TLBIMP

[L'utilità MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft Interface Definition Language) converte i file IDL che descrivono l'interfaccia COM BITS in un file TLB (libreria dei tipi). Lo strumento MIDL dipende dall'utilità CL (preprocessore C) per leggere correttamente il file di linguaggio IDL. L'utilità CL fa parte Visual Studio e viene installata quando si includono le funzionalità C/C++ nell'Visual Studio installazione.

L'utilità MIDL crea in genere un set di file C e H (codice del linguaggio C e intestazione del linguaggio C). È possibile eliminare questi file aggiuntivi inviando l'output al dispositivo NUL: . Ad esempio, l'impostazione dell'opzione /dlldata NUL: elimina la creazione di un file dlldata.c. I comandi di esempio seguenti illustrano quali opzioni devono essere impostate su NUL:.

[L'utilità TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (Type Library Importer) legge in un file TLB e crea il file DLL di riferimento corrispondente. 


### <a name="example-commands-for-midl-and-tlbimp"></a>Comandi di esempio per MIDL e TLBIMP

Questo è un esempio del set completo di comandi per generare un set di file di riferimento. Potrebbe essere necessario modificare i comandi in base all'installazione di Visual Studio e Windows SDK e in base alle funzionalità BITS e alle versioni del sistema operativo di destinazione. 

Nell'esempio viene creata una directory in cui inserire i file DLL di riferimento e viene creata una variabile di ambiente BITSTEMP che punta a tale directory. 

I comandi di esempio eseguono vsdevcmd.bat file creato dal programma di Visual Studio programma di installazione. Questo file BAT configura i percorsi e alcune variabili di ambiente in modo che i comandi MIDL e TLBIMP verranno eseguiti. Configura anche le variabili WindowsSdkDir e WindowsSDKLibVersion in modo che puntino alle directory più recenti Windows SDK.

```console
REM Create a working directory
REM You can select a different directory based on your needs.
SET BITSTEMP=C:\BITSTEMPDIR
MKDIR "%BITSTEMP%"

REM Run the VsDevCmd.bat file to locate the Windows
REM SDK directory and the tools directories
REM This will be different for different versions of
REM Visual Studio

CALL "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools\vsdevcmd.bat"

REM Run the MIDL command on the desired BITS IDL file
REM This will generate a TLB file for the TLBIMP command
REM The IDL file will be different depending on which
REM set of BITS interfaces you need to use.
REM Run the MIDL command once per reference file
REM that you will need to explicitly use.
PUSHD .
CD /D "%WindowsSdkDir%Include\%WindowsSDKLibVersion%um"

MIDL  /I ..\shared /out "%BITSTEMP%" bits1_5.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits4_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits5_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_1.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_2.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:

REM Run the TLBIMP command on the resulting TLB file(s)
REM Try to keep a parallel set of names.
TLBIMP "%BITSTEMP%"\bits1_5.tlb /out: "%BITSTEMP%"\BITSReference1_5.dll
TLBIMP "%BITSTEMP%"\bits4_0.tlb /out: "%BITSTEMP%"\BITSReference4_0.dll
TLBIMP "%BITSTEMP%"\bits5_0.tlb /out: "%BITSTEMP%"\BITSReference5_0.dll
TLBIMP "%BITSTEMP%"\bits10_1.tlb /out: "%BITSTEMP%"\BITSReference10_1.dll
TLBIMP "%BITSTEMP%"\bits10_2.tlb /out: "%BITSTEMP%"\BITSReference10_2.dll
DEL "%BITSTEMP%"\bits*.tlb
POPD

```
Una volta eseguiti questi comandi, nella directory BITSTEMP sarà presente un set di DLL di riferimento.

### <a name="adding-the-reference-dlls-to-your-project"></a>Aggiunta delle DLL di riferimento al progetto

Per usare una DLL di riferimento in un progetto C#, aprire il progetto C# in Visual Studio. Nel riquadro Esplora soluzioni fare clic con il pulsante destro del mouse su Riferimenti e scegliere Aggiungi riferimento. Fare quindi clic sul pulsante Sfoglia e quindi sul pulsante Aggiungi. Passare alla directory con le DLL di riferimento, selezionarle e fare clic su Aggiungi. Nella finestra Gestione riferimenti verranno controllate le DLL di riferimento. Fare quindi clic su OK.

Le DLL di riferimento BITS vengono ora aggiunte al progetto.

Le informazioni nei file DLL di riferimento verranno incorporate nel programma finale. Non è necessario spedire i file DLL di riferimento con il programma. è sufficiente spedire il .EXE. 

È possibile modificare se le DLL di riferimento sono incorporate nel file EXE finale. Usare la [proprietà Incorpora tipi di](/dotnet/framework/interop/how-to-add-references-to-type-libraries) interoperabilità per impostare se le DLL di riferimento verranno incorporate. Questa operazione può essere eseguita in base al riferimento. Il valore predefinito è True per incorporare le DLL.

## <a name="modifying-idl-files-for-more-complete-net-code"></a>Modifica dei file IDL per un codice .NET più completo

I file IDL BITS (Microsoft Interface Definition Language) possono essere usati senza modifiche per rendere il file DLL BackgroundCopyManager. Tuttavia, la DLL di riferimento .NET risultante manderà alcune unioni non traducibili e avrà nomi difficili da usare per alcune strutture ed enumerazioni. Questa sezione descrive alcune delle modifiche che è possibile apportare per rendere la DLL .NET più completa e più facile da usare.

### <a name="simpler-enum-names"></a>Nomi ENUM più semplici

I file IDL BITS definiscono in genere valori di enumerazione come i seguenti:
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
Il BG_AUTH_TARGET è il nome del typedef. L'enumerazione effettiva non è denominata. Questo non causa in genere problemi con il codice C, ma non si traduce bene per l'uso con un programma .NET. Verrà creato automaticamente un nuovo nome, ma potrebbe essere simile a _MIDL___MIDL_itf_bits4_0_0005_0001_0001 anziché a un valore leggibile dall'utente. È possibile risolvere questo problema aggiornando i file MIDL in modo da includere un nome di enumerazione.

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

Il nome dell'enumerazione può essere uguale al nome typedef. Alcuni programmatori hanno una convenzione di denominazione in cui vengono mantenuti diversi (ad esempio, inserendo un carattere di sottolineatura prima del nome dell'enumerazione), ma questo confonde solo le traduzioni .NET. 

### <a name="string-types-in-unions"></a>Tipi stringa nelle unioni

I file IDL BITS passano stringhe usando la convenzione LPWSTR (puntatore lungo a stringa di caratteri wide). Anche se funziona quando si passano parametri di funzione (ad esempio il metodo Job.GetDisplayName([out] LPWSTR *pVal), non funziona quando le stringhe fanno parte delle unioni. Ad esempio, il file bits5_0.idl include l'BITS_FILE_PROPERTY_VALUE union:

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

Il campo LPWSTR non verrà incluso nella versione .NET dell'unione. Per risolvere il problema, modificare LPWSTR in WCHAR*. Il campo risultante (denominato String) verrà passato come IntPtr. Convertirlo in una stringa usando System.Runtime.InteropServices.Marshal.PtrToStringAuto(value. String); Metodo.

### <a name="unions-in-structures"></a>Unioni nelle strutture

In alcuni casi le unioni incorporate nelle strutture non verranno incluse nella struttura. Ad esempio, nel file Bits1_5.idl il BG_AUTH_CREDENTIALS è definito come segue:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

La BG_AUTH_CREDENTIALS_UNION è definita come unione come segue:
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
Il campo Credentials (Credenziali) BG_AUTH_CREDENTIALS non verrà incluso nella definizione della classe .NET.

Si noti che l'unione è definita come sempre BG_BASIC_CREDENTIALS indipendentemente dal BG_AUTH_SCHEME. Poiché l'unione non viene usata come unione, è possibile passare una BG_BASIC_CREDENTIALS simile alla seguente:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a>Uso di BITS da C #

### <a name="recommended-using-statement"></a>Istruzione using consigliata

La configurazione di alcune istruzioni using in C# ridurrà il numero di caratteri da digitare per usare le diverse versioni BITS. Il nome "BITSReference" deriva dal nome della DLL di riferimento.

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a>Esempio rapido: scaricare un file

Di seguito è riportato un frammento breve ma completo di codice C# per scaricare un file da un URL. 

```csharp
    var mgr = new BITS.BackgroundCopyManager1_5();
    BITS.GUID jobGuid;
    BITS.IBackgroundCopyJob job;
    mgr.CreateJob("Quick download", BITS.BG_JOB_TYPE.BG_JOB_TYPE_DOWNLOAD, out jobGuid, out job);
    job.AddFile("https://aka.ms/WinServ16/StndPDF", @"C:\Server2016.pdf");
    job.Resume();
    bool jobIsFinal = false;
    while (!jobIsFinal)
    {
        BITS.BG_JOB_STATE state;
        job.GetState(out state);
        switch (state)
        {
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ERROR:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_TRANSFERRED:
                job.Complete();
                break;

            case BITS.BG_JOB_STATE.BG_JOB_STATE_CANCELLED:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ACKNOWLEDGED:
                jobIsFinal = true;
                break;
            default:
                Task.Delay(500); // delay a little bit
                break;
        }
    }
    // Job is complete
```

In questo codice di esempio viene creato un gestore BITS denominato mgr. Corrisponde direttamente [all'interfaccia IBackgroundCopyManager.](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) 

Dal manager viene creato un nuovo processo. Il processo è un parametro out nel metodo CreateJob. Vengono passati anche il nome del processo (che non deve essere univoco) e il tipo di download, ovvero un processo di download. Viene compilato anche un GUID BITS per l'identificatore del processo.

Dopo aver creato il processo, aggiungere un nuovo file di download al processo con il metodo AddFile. È necessario passare due stringhe, una per il file remoto (URL o condivisione file) e una per il file locale. 

Dopo aver aggiunto il file, chiamare Resume sul processo per avviarlo. Il codice attende quindi fino a quando il processo non si trova nello stato finale (ERROR o TRANSFERRED) e viene quindi completato.

### <a name="bits-versions-casting-and-queryinterface"></a>Versioni BITS, cast e QueryInterface

Spesso è necessario usare sia una versione precedente di un oggetto BITS che una versione più recente nel programma.  

Ad esempio, quando si crea un oggetto processo, si otterrà un IBackgroundCopyJob (parte di BITS versione 1.0) anche quando si usa un oggetto di gestione più recente ed è disponibile un oggetto IBackgroundCopyJob più recente. Poiché il metodo CreateJob non accetta un'interfaccia per la versione più recente, non è possibile creare direttamente la versione più recente.

Usare un cast .NET per eseguire la conversione da un oggetto di tipo meno recente a un oggetto di tipo più recente. Il cast chiamerà automaticamente un oggetto QueryInterface COM in base alle esigenze. 

In questo esempio è presente un oggetto IBackgroundCopyJob BITS denominato "job" e si vuole convertirlo in un oggetto IBackgroundCopyJob5 denominato "job5" in modo da poter chiamare il metodo GetProperty di BITS 5.0. È sufficiente eseguire il cast al tipo IBackgroundCopyJob5 come il seguente:

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

La variabile job5 verrà inizializzata da .NET usando l'interfaccia QueryInterface corretta. 

Se il codice può essere eseguito in un sistema che non supporta una particolare versione di BITS, è possibile provare il cast e intercettare System.InvalidCastException. 

```csharp
BITS5.IBackgroundCopyJob5 job5 = null;
try
{
    job5 = (BITS5.IBackgroundCopyJob5)Job;
}
catch (System.InvalidCastException)
{
    ; // Must be running an earlier version of BITS
}
```

Un problema comune è quando si tenta di eseguire il cast nel tipo di oggetto errato. Il sistema .NET non conosce la relazione reale tra le interfacce BITS. Se si richiede un tipo di interfaccia errato, .NET tenterà di renderla valida e avrà esito negativo con invalidCastException e HResult 0x80004002 (E_NOINTERFACE).

### <a name="working-with-bits-versions-10_1-and-10_2"></a>Uso delle versioni BITS 10_1 e 10_2

In alcune versioni di Windows 10 non è possibile creare direttamente un oggetto IBackgroundCopyManager BITS usando le interfacce 10.1 o 10.2. Sarà invece necessario usare più versioni dei file di riferimento della DLL BackgroundCopyManager. Ad esempio, è possibile usare la versione 1.5 per creare un oggetto IBackgroundCopyManager e quindi eseguire il cast degli oggetti processo o file risultanti usando le versioni 10.1 o 10.2.

