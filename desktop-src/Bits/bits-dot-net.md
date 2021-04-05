---
title: Uso di BITS da .NET con dll di riferimento
description: Negli esempi seguenti viene illustrato come chiamare l'interfaccia COM BITS da un programma .NET
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c359bafe4f1937d49a6ec21896af32606a2ae894
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/26/2019
ms.locfileid: "103719582"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a>Chiamata a BITS da .NET e C# usando le DLL di riferimento

Un modo per chiamare le classi COM BITS da un programma .NET consiste nel creare un file DLL di riferimento che inizia con i file [IDL](/windows/desktop/Midl/midl-start-page) (Interface Definition Language) bits nell'Windows SDK, usando gli strumenti [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) e [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) . La DLL di riferimento è un set di wrapper della classe per le classi COM BITS. è quindi possibile usare le classi wrapper direttamente da .NET.

Un'alternativa all'uso di dll di riferimento create automaticamente consiste nell'usare un wrapper BITS .NET di terze parti da [GitHub](https://github.com/) e [NuGet](https://www.nuget.org/). Questi wrapper hanno spesso uno stile di programmazione .NET più naturale, ma potrebbero ritardare le modifiche e gli aggiornamenti nelle interfacce BITS.

## <a name="creating-the-reference-dlls"></a>Creazione di dll di riferimento
### <a name="bits-idl-files"></a>File IDL BITS

Si inizierà con il set di file IDL BITS. Si tratta di file che definiscono completamente l'interfaccia COM BITS. I file si trovano nella directory di **Windows Kit** e sono denominati bits *versione*. IDL (ad esempio, bits10_2. idl) ad eccezione del file della versione 1,0, che è solo BITS. idl. Quando vengono create nuove versioni di bit, vengono creati anche i nuovi file IDL di BITS.

Potrebbe inoltre essere necessario modificare una copia dei file IDL BITS SDK per utilizzare le funzionalità BITS che non vengono convertite automaticamente in equivalenti .NET. Le modifiche al file IDL possibili verranno discusse più avanti.

I file IDL BITS includono diversi altri file IDL per riferimento. Nidificano, in modo che, se si usa una versione, includa tutte le versioni inferiori.

Per ogni versione di bit di destinazione nel programma è necessaria una DLL di riferimento per tale versione. Se, ad esempio, si desidera scrivere un programma che funziona su BITS 1,5 e su, ma dispone di funzionalità aggiuntive quando BITS 10,2 è presente, è necessario convertire i file bits1_5. idl e bits10_2. idl.


### <a name="midl-and-tlbimp-utilities"></a>Utilità MIDL e TLBIMP

L'utilità [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft Interface Definition Language) converte i file IDL che descrivono l'interfaccia com bits in un file TLB (libreria di tipi). Lo strumento MIDL dipende dall'utilità CL (preprocessore C) per leggere correttamente il file di linguaggio IDL. L'utilità CL fa parte di Visual Studio e viene installata quando si includono funzionalità C/C++ nell'installazione di Visual Studio.

Tramite l'utilità MIDL viene in genere creato un set di file C e H (codice del linguaggio c e intestazione del linguaggio C). È possibile disattivare questi file aggiuntivi inviando l'output al dispositivo NUL:. Se, ad esempio, si imposta l'opzione/dlldata NUL:, non è possibile creare un file dlldata. c. I comandi di esempio seguenti mostrano quali opzioni devono essere impostate su NUL:.

L'utilità [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (utilità di importazione della libreria dei tipi) legge in un file tlb e crea il file dll di riferimento corrispondente. 


### <a name="example-commands-for-midl-and-tlbimp"></a>Comandi di esempio per MIDL e TLBIMP

Questo è un esempio del set completo di comandi per generare un set di file di riferimento. Potrebbe essere necessario modificare i comandi in base all'installazione di Visual Studio e Windows SDK e basandosi sulle funzionalità BITS e sulle versioni del sistema operativo di destinazione. 

Nell'esempio viene creata una directory in cui inserire i file DLL di riferimento e viene creata una variabile di ambiente BITSTEMP in modo che punti a tale directory. 

I comandi di esempio eseguono quindi il file vsdevcmd.bat creato dal programma di installazione di Visual Studio. Questo file BAT imposterà i percorsi e alcune variabili di ambiente in modo che i comandi MIDL e TLBIMP vengano eseguiti. Vengono inoltre impostate le variabili WindowsSdkDir e WindowsSDKLibVersion in modo che puntino alle directory Windows SDK più recenti.

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
Dopo l'esecuzione di questi comandi, nella directory BITSTEMP sarà presente un set di dll di riferimento.

### <a name="adding-the-reference-dlls-to-your-project"></a>Aggiunta di dll di riferimento al progetto

Per usare una DLL di riferimento in un progetto C#, aprire il progetto C# in Visual Studio. Nella Esplora soluzioni fare clic con il pulsante destro del mouse sui riferimenti e scegliere Aggiungi riferimento. Fare quindi clic sul pulsante Sfoglia e quindi sul pulsante Aggiungi. Passare alla directory con le DLL di riferimento, selezionarle e fare clic su Aggiungi. Nella finestra Gestione riferimenti verranno controllate le DLL di riferimento. Fare quindi clic su OK.

Le DLL di riferimento BITS vengono ora aggiunte al progetto.

Le informazioni nei file DLL di riferimento verranno incorporate nel programma finale. Non è necessario spedire i file DLL di riferimento al programma. è sufficiente spedire il. EXE. 

È possibile modificare se le DLL di riferimento sono incorporate nel file EXE finale. Utilizzare la proprietà [Incorpora tipi di interoperabilità](/dotnet/framework/interop/how-to-add-references-to-type-libraries) per impostare se le DLL di riferimento verranno incorporate o meno. Questa operazione può essere eseguita in base ai singoli riferimenti. Il valore predefinito è true per incorporare le dll.

## <a name="modifying-idl-files-for-more-complete-net-code"></a>Modifica di file IDL per codice .NET più completo

I file IDL (Microsoft Interface Definition Language) BITS possono essere utilizzati senza modifiche per creare il file DLL BackgroundCopyManager. Tuttavia, nella DLL di riferimento .NET risultante mancano alcune unioni non convertibili e sono presenti nomi difficili da usare per alcune strutture ed enumerazioni. In questa sezione vengono descritte alcune delle modifiche che è possibile apportare per rendere la DLL .NET più completa e più semplice da utilizzare.

### <a name="simpler-enum-names"></a>Nomi ENUM più semplici

I file IDL BITS definiscono in genere valori enum come il seguente:
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
Il BG_AUTH_TARGET è il nome del typedef. l'enumerazione effettiva non è denominata. Questa operazione in genere non provoca problemi con il codice C, ma non viene convertita correttamente per l'uso con un programma .NET. Verrà creato automaticamente un nuovo nome, ma potrebbe essere simile _MIDL___MIDL_itf_bits4_0_0005_0001_0001 anziché un valore leggibile. È possibile risolvere questo problema aggiornando i file MIDL in modo da includere un nome di enumerazione.

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

Il nome dell'enumerazione può essere uguale al nome del typedef. Alcuni programmatori hanno una convenzione di denominazione in cui vengono mantenuti diversi, ad esempio inserendo un carattere di sottolineatura prima del nome dell'enum, ma questo confonderà solo le conversioni di .NET. 

### <a name="string-types-in-unions"></a>Tipi stringa nelle unioni

I file IDL BITS passano le stringhe usando la convenzione LPWSTR (puntatore lungo alla stringa di caratteri wide). Sebbene questa operazione funzioni quando si passano parametri di funzione, ad esempio il metodo job. GetDisplayName ([out] LPWSTR * pVal), non funziona quando le stringhe fanno parte di unioni. Il file bits5_0. idl, ad esempio, include l'Unione BITS_FILE_PROPERTY_VALUE:

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

Il campo LPWSTR non verrà incluso nella versione .NET dell'Unione. Per risolvere il problema, impostare LPWSTR su WCHAR *. Il campo risultante (denominato stringa) verrà passato come IntPtr. Convertirlo in una stringa usando System. Runtime. InteropServices. Marshal. PtrToStringAuto (value. Stringa); Metodo.

### <a name="unions-in-structures"></a>Unioni in strutture

Talvolta le unioni incorporate nelle strutture non verranno incluse nella struttura. Ad esempio, in Bits1_5. idl il BG_AUTH_CREDENTIALS viene definito come segue:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

Il BG_AUTH_CREDENTIALS_UNION viene definito come un'Unione come segue:
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
Il campo delle credenziali nel BG_AUTH_CREDENTIALS non verrà incluso nella definizione della classe .NET.

Si noti che l'Unione è definita in modo da essere sempre un BG_BASIC_CREDENTIALS indipendentemente dall'BG_AUTH_SCHEME. Poiché l'Unione non viene usata come Unione, è possibile passare solo una BG_BASIC_CREDENTIALS come la seguente:
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a>Utilizzo di BITS da C #

### <a name="recommended-using-statement"></a>Istruzione using consigliata

La configurazione di alcune istruzioni using in C# ridurrà il numero di caratteri che è necessario digitare per utilizzare le diverse versioni BITS. Il nome "BITSReference" deriva dal nome della DLL di riferimento.

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a>Esempio rapido: scaricare un file

Di seguito è riportato un frammento breve ma completo del codice C# per scaricare un file da un URL. 

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

In questo codice di esempio viene creato un gestore BITS denominato Mgr. Corrisponde direttamente all'interfaccia [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) . 

Dal gestore viene creato un nuovo processo. Il processo è un parametro out nel metodo CreateJob. Viene passato anche il nome del processo (che non deve essere univoco) e il tipo di download, che è un processo di download. Viene compilato anche un GUID BITS per l'identificatore di processo.

Una volta creato il processo, aggiungere un nuovo file di download al processo con il metodo AddFile. È necessario passare due stringhe, una per il file remoto (l'URL o la condivisione file) e una per il file locale. 

Dopo l'aggiunta del file, chiamare Resume sul processo per avviarlo. Il codice attende quindi che il processo sia in uno stato finale (errore o trasferito) e quindi completato.

### <a name="bits-versions-casting-and-queryinterface"></a>Versioni BITS, cast e QueryInterface

Si noterà che è spesso necessario usare una versione iniziale di un oggetto BITS e una versione più recente del programma.  

Quando si crea un oggetto processo, ad esempio, si otterrà un metodo ibackgroundcopyjob (parte di BITS versione 1,0) anche quando si usa un oggetto Manager più recente e è disponibile un oggetto Metodo ibackgroundcopyjob più recente. Poiché il metodo CreateJob non accetta un'interfaccia per la versione più recente, non è possibile creare direttamente la versione più recente.

Usare un cast .NET per eseguire la conversione da un oggetto di tipo precedente a un oggetto di tipo più recente. Il cast chiamerà automaticamente un COM QueryInterface nel modo appropriato. 

In questo esempio è presente un oggetto BITS metodo ibackgroundcopyjob denominato "Job" e si vuole convertirlo in un oggetto IBackgroundCopyJob5 denominato "job5" in modo che sia possibile chiamare il metodo BITS 5,0 GetProperty. È sufficiente eseguire il cast al tipo IBackgroundCopyJob5 come segue:

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

La variabile job5 viene inizializzata da .NET utilizzando la funzione QueryInterface corretta. 

Se il codice potrebbe essere eseguito in un sistema che non supporta una particolare versione di bit, è possibile provare il cast e rilevare System. InvalidCastException. 

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

Un problema comune è quando si tenta di eseguire il cast nel tipo di oggetto errato. Il sistema .NET non conosce la relazione reale tra le interfacce BITS. Se si richiede un tipo di interfaccia errato, .NET tenterà di crearla e avrà esito negativo con un'eccezione InvalidCastException e HResult 0X80004002 (E_NOINTERFACE).

### <a name="working-with-bits-versions-10_1-and-10_2"></a>Uso delle versioni BITS 10_1 e 10_2

In alcune versioni di Windows 10 non è possibile creare direttamente un oggetto BITS IBackgroundCopyManager usando le interfacce 10,1 o 10,2. Sarà invece necessario usare più versioni dei file di riferimento della DLL BackgroundCopyManager. Ad esempio, è possibile usare la versione 1,5 per creare un oggetto IBackgroundCopyManager, quindi eseguire il cast del processo o degli oggetti file risultante usando le versioni 10,1 o 10,2.

