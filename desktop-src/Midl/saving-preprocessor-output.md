---
title: Salvataggio dell'output del preprocessore
description: La visualizzazione dell'output del preprocessore può essere un metodo efficace per la risoluzione dei problemi, ad esempio quando si verifica una sintassi non valida per il preprocessore IDL, C o C, oppure quando i valori fittizi-D nella riga di comando MIDL generano errori arcani di segnalazione MIDL.
ms.assetid: 79c53f0c-c179-4731-a2c3-a1022d378e7b
keywords:
- MIDL Compiler MIDL, salvataggio dell'output del preprocessore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49ca1e07658fb2da525999e396b7c3da27add385
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396214"
---
# <a name="saving-preprocessor-output"></a><span data-ttu-id="70bbe-104">Salvataggio dell'output del preprocessore</span><span class="sxs-lookup"><span data-stu-id="70bbe-104">Saving Preprocessor Output</span></span>

<span data-ttu-id="70bbe-105">La visualizzazione dell'output del preprocessore può essere un metodo efficace per la risoluzione dei problemi, ad esempio quando si verifica una sintassi non valida per il preprocessore IDL, C o C, oppure quando i valori fittizi-D nella riga di comando MIDL generano errori arcani di segnalazione MIDL.</span><span class="sxs-lookup"><span data-stu-id="70bbe-105">Viewing preprocessor output can be an effective troubleshooting method, such as when invalid IDL, C, or C-preprocessor syntax occurs, or when bogus -D values on the MIDL command line result in MIDL reporting arcane errors.</span></span> <span data-ttu-id="70bbe-106">Gli sviluppatori possono anche esaminare l'output del preprocessore per determinare quali file e definizioni erano presenti nel flusso di input del compilatore, ad esempio quando è necessario risolvere un caso complesso di conflitti di ridefinizione dei tipi.</span><span class="sxs-lookup"><span data-stu-id="70bbe-106">Developers may also want to examine preprocessor output to determine which files and definitions were present in the compiler input stream, such as when a difficult case of type redefinition conflict must be resolved.</span></span> <span data-ttu-id="70bbe-107">O meno comunemente, determinati sviluppatori potrebbero voler forzare i commutatori privati sul preprocessore con [**/cpp \_ opt**](-cpp-opt.md)o vedere come funzionano i commutatori.</span><span class="sxs-lookup"><span data-stu-id="70bbe-107">Or less commonly, certain developers may want to force private switches on the preprocessor with [**/cpp\_opt**](-cpp-opt.md), or may want to see how the switches work.</span></span>

<span data-ttu-id="70bbe-108">Il modo più semplice e meno intrusivo per ottenere i file pre-elaborati da un'esecuzione di compilazione MIDL consiste nell'usare l'opzione [**-savePP**](-savepp.md) .</span><span class="sxs-lookup"><span data-stu-id="70bbe-108">The easiest and the least obtrusive way to obtain the preprocessed files from a MIDL compile run is to use the [**-savePP**](-savepp.md) switch.</span></span> <span data-ttu-id="70bbe-109">L'opzione **-savePP** impedisce semplicemente a MIDL di eliminare i file temporanei che il preprocessore passa di nuovo a MIDL.</span><span class="sxs-lookup"><span data-stu-id="70bbe-109">The **-savePP** switch simply prevents MIDL from deleting the temporary files that the preprocessor passes back to MIDL.</span></span> <span data-ttu-id="70bbe-110">Considerare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="70bbe-110">Consider the following:</span></span>

<span data-ttu-id="70bbe-111">**MIDL-savePP-ID: \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1-Oicf-ENV Win32 stub. idl**</span><span class="sxs-lookup"><span data-stu-id="70bbe-111">**midl -savePP -Id:\\nt\\public\\sdk\\inc -DNTENV=1 -Oicf -env win32 stub.idl**</span></span>

<span data-ttu-id="70bbe-112">Questa direttiva compila stub. idl, mantenendo tuttavia tutti i file del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="70bbe-112">This directive compiles Stub.idl, yet preserves all preprocessor files.</span></span>

> [!Note]  
> <span data-ttu-id="70bbe-113">MIDL genera esecuzioni del preprocessore separate per il file IDL e ACF (se presente), nonché per ogni file importato.</span><span class="sxs-lookup"><span data-stu-id="70bbe-113">MIDL spawns separate preprocessor runs for IDL and ACF file (if present) as well as for every imported file.</span></span>

 

<span data-ttu-id="70bbe-114">Per una compilazione DCOM, in genere vengono prodotti diversi file del preprocessore, anche se vengono elaborati da MIDL come flusso di input contiguo virtuale.</span><span class="sxs-lookup"><span data-stu-id="70bbe-114">For a DCOM compile, several preprocessor files are typically produced, even though they are processed by MIDL as a virtual contiguous input stream.</span></span> <span data-ttu-id="70bbe-115">In un ambiente di programmazione Windows tipico, i file temporanei sono disponibili nella directory Temp come nomi di file, ad esempio MID \* . tmp.</span><span class="sxs-lookup"><span data-stu-id="70bbe-115">In a typical Windows programming environment, the temporary files can be found in the Temp directory as file names such as MID\*.tmp.</span></span> <span data-ttu-id="70bbe-116">Se si conserva l'output del preprocessore, è consigliabile controllare i file recenti nella directory Temp per identificare quali file sono associati al preprocessore eseguito.</span><span class="sxs-lookup"><span data-stu-id="70bbe-116">If preserving preprocessor output, it is good practice to watch for recent files in the Temp directory to identify which files are associated with which preprocessor run.</span></span>

<span data-ttu-id="70bbe-117">In casi semplici, ad esempio quando il file IDL compilato non importa altri file direttamente o indirettamente oppure quando si esamina il file di livello superiore, il preprocessore può essere richiamato direttamente.</span><span class="sxs-lookup"><span data-stu-id="70bbe-117">In simple cases, such as when the compiled IDL file does not import other files directly or indirectly, or when examining the top-level file, the preprocessor can be invoked directly.</span></span> <span data-ttu-id="70bbe-118">L'esecuzione diretta del preprocessore C/C++ può rivelare errori mascherati o confusi da MIDL.</span><span class="sxs-lookup"><span data-stu-id="70bbe-118">Executing C/C++ preprocessor directly can reveal errors masked or confused by MIDL.</span></span> <span data-ttu-id="70bbe-119">Ad esempio, le due righe di comando per il preprocessore seguenti possono essere utilizzate per la riga MIDL precedentemente racchiusa tra virgolette:</span><span class="sxs-lookup"><span data-stu-id="70bbe-119">For example, the following two preprocessor command lines can be used for the previously quoted MIDL line:</span></span>

<span data-ttu-id="70bbe-120">**CL/E/nologo-ID: \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1 stub. idl > stub. PP**</span><span class="sxs-lookup"><span data-stu-id="70bbe-120">**cl /E /nologo -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl > stub.pp**</span></span>

<span data-ttu-id="70bbe-121">**CL/E/P-ID: \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1 stub. idl**</span><span class="sxs-lookup"><span data-stu-id="70bbe-121">**cl /E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1 stub.idl**</span></span>

<span data-ttu-id="70bbe-122">Nel primo di questi due esempi, **/e** [**/nologo**](-nologo.md) sono i commutatori aggiunti da MIDL quando si richiama il preprocessore.</span><span class="sxs-lookup"><span data-stu-id="70bbe-122">In the first of these two examples, **/E** [**/nologo**](-nologo.md) are the switches that MIDL adds when invoking the preprocessor.</span></span> <span data-ttu-id="70bbe-123">L'output del preprocessore viene inviato a stdout (schermata) e pertanto richiede il reindirizzamento a un file per l'analisi.</span><span class="sxs-lookup"><span data-stu-id="70bbe-123">The preprocessor output is sent to stdout (the screen), and therefore requires redirection to a file for examination.</span></span> <span data-ttu-id="70bbe-124">Nel secondo di questi esempi, **/p** indica al preprocessore di reindirizzare l'output a un \* file con estensione i, in questo caso verrà creato un file stub. i nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="70bbe-124">In the second of these examples, **/P** directs the preprocessor to redirect the output to a \*.i file; in this case a Stub.i file would be created in the current directory.</span></span>

<span data-ttu-id="70bbe-125">L'opzione [**/cpp \_ opt**](-cpp-opt.md) può essere usata anche per ottenere un file pre-elaborato, ma è difficile e inferiore ai metodi citati in precedenza.</span><span class="sxs-lookup"><span data-stu-id="70bbe-125">The [**/cpp\_opt**](-cpp-opt.md) switch can also be used to obtain a preprocessed file, but is difficult and inferior to the previously mentioned methods.</span></span> <span data-ttu-id="70bbe-126">Nell'esempio seguente viene inoltre generato un file stub. i, come nell'esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="70bbe-126">The following example also produces a Stub.i file, as did the previous example.</span></span> <span data-ttu-id="70bbe-127">Le virgolette nell'esempio seguente sono essenziali:</span><span class="sxs-lookup"><span data-stu-id="70bbe-127">The quotes in the following example are essential:</span></span>

<span data-ttu-id="70bbe-128">**MIDL-Oicf-Win32-cpp \_ opz "/E/p-ID: \\ NT \\ public \\ SDK \\ Inc-DNTENV = 1" Stub. idl**</span><span class="sxs-lookup"><span data-stu-id="70bbe-128">**Midl -Oicf -win32 -cpp\_opt "/E /P -Id:\\nt\\public\\sdk\\inc -DNTENV=1" stub.idl**</span></span>

 

 




