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
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a><span data-ttu-id="4e09f-103">Chiamata a BITS da .NET e C# usando le DLL di riferimento</span><span class="sxs-lookup"><span data-stu-id="4e09f-103">Calling into BITS from .NET and C# using Reference DLLs</span></span>

<span data-ttu-id="4e09f-104">Un modo per chiamare le classi COM BITS da un programma .NET consiste nel creare un file DLL di riferimento che inizia con i file [IDL](/windows/desktop/Midl/midl-start-page) (Interface Definition Language) bits nell'Windows SDK, usando gli strumenti [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) e [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) .</span><span class="sxs-lookup"><span data-stu-id="4e09f-104">One way to call into the BITS COM classes from a .NET program is to create a reference DLL file starting with the BITS [IDL](/windows/desktop/Midl/midl-start-page) (Interface Definition Language) files in the Windows SDK, using the [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) and [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) tools.</span></span> <span data-ttu-id="4e09f-105">La DLL di riferimento è un set di wrapper della classe per le classi COM BITS. è quindi possibile usare le classi wrapper direttamente da .NET.</span><span class="sxs-lookup"><span data-stu-id="4e09f-105">The reference DLL is a set of class wrappers for the BITS COM classes; you can then use the wrapper classes directly from .NET.</span></span>

<span data-ttu-id="4e09f-106">Un'alternativa all'uso di dll di riferimento create automaticamente consiste nell'usare un wrapper BITS .NET di terze parti da [GitHub](https://github.com/) e [NuGet](https://www.nuget.org/).</span><span class="sxs-lookup"><span data-stu-id="4e09f-106">An alternative to using automatically-created reference DLLs is to use a 3rd party .NET BITS wrapper from [GitHub](https://github.com/) and [NuGet](https://www.nuget.org/).</span></span> <span data-ttu-id="4e09f-107">Questi wrapper hanno spesso uno stile di programmazione .NET più naturale, ma potrebbero ritardare le modifiche e gli aggiornamenti nelle interfacce BITS.</span><span class="sxs-lookup"><span data-stu-id="4e09f-107">These wrappers often have a more natural .NET programming style but they might lag behind the changes and updates in the BITS interfaces.</span></span>

## <a name="creating-the-reference-dlls"></a><span data-ttu-id="4e09f-108">Creazione di dll di riferimento</span><span class="sxs-lookup"><span data-stu-id="4e09f-108">Creating the reference DLLs</span></span>
### <a name="bits-idl-files"></a><span data-ttu-id="4e09f-109">File IDL BITS</span><span class="sxs-lookup"><span data-stu-id="4e09f-109">BITS IDL files</span></span>

<span data-ttu-id="4e09f-110">Si inizierà con il set di file IDL BITS.</span><span class="sxs-lookup"><span data-stu-id="4e09f-110">You will start with the set of BITS IDL files.</span></span> <span data-ttu-id="4e09f-111">Si tratta di file che definiscono completamente l'interfaccia COM BITS.</span><span class="sxs-lookup"><span data-stu-id="4e09f-111">These are files that fully define the BITS COM interface.</span></span> <span data-ttu-id="4e09f-112">I file si trovano nella directory di **Windows Kit** e sono denominati bits *versione*. IDL (ad esempio, bits10_2. idl) ad eccezione del file della versione 1,0, che è solo BITS. idl.</span><span class="sxs-lookup"><span data-stu-id="4e09f-112">The files are located in the **Windows Kits** directory and are named bits *version*.idl (for example, bits10_2.idl) except for the version 1.0 file which is just Bits.idl.</span></span> <span data-ttu-id="4e09f-113">Quando vengono create nuove versioni di bit, vengono creati anche i nuovi file IDL di BITS.</span><span class="sxs-lookup"><span data-stu-id="4e09f-113">As new versions of BITS are created, new BITS IDL files are also created.</span></span>

<span data-ttu-id="4e09f-114">Potrebbe inoltre essere necessario modificare una copia dei file IDL BITS SDK per utilizzare le funzionalità BITS che non vengono convertite automaticamente in equivalenti .NET.</span><span class="sxs-lookup"><span data-stu-id="4e09f-114">You may also want to modify a copy of the SDK BITS IDL files to use BITS features that aren't automatically converted into .NET equivalents.</span></span> <span data-ttu-id="4e09f-115">Le modifiche al file IDL possibili verranno discusse più avanti.</span><span class="sxs-lookup"><span data-stu-id="4e09f-115">Possible IDL file changes are discussed later on.</span></span>

<span data-ttu-id="4e09f-116">I file IDL BITS includono diversi altri file IDL per riferimento.</span><span class="sxs-lookup"><span data-stu-id="4e09f-116">The BITS IDL files include several other IDL files by reference.</span></span> <span data-ttu-id="4e09f-117">Nidificano, in modo che, se si usa una versione, includa tutte le versioni inferiori.</span><span class="sxs-lookup"><span data-stu-id="4e09f-117">They also nest, so that if you use one version, it includes all the lower versions.</span></span>

<span data-ttu-id="4e09f-118">Per ogni versione di bit di destinazione nel programma è necessaria una DLL di riferimento per tale versione.</span><span class="sxs-lookup"><span data-stu-id="4e09f-118">For each version of BITS that you want to target in your program you will need one reference DLL for that version.</span></span> <span data-ttu-id="4e09f-119">Se, ad esempio, si desidera scrivere un programma che funziona su BITS 1,5 e su, ma dispone di funzionalità aggiuntive quando BITS 10,2 è presente, è necessario convertire i file bits1_5. idl e bits10_2. idl.</span><span class="sxs-lookup"><span data-stu-id="4e09f-119">For example, if you want to write a program that works on BITS 1.5 and up but has additional features when BITS 10.2 is present, you need to convert both the bits1_5.idl and bits10_2.idl files.</span></span>


### <a name="midl-and-tlbimp-utilities"></a><span data-ttu-id="4e09f-120">Utilità MIDL e TLBIMP</span><span class="sxs-lookup"><span data-stu-id="4e09f-120">MIDL and TLBIMP utilities</span></span>

<span data-ttu-id="4e09f-121">L'utilità [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft Interface Definition Language) converte i file IDL che descrivono l'interfaccia com bits in un file TLB (libreria di tipi).</span><span class="sxs-lookup"><span data-stu-id="4e09f-121">The [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft Interface Definition Language) utility converts the IDL files that describe the BITS COM interface into a TLB (Type Library) file.</span></span> <span data-ttu-id="4e09f-122">Lo strumento MIDL dipende dall'utilità CL (preprocessore C) per leggere correttamente il file di linguaggio IDL.</span><span class="sxs-lookup"><span data-stu-id="4e09f-122">The MIDL tool depends on the CL utility (C preprocessor) to correctly read the IDL language file.</span></span> <span data-ttu-id="4e09f-123">L'utilità CL fa parte di Visual Studio e viene installata quando si includono funzionalità C/C++ nell'installazione di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4e09f-123">The CL utility is part of Visual Studio and is installed when you include C/C++ features in the Visual Studio installation.</span></span>

<span data-ttu-id="4e09f-124">Tramite l'utilità MIDL viene in genere creato un set di file C e H (codice del linguaggio c e intestazione del linguaggio C).</span><span class="sxs-lookup"><span data-stu-id="4e09f-124">The MIDL utility will normally create a set of C and H (C language code and C language header) files.</span></span> <span data-ttu-id="4e09f-125">È possibile disattivare questi file aggiuntivi inviando l'output al dispositivo NUL:.</span><span class="sxs-lookup"><span data-stu-id="4e09f-125">You can suppress these extra files by sending the output to the NUL: device.</span></span> <span data-ttu-id="4e09f-126">Se, ad esempio, si imposta l'opzione/dlldata NUL:, non è possibile creare un file dlldata. c.</span><span class="sxs-lookup"><span data-stu-id="4e09f-126">For example, setting the /dlldata NUL: switch will suppress creating a dlldata.c file.</span></span> <span data-ttu-id="4e09f-127">I comandi di esempio seguenti mostrano quali opzioni devono essere impostate su NUL:.</span><span class="sxs-lookup"><span data-stu-id="4e09f-127">The sample commands below shows which switches should be set to NUL:.</span></span>

<span data-ttu-id="4e09f-128">L'utilità [Tlbimp](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (utilità di importazione della libreria dei tipi) legge in un file tlb e crea il file dll di riferimento corrispondente.</span><span class="sxs-lookup"><span data-stu-id="4e09f-128">The [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (Type Library Importer) utility reads in a TLB file and creates the corresponding reference DLL file.</span></span> 


### <a name="example-commands-for-midl-and-tlbimp"></a><span data-ttu-id="4e09f-129">Comandi di esempio per MIDL e TLBIMP</span><span class="sxs-lookup"><span data-stu-id="4e09f-129">Example commands for MIDL and TLBIMP</span></span>

<span data-ttu-id="4e09f-130">Questo è un esempio del set completo di comandi per generare un set di file di riferimento.</span><span class="sxs-lookup"><span data-stu-id="4e09f-130">This is an example of the complete set of commands to generate a set of reference files.</span></span> <span data-ttu-id="4e09f-131">Potrebbe essere necessario modificare i comandi in base all'installazione di Visual Studio e Windows SDK e basandosi sulle funzionalità BITS e sulle versioni del sistema operativo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4e09f-131">You may need to modify the commands based on your Visual Studio and Windows SDK installation and based on the BITS features and OS versions you are targeting.</span></span> 

<span data-ttu-id="4e09f-132">Nell'esempio viene creata una directory in cui inserire i file DLL di riferimento e viene creata una variabile di ambiente BITSTEMP in modo che punti a tale directory.</span><span class="sxs-lookup"><span data-stu-id="4e09f-132">The example creates a directory to place the reference DLL files and creates an environment variable BITSTEMP to point to that directory.</span></span> 

<span data-ttu-id="4e09f-133">I comandi di esempio eseguono quindi il file vsdevcmd.bat creato dal programma di installazione di Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4e09f-133">The example commands then run the vsdevcmd.bat file that's created by the Visual Studio installer.</span></span> <span data-ttu-id="4e09f-134">Questo file BAT imposterà i percorsi e alcune variabili di ambiente in modo che i comandi MIDL e TLBIMP vengano eseguiti.</span><span class="sxs-lookup"><span data-stu-id="4e09f-134">This BAT file will set up your paths and some environment variables so that the MIDL and TLBIMP commands will run.</span></span> <span data-ttu-id="4e09f-135">Vengono inoltre impostate le variabili WindowsSdkDir e WindowsSDKLibVersion in modo che puntino alle directory Windows SDK più recenti.</span><span class="sxs-lookup"><span data-stu-id="4e09f-135">It also sets up the WindowsSdkDir and WindowsSDKLibVersion variables to point to the most recent Windows SDK directories.</span></span>

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
<span data-ttu-id="4e09f-136">Dopo l'esecuzione di questi comandi, nella directory BITSTEMP sarà presente un set di dll di riferimento.</span><span class="sxs-lookup"><span data-stu-id="4e09f-136">Once these commands are run you will have a set of reference DLLs in the BITSTEMP directory.</span></span>

### <a name="adding-the-reference-dlls-to-your-project"></a><span data-ttu-id="4e09f-137">Aggiunta di dll di riferimento al progetto</span><span class="sxs-lookup"><span data-stu-id="4e09f-137">Adding the reference DLLs to your project</span></span>

<span data-ttu-id="4e09f-138">Per usare una DLL di riferimento in un progetto C#, aprire il progetto C# in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="4e09f-138">To use a reference DLL in a C# project, open your C# project in Visual Studio.</span></span> <span data-ttu-id="4e09f-139">Nella Esplora soluzioni fare clic con il pulsante destro del mouse sui riferimenti e scegliere Aggiungi riferimento.</span><span class="sxs-lookup"><span data-stu-id="4e09f-139">In the Solution Explorer, right-click the References and click Add Reference.</span></span> <span data-ttu-id="4e09f-140">Fare quindi clic sul pulsante Sfoglia e quindi sul pulsante Aggiungi.</span><span class="sxs-lookup"><span data-stu-id="4e09f-140">Then click the Browse button and then the Add button.</span></span> <span data-ttu-id="4e09f-141">Passare alla directory con le DLL di riferimento, selezionarle e fare clic su Aggiungi.</span><span class="sxs-lookup"><span data-stu-id="4e09f-141">Navigate to the directory with the reference DLLs, select them, and click Add.</span></span> <span data-ttu-id="4e09f-142">Nella finestra Gestione riferimenti verranno controllate le DLL di riferimento.</span><span class="sxs-lookup"><span data-stu-id="4e09f-142">In the Reference Manager window the reference DLLs will be checked.</span></span> <span data-ttu-id="4e09f-143">Fare quindi clic su OK.</span><span class="sxs-lookup"><span data-stu-id="4e09f-143">Then click OK.</span></span>

<span data-ttu-id="4e09f-144">Le DLL di riferimento BITS vengono ora aggiunte al progetto.</span><span class="sxs-lookup"><span data-stu-id="4e09f-144">The BITS reference DLLs are now added to your project.</span></span>

<span data-ttu-id="4e09f-145">Le informazioni nei file DLL di riferimento verranno incorporate nel programma finale.</span><span class="sxs-lookup"><span data-stu-id="4e09f-145">The information in the reference DLL files will be embedded into your final program.</span></span> <span data-ttu-id="4e09f-146">Non è necessario spedire i file DLL di riferimento al programma. è sufficiente spedire il. EXE.</span><span class="sxs-lookup"><span data-stu-id="4e09f-146">You do not have to ship the reference DLL files with your program; you just need to ship the .EXE.</span></span> 

<span data-ttu-id="4e09f-147">È possibile modificare se le DLL di riferimento sono incorporate nel file EXE finale.</span><span class="sxs-lookup"><span data-stu-id="4e09f-147">You can change whether the reference DLLs are embedded into the final EXE.</span></span> <span data-ttu-id="4e09f-148">Utilizzare la proprietà [Incorpora tipi di interoperabilità](/dotnet/framework/interop/how-to-add-references-to-type-libraries) per impostare se le DLL di riferimento verranno incorporate o meno.</span><span class="sxs-lookup"><span data-stu-id="4e09f-148">Use the [Embed Interop Types](/dotnet/framework/interop/how-to-add-references-to-type-libraries) property to set whether or not the reference DLLs will be embedded.</span></span> <span data-ttu-id="4e09f-149">Questa operazione può essere eseguita in base ai singoli riferimenti.</span><span class="sxs-lookup"><span data-stu-id="4e09f-149">This can be done on a per-reference basis.</span></span> <span data-ttu-id="4e09f-150">Il valore predefinito è true per incorporare le dll.</span><span class="sxs-lookup"><span data-stu-id="4e09f-150">The default is True to embed the DLLs.</span></span>

## <a name="modifying-idl-files-for-more-complete-net-code"></a><span data-ttu-id="4e09f-151">Modifica di file IDL per codice .NET più completo</span><span class="sxs-lookup"><span data-stu-id="4e09f-151">Modifying IDL files for more complete .NET code</span></span>

<span data-ttu-id="4e09f-152">I file IDL (Microsoft Interface Definition Language) BITS possono essere utilizzati senza modifiche per creare il file DLL BackgroundCopyManager.</span><span class="sxs-lookup"><span data-stu-id="4e09f-152">The BITS IDL (Microsoft Interface Definition Language) files can be used unchanged to make the BackgroundCopyManager DLL file.</span></span> <span data-ttu-id="4e09f-153">Tuttavia, nella DLL di riferimento .NET risultante mancano alcune unioni non convertibili e sono presenti nomi difficili da usare per alcune strutture ed enumerazioni.</span><span class="sxs-lookup"><span data-stu-id="4e09f-153">However, the resulting .NET reference DLL will be missing some untranslatable unions and has hard-to-use names for some structures and enums.</span></span> <span data-ttu-id="4e09f-154">In questa sezione vengono descritte alcune delle modifiche che è possibile apportare per rendere la DLL .NET più completa e più semplice da utilizzare.</span><span class="sxs-lookup"><span data-stu-id="4e09f-154">This section will describe some of the changes that you can make to make the .NET DLL more complete and easier to use.</span></span>

### <a name="simpler-enum-names"></a><span data-ttu-id="4e09f-155">Nomi ENUM più semplici</span><span class="sxs-lookup"><span data-stu-id="4e09f-155">Simpler ENUM names</span></span>

<span data-ttu-id="4e09f-156">I file IDL BITS definiscono in genere valori enum come il seguente:</span><span class="sxs-lookup"><span data-stu-id="4e09f-156">The BITS IDL files typically define enum values like this:</span></span>
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
<span data-ttu-id="4e09f-157">Il BG_AUTH_TARGET è il nome del typedef. l'enumerazione effettiva non è denominata.</span><span class="sxs-lookup"><span data-stu-id="4e09f-157">The BG_AUTH_TARGET is the name of the typedef; the actual enum is not named.</span></span> <span data-ttu-id="4e09f-158">Questa operazione in genere non provoca problemi con il codice C, ma non viene convertita correttamente per l'uso con un programma .NET.</span><span class="sxs-lookup"><span data-stu-id="4e09f-158">This doesn’t typically cause problems with C code but doesn’t translate well for use with a .NET program.</span></span> <span data-ttu-id="4e09f-159">Verrà creato automaticamente un nuovo nome, ma potrebbe essere simile _MIDL___MIDL_itf_bits4_0_0005_0001_0001 anziché un valore leggibile.</span><span class="sxs-lookup"><span data-stu-id="4e09f-159">A new name will be automatically created, but it might look something like _MIDL___MIDL_itf_bits4_0_0005_0001_0001 instead of a human-readable value.</span></span> <span data-ttu-id="4e09f-160">È possibile risolvere questo problema aggiornando i file MIDL in modo da includere un nome di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="4e09f-160">You can fix this problem by updating the MIDL files to include an enum name.</span></span>

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

<span data-ttu-id="4e09f-161">Il nome dell'enumerazione può essere uguale al nome del typedef.</span><span class="sxs-lookup"><span data-stu-id="4e09f-161">The enum name is allowed to be the same as the typedef name.</span></span> <span data-ttu-id="4e09f-162">Alcuni programmatori hanno una convenzione di denominazione in cui vengono mantenuti diversi, ad esempio inserendo un carattere di sottolineatura prima del nome dell'enum, ma questo confonderà solo le conversioni di .NET.</span><span class="sxs-lookup"><span data-stu-id="4e09f-162">Some programmers have a naming convention where they are kept different (for example, by putting an underscore before the enum name), but this will only confuse the .NET translations.</span></span> 

### <a name="string-types-in-unions"></a><span data-ttu-id="4e09f-163">Tipi stringa nelle unioni</span><span class="sxs-lookup"><span data-stu-id="4e09f-163">String types in unions</span></span>

<span data-ttu-id="4e09f-164">I file IDL BITS passano le stringhe usando la convenzione LPWSTR (puntatore lungo alla stringa di caratteri wide).</span><span class="sxs-lookup"><span data-stu-id="4e09f-164">The BITS IDL files pass strings using the LPWSTR (long pointer to wide-character string) convention.</span></span> <span data-ttu-id="4e09f-165">Sebbene questa operazione funzioni quando si passano parametri di funzione, ad esempio il metodo job. GetDisplayName ([out] LPWSTR \* pVal), non funziona quando le stringhe fanno parte di unioni.</span><span class="sxs-lookup"><span data-stu-id="4e09f-165">Although this works when passing function parameters (like the Job.GetDisplayName([out] LPWSTR \*pVal) method), it doesn’t work when the strings are part of unions.</span></span> <span data-ttu-id="4e09f-166">Il file bits5_0. idl, ad esempio, include l'Unione BITS_FILE_PROPERTY_VALUE:</span><span class="sxs-lookup"><span data-stu-id="4e09f-166">For example, the bits5_0.idl file includes the BITS_FILE_PROPERTY_VALUE union:</span></span>

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

<span data-ttu-id="4e09f-167">Il campo LPWSTR non verrà incluso nella versione .NET dell'Unione.</span><span class="sxs-lookup"><span data-stu-id="4e09f-167">The LPWSTR field won’t be included in the .NET version of the union.</span></span> <span data-ttu-id="4e09f-168">Per risolvere il problema, impostare LPWSTR su WCHAR \*.</span><span class="sxs-lookup"><span data-stu-id="4e09f-168">To fix this, change the LPWSTR to a WCHAR\*.</span></span> <span data-ttu-id="4e09f-169">Il campo risultante (denominato stringa) verrà passato come IntPtr.</span><span class="sxs-lookup"><span data-stu-id="4e09f-169">The resulting field (called String) will be passed as a IntPtr.</span></span> <span data-ttu-id="4e09f-170">Convertirlo in una stringa usando System. Runtime. InteropServices. Marshal. PtrToStringAuto (value. Stringa); Metodo.</span><span class="sxs-lookup"><span data-stu-id="4e09f-170">Convert this into a string using the  System.Runtime.InteropServices.Marshal.PtrToStringAuto(value.String); method.</span></span>

### <a name="unions-in-structures"></a><span data-ttu-id="4e09f-171">Unioni in strutture</span><span class="sxs-lookup"><span data-stu-id="4e09f-171">Unions in structures</span></span>

<span data-ttu-id="4e09f-172">Talvolta le unioni incorporate nelle strutture non verranno incluse nella struttura.</span><span class="sxs-lookup"><span data-stu-id="4e09f-172">Sometimes unions that are embedded in structures won't be included in the structure at all.</span></span> <span data-ttu-id="4e09f-173">Ad esempio, in Bits1_5. idl il BG_AUTH_CREDENTIALS viene definito come segue:</span><span class="sxs-lookup"><span data-stu-id="4e09f-173">For example, in the Bits1_5.idl the BG_AUTH_CREDENTIALS is defined as follows:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

<span data-ttu-id="4e09f-174">Il BG_AUTH_CREDENTIALS_UNION viene definito come un'Unione come segue:</span><span class="sxs-lookup"><span data-stu-id="4e09f-174">The BG_AUTH_CREDENTIALS_UNION is defined to be a union as follows:</span></span>
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
<span data-ttu-id="4e09f-175">Il campo delle credenziali nel BG_AUTH_CREDENTIALS non verrà incluso nella definizione della classe .NET.</span><span class="sxs-lookup"><span data-stu-id="4e09f-175">The Credentials field in the BG_AUTH_CREDENTIALS will not be included in the .NET class definition.</span></span>

<span data-ttu-id="4e09f-176">Si noti che l'Unione è definita in modo da essere sempre un BG_BASIC_CREDENTIALS indipendentemente dall'BG_AUTH_SCHEME.</span><span class="sxs-lookup"><span data-stu-id="4e09f-176">Note that the union is defined to always be a BG_BASIC_CREDENTIALS regardless of the BG_AUTH_SCHEME.</span></span> <span data-ttu-id="4e09f-177">Poiché l'Unione non viene usata come Unione, è possibile passare solo una BG_BASIC_CREDENTIALS come la seguente:</span><span class="sxs-lookup"><span data-stu-id="4e09f-177">Because the union isn’t used as a union, we can just pass a BG_BASIC_CREDENTIALS like this:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a><span data-ttu-id="4e09f-178">Utilizzo di BITS da C #</span><span class="sxs-lookup"><span data-stu-id="4e09f-178">Using BITS from C#</span></span>

### <a name="recommended-using-statement"></a><span data-ttu-id="4e09f-179">Istruzione using consigliata</span><span class="sxs-lookup"><span data-stu-id="4e09f-179">Recommended using statement</span></span>

<span data-ttu-id="4e09f-180">La configurazione di alcune istruzioni using in C# ridurrà il numero di caratteri che è necessario digitare per utilizzare le diverse versioni BITS.</span><span class="sxs-lookup"><span data-stu-id="4e09f-180">Setting up some using statements in C# will reduce the number of characters you need to type to use the different BITS versions.</span></span> <span data-ttu-id="4e09f-181">Il nome "BITSReference" deriva dal nome della DLL di riferimento.</span><span class="sxs-lookup"><span data-stu-id="4e09f-181">The name "BITSReference" comes from the name of the reference DLL.</span></span>

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a><span data-ttu-id="4e09f-182">Esempio rapido: scaricare un file</span><span class="sxs-lookup"><span data-stu-id="4e09f-182">Quick Sample: download a file</span></span>

<span data-ttu-id="4e09f-183">Di seguito è riportato un frammento breve ma completo del codice C# per scaricare un file da un URL.</span><span class="sxs-lookup"><span data-stu-id="4e09f-183">A short but complete snippet of C# code to download a file from a URL is given below.</span></span> 

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

<span data-ttu-id="4e09f-184">In questo codice di esempio viene creato un gestore BITS denominato Mgr.</span><span class="sxs-lookup"><span data-stu-id="4e09f-184">In this sample code, a BITS manager named mgr is created.</span></span> <span data-ttu-id="4e09f-185">Corrisponde direttamente all'interfaccia [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) .</span><span class="sxs-lookup"><span data-stu-id="4e09f-185">It directly corresponds to the [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) interface.</span></span> 

<span data-ttu-id="4e09f-186">Dal gestore viene creato un nuovo processo.</span><span class="sxs-lookup"><span data-stu-id="4e09f-186">From the manager a new job is created.</span></span> <span data-ttu-id="4e09f-187">Il processo è un parametro out nel metodo CreateJob.</span><span class="sxs-lookup"><span data-stu-id="4e09f-187">The job is an out parameter on the CreateJob method.</span></span> <span data-ttu-id="4e09f-188">Viene passato anche il nome del processo (che non deve essere univoco) e il tipo di download, che è un processo di download.</span><span class="sxs-lookup"><span data-stu-id="4e09f-188">Also passed in is the job name (which doesn't have to be unique) and the download type, which is a download job.</span></span> <span data-ttu-id="4e09f-189">Viene compilato anche un GUID BITS per l'identificatore di processo.</span><span class="sxs-lookup"><span data-stu-id="4e09f-189">A BITS GUID for the job identifier is also filled in.</span></span>

<span data-ttu-id="4e09f-190">Una volta creato il processo, aggiungere un nuovo file di download al processo con il metodo AddFile.</span><span class="sxs-lookup"><span data-stu-id="4e09f-190">Once the job is created you add a new download file to the job with the AddFile method.</span></span> <span data-ttu-id="4e09f-191">È necessario passare due stringhe, una per il file remoto (l'URL o la condivisione file) e una per il file locale.</span><span class="sxs-lookup"><span data-stu-id="4e09f-191">You need to pass in two strings, one for the remote file (the URL or file share) and one for the local file.</span></span> 

<span data-ttu-id="4e09f-192">Dopo l'aggiunta del file, chiamare Resume sul processo per avviarlo.</span><span class="sxs-lookup"><span data-stu-id="4e09f-192">After adding the file, call Resume on the job to start it.</span></span> <span data-ttu-id="4e09f-193">Il codice attende quindi che il processo sia in uno stato finale (errore o trasferito) e quindi completato.</span><span class="sxs-lookup"><span data-stu-id="4e09f-193">Then the code waits until the job is in a final state (ERROR or TRANSFERRED) and is then completed.</span></span>

### <a name="bits-versions-casting-and-queryinterface"></a><span data-ttu-id="4e09f-194">Versioni BITS, cast e QueryInterface</span><span class="sxs-lookup"><span data-stu-id="4e09f-194">BITS Versions, Casting and QueryInterface</span></span>

<span data-ttu-id="4e09f-195">Si noterà che è spesso necessario usare una versione iniziale di un oggetto BITS e una versione più recente del programma.</span><span class="sxs-lookup"><span data-stu-id="4e09f-195">You'll find that you often have to use both an early version of a BITS object and a more recent version in your program.</span></span>  

<span data-ttu-id="4e09f-196">Quando si crea un oggetto processo, ad esempio, si otterrà un metodo ibackgroundcopyjob (parte di BITS versione 1,0) anche quando si usa un oggetto Manager più recente e è disponibile un oggetto Metodo ibackgroundcopyjob più recente.</span><span class="sxs-lookup"><span data-stu-id="4e09f-196">For example, when you make a job object, you will get an IBackgroundCopyJob (part of BITS version 1.0) even when you're making it using a more recent manager object and a more recent IBackgroundCopyJob object is available.</span></span> <span data-ttu-id="4e09f-197">Poiché il metodo CreateJob non accetta un'interfaccia per la versione più recente, non è possibile creare direttamente la versione più recente.</span><span class="sxs-lookup"><span data-stu-id="4e09f-197">Because the CreateJob method doesn't accept an interface for the more recent version, you can't directly make the more recent version.</span></span>

<span data-ttu-id="4e09f-198">Usare un cast .NET per eseguire la conversione da un oggetto di tipo precedente a un oggetto di tipo più recente.</span><span class="sxs-lookup"><span data-stu-id="4e09f-198">Use a .NET cast to convert from an older type object to a newer type object.</span></span> <span data-ttu-id="4e09f-199">Il cast chiamerà automaticamente un COM QueryInterface nel modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="4e09f-199">The cast will automatically call a COM QueryInterface as appropriate.</span></span> 

<span data-ttu-id="4e09f-200">In questo esempio è presente un oggetto BITS metodo ibackgroundcopyjob denominato "Job" e si vuole convertirlo in un oggetto IBackgroundCopyJob5 denominato "job5" in modo che sia possibile chiamare il metodo BITS 5,0 GetProperty.</span><span class="sxs-lookup"><span data-stu-id="4e09f-200">In this example, there's a BITS IBackgroundCopyJob object named "job", and we want to convert it to an IBackgroundCopyJob5 object named "job5" so that we can call the BITS 5.0 GetProperty method.</span></span> <span data-ttu-id="4e09f-201">È sufficiente eseguire il cast al tipo IBackgroundCopyJob5 come segue:</span><span class="sxs-lookup"><span data-stu-id="4e09f-201">We just cast to the IBackgroundCopyJob5 type like this:</span></span>

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

<span data-ttu-id="4e09f-202">La variabile job5 viene inizializzata da .NET utilizzando la funzione QueryInterface corretta.</span><span class="sxs-lookup"><span data-stu-id="4e09f-202">The job5 variable will be initialized by .NET by using the correct QueryInterface.</span></span> 

<span data-ttu-id="4e09f-203">Se il codice potrebbe essere eseguito in un sistema che non supporta una particolare versione di bit, è possibile provare il cast e rilevare System. InvalidCastException.</span><span class="sxs-lookup"><span data-stu-id="4e09f-203">If your code might run on a system that doesn't support a particular version of BITS, you can try the cast and catch the System.InvalidCastException.</span></span> 

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

<span data-ttu-id="4e09f-204">Un problema comune è quando si tenta di eseguire il cast nel tipo di oggetto errato.</span><span class="sxs-lookup"><span data-stu-id="4e09f-204">A common problem is when you try to cast into the wrong kind of object.</span></span> <span data-ttu-id="4e09f-205">Il sistema .NET non conosce la relazione reale tra le interfacce BITS.</span><span class="sxs-lookup"><span data-stu-id="4e09f-205">The .NET system doesn't know about the real relationship between the BITS interfaces.</span></span> <span data-ttu-id="4e09f-206">Se si richiede un tipo di interfaccia errato, .NET tenterà di crearla e avrà esito negativo con un'eccezione InvalidCastException e HResult 0X80004002 (E_NOINTERFACE).</span><span class="sxs-lookup"><span data-stu-id="4e09f-206">If you ask for the wrong kind of interface, .NET will try to make it for you and will fail with an InvalidCastException and HResult 0x80004002 (E_NOINTERFACE).</span></span>

### <a name="working-with-bits-versions-10_1-and-10_2"></a><span data-ttu-id="4e09f-207">Uso delle versioni BITS 10_1 e 10_2</span><span class="sxs-lookup"><span data-stu-id="4e09f-207">Working with BITS Versions 10_1 and 10_2</span></span>

<span data-ttu-id="4e09f-208">In alcune versioni di Windows 10 non è possibile creare direttamente un oggetto BITS IBackgroundCopyManager usando le interfacce 10,1 o 10,2.</span><span class="sxs-lookup"><span data-stu-id="4e09f-208">On some versions of Windows 10 you can't directly create a BITS IBackgroundCopyManager object using the 10.1 or 10.2 interfaces.</span></span> <span data-ttu-id="4e09f-209">Sarà invece necessario usare più versioni dei file di riferimento della DLL BackgroundCopyManager.</span><span class="sxs-lookup"><span data-stu-id="4e09f-209">Instead, you'll have to use multiple versions of the BackgroundCopyManager DLL reference files.</span></span> <span data-ttu-id="4e09f-210">Ad esempio, è possibile usare la versione 1,5 per creare un oggetto IBackgroundCopyManager, quindi eseguire il cast del processo o degli oggetti file risultante usando le versioni 10,1 o 10,2.</span><span class="sxs-lookup"><span data-stu-id="4e09f-210">For example, you can use the 1.5 version to make an IBackgroundCopyManager object, and then cast the resulting job or file objects using the 10.1 or 10.2 versions.</span></span>

