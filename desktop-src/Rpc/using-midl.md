---
title: Uso di MIDL
description: Creazione e compilazione di un'interfaccia Microsoft Interface Definition Language (MIDL) e RPC (Remote Procedure Call).
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da60f20cba6c558c7f1a67478adef7b407d591
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730015"
---
# <a name="using-midl"></a><span data-ttu-id="b6dbd-103">Uso di MIDL</span><span class="sxs-lookup"><span data-stu-id="b6dbd-103">Using MIDL</span></span>

<span data-ttu-id="b6dbd-104">Tutte le interfacce per i programmi che usano RPC devono essere definite in Microsoft Interface Definition Language (MIDL) e compilate con il compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-104">All interfaces for programs using RPC must be defined in Microsoft Interface Definition Language (MIDL) and compiled with the MIDL compiler.</span></span> <span data-ttu-id="b6dbd-105">Negli argomenti seguenti viene presentata una breve panoramica sulla creazione e la compilazione di un'interfaccia MIDL:</span><span class="sxs-lookup"><span data-stu-id="b6dbd-105">The following topics present a brief overview of creating and compiling a MIDL interface:</span></span>

-   [<span data-ttu-id="b6dbd-106">Definizione di un'interfaccia con MIDL</span><span class="sxs-lookup"><span data-stu-id="b6dbd-106">Defining an Interface with MIDL</span></span>](#defining-an-interface-with-midl)
-   [<span data-ttu-id="b6dbd-107">Compilazione di un file MIDL</span><span class="sxs-lookup"><span data-stu-id="b6dbd-107">Compiling a MIDL File</span></span>](#compiling-a-midl-file)

<span data-ttu-id="b6dbd-108">Per una descrizione dettagliata di questi argomenti, vedere [i file IDL e ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="b6dbd-108">For a detailed discussion of these topics, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

## <a name="defining-an-interface-with-midl"></a><span data-ttu-id="b6dbd-109">Definizione di un'interfaccia con MIDL</span><span class="sxs-lookup"><span data-stu-id="b6dbd-109">Defining an Interface with MIDL</span></span>

<span data-ttu-id="b6dbd-110">I file MIDL sono file di testo che è possibile creare e modificare con un editor di testo.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-110">MIDL files are text files that you can create and edit with a text editor.</span></span> <span data-ttu-id="b6dbd-111">Se si genera un UUID per l'interfaccia, in genere l'output viene archiviato in un file MIDL del modello.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-111">If you generate a UUID for your interface, you will typically store the output in a template MIDL file.</span></span> <span data-ttu-id="b6dbd-112">Per altre informazioni sugli UUID, vedere [generazione di UUID di interfaccia](generating-interface-uuids.md).</span><span class="sxs-lookup"><span data-stu-id="b6dbd-112">For more information on UUIDs, see [Generating Interface UUIDs](generating-interface-uuids.md).</span></span>

<span data-ttu-id="b6dbd-113">Tutte le interfacce in MIDL seguono lo stesso formato.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-113">All interfaces in MIDL follow the same format.</span></span> <span data-ttu-id="b6dbd-114">Iniziano con un'intestazione contenente un elenco di attributi di interfaccia e il nome dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-114">They begin with a header that contains a list of interface attributes and the interface name.</span></span> <span data-ttu-id="b6dbd-115">Gli attributi sono racchiusi tra parentesi quadre.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-115">The attributes are enclosed in square brackets.</span></span> <span data-ttu-id="b6dbd-116">L'intestazione dell'interfaccia è seguita dal corpo, racchiuso tra parentesi graffe.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-116">The interface header is followed by its body, which is enclosed in curly brackets.</span></span> <span data-ttu-id="b6dbd-117">Nell'esempio seguente viene illustrata un'interfaccia semplice:</span><span class="sxs-lookup"><span data-stu-id="b6dbd-117">A simple interface is shown in the following example:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface MyInterface
{
  const unsigned short INT_ARRAY_LEN = 100;

  void MyRemoteProc( 
      [in] int param1,
      [out] int outArray[INT_ARRAY_LEN]
  );
}
```

<span data-ttu-id="b6dbd-118">Alcuni degli attributi che in genere compaiono in una definizione di interfaccia MIDL sono UUID e il numero di versione dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-118">Some of the attributes that typically appear in a MIDL interface definition are the UUID and the interface version number.</span></span> <span data-ttu-id="b6dbd-119">Il corpo della definizione dell'interfaccia deve contenere le dichiarazioni di routine di tutte le procedure remote nell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-119">The body of the interface definition must contain the procedure declarations of all of the remote procedures in the interface.</span></span> <span data-ttu-id="b6dbd-120">Può inoltre contenere le dichiarazioni dei tipi di dati e delle costanti richieste dall'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-120">It can also contain the declarations of data types and constants required by the interface.</span></span>

<span data-ttu-id="b6dbd-121">Tutti i parametri nelle dichiarazioni di procedura remota devono essere dichiarati come \[ [**in**](/windows/desktop/Midl/in) \] , \[ [**out**](/windows/desktop/Midl/out-idl) \] o \[ **in**, **out** \] .</span><span class="sxs-lookup"><span data-stu-id="b6dbd-121">All parameters in the remote procedure declarations must be declared as \[[**in**](/windows/desktop/Midl/in)\], \[[**out**](/windows/desktop/Midl/out-idl)\], or \[**in**, **out**\].</span></span> <span data-ttu-id="b6dbd-122">Queste dichiarazioni specificano che il programma client passa i dati in una procedura remota, ottiene i dati da una procedura remota o entrambi.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-122">These declarations specify that the client program passes data into a remote procedure, gets data out of a remote procedure, or both.</span></span> <span data-ttu-id="b6dbd-123">Per informazioni più dettagliate sulle dichiarazioni dei parametri di interfaccia, vedere [il corpo dell'interfaccia IDL](the-idl-interface-body.md).</span><span class="sxs-lookup"><span data-stu-id="b6dbd-123">For more detailed information about interface parameter declarations, see [The IDL Interface Body](the-idl-interface-body.md).</span></span>

## <a name="compiling-a-midl-file"></a><span data-ttu-id="b6dbd-124">Compilazione di un file MIDL</span><span class="sxs-lookup"><span data-stu-id="b6dbd-124">Compiling a MIDL File</span></span>

<span data-ttu-id="b6dbd-125">Il compilatore MIDL è uno strumento da riga di comando che viene installato automaticamente con Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="b6dbd-125">The MIDL compiler is a command-line tool that is automatically installed with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="b6dbd-126">Richiamarlo in una finestra di comando digitando il comando **MIDL**, seguito dal nome di un file MIDL, nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-126">Invoke it in a command window by typing the command **midl**, followed by the name of a MIDL file, at the command line.</span></span> <span data-ttu-id="b6dbd-127">Assicurarsi che la directory contenente il compilatore MIDL si trovi nel percorso.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-127">Make sure that the directory containing the MIDL compiler is in your path.</span></span> <span data-ttu-id="b6dbd-128">Nell'esempio seguente viene illustrato l'utilizzo di:</span><span class="sxs-lookup"><span data-stu-id="b6dbd-128">The following example illustrates its use:</span></span>

<span data-ttu-id="b6dbd-129">**MIDL MyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="b6dbd-129">**midl MyApp.idl**</span></span>

<span data-ttu-id="b6dbd-130">Si noti che non è necessario includere l'estensione se il nome file ha l'estensione. idl.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-130">Note that you do not have to include the extension if the file name has the .idl extension.</span></span> <span data-ttu-id="b6dbd-131">È anche possibile usare le opzioni della [riga di comando](/windows/desktop/Midl/midl-command-line-reference) del compilatore MIDL inserendole tra il comando **MIDL** e il nome del file.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-131">You can also use the MIDL compiler [command-line switches](/windows/desktop/Midl/midl-command-line-reference) by inserting them between the **midl** command and the file name.</span></span> <span data-ttu-id="b6dbd-132">Questa operazione è illustrata nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="b6dbd-132">This is demonstrated in the following example:</span></span>

<span data-ttu-id="b6dbd-133">**MIDL/ACF MyApp. ACF MyApp. idl**</span><span class="sxs-lookup"><span data-stu-id="b6dbd-133">**midl /acf MyApp.acf MyApp.idl**</span></span>

<span data-ttu-id="b6dbd-134">In questo esempio, il compilatore MIDL viene eseguito utilizzando il file MyApp. idl come file di input.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-134">In this example, the MIDL compiler is executed using the file MyApp.idl as the input file.</span></span> <span data-ttu-id="b6dbd-135">L'opzione della riga di comando **/ACF** indica al compilatore di usare un file di configurazione dell'applicazione (ACF) anche per l'input.</span><span class="sxs-lookup"><span data-stu-id="b6dbd-135">The command line switch **/acf** instructs the compiler to use an application configuration file (ACF) for input as well.</span></span> <span data-ttu-id="b6dbd-136">I file di configurazione dell'applicazione sono trattati più accuratamente nei [file IDL e ACF](the-idl-and-acf-files.md).</span><span class="sxs-lookup"><span data-stu-id="b6dbd-136">Application configuration files are discussed more thoroughly in [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="b6dbd-137">Per informazioni più dettagliate sull'uso del compilatore MIDL, vedere il [Microsoft Interface Definition Language (MIDL)](/windows/desktop/Midl/midl-start-page), che contiene informazioni sugli argomenti seguenti:</span><span class="sxs-lookup"><span data-stu-id="b6dbd-137">For more detailed information on using the MIDL compiler, see the [Microsoft Interface Definition Language (MIDL)](/windows/desktop/Midl/midl-start-page), which contains information on the following topics:</span></span>

-   [<span data-ttu-id="b6dbd-138">C-requisiti per il preprocessore MIDL</span><span class="sxs-lookup"><span data-stu-id="b6dbd-138">C-Preprocessor Requirements for MIDL</span></span>](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [<span data-ttu-id="b6dbd-139">C/C++-considerazioni sul compilatore</span><span class="sxs-lookup"><span data-stu-id="b6dbd-139">C/C++-Compiler Considerations</span></span>](/windows/desktop/Midl/c-c-compiler-considerations)
-   [<span data-ttu-id="b6dbd-140">File generati per un'interfaccia RPC</span><span class="sxs-lookup"><span data-stu-id="b6dbd-140">Files Generated for an RPC Interface</span></span>](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [<span data-ttu-id="b6dbd-141">Riferimenti alla riga di comando MIDL</span><span class="sxs-lookup"><span data-stu-id="b6dbd-141">MIDL Command-line Reference</span></span>](/windows/desktop/Midl/midl-command-line-reference)
-   [<span data-ttu-id="b6dbd-142">Riferimenti per il linguaggio MIDL</span><span class="sxs-lookup"><span data-stu-id="b6dbd-142">MIDL Language Reference</span></span>](/windows/desktop/Midl/midl-language-reference)
-   [<span data-ttu-id="b6dbd-143">Errori e avvisi del compilatore MIDL</span><span class="sxs-lookup"><span data-stu-id="b6dbd-143">MIDL Compiler Errors and Warnings</span></span>](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 