---
title: C-requisiti per il preprocessore MIDL
description: Questa pagina è valida solo per gli sviluppatori che hanno motivi specifici per sostituire il preprocessore Microsoft C/C++ come preprocessore utilizzato da MIDL o per sviluppatori che devono specificare opzioni personalizzate per il preprocessore.
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- MIDL compilatore MIDL, C-preprocessore, requisiti
- C-preprocessore MIDL, requisiti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49c4e0c086a52eda2705d72cf2a2ff22c759290
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955697"
---
# <a name="c-preprocessor-requirements-for-midl"></a><span data-ttu-id="91422-105">C-requisiti per il preprocessore MIDL</span><span class="sxs-lookup"><span data-stu-id="91422-105">C-Preprocessor Requirements for MIDL</span></span>

<span data-ttu-id="91422-106">Questa pagina è valida solo per gli sviluppatori che hanno motivi specifici per sostituire il preprocessore Microsoft C/C++ come preprocessore utilizzato da MIDL o per sviluppatori che devono specificare opzioni personalizzate per il preprocessore.</span><span class="sxs-lookup"><span data-stu-id="91422-106">This page applies only to developers who have specific reasons to replace the Microsoft C/C++ preprocessor as the preprocessor used by MIDL, or to developers who must specify customized preprocessor switches.</span></span> <span data-ttu-id="91422-107">I commutatori MIDL [**/cpp \_ cmd**](-cpp-cmd.md), [**/cpp \_ opt**](-cpp-opt.md)e [**/No \_ cpp**](-no-cpp-nocpp.md) vengono usati per eseguire l'override del comportamento predefinito del compilatore.</span><span class="sxs-lookup"><span data-stu-id="91422-107">The MIDL switches [**/cpp\_cmd**](-cpp-cmd.md), [**/cpp\_opt**](-cpp-opt.md), and [**/no\_cpp**](-no-cpp-nocpp.md) are used to override the default behavior of the compiler.</span></span> <span data-ttu-id="91422-108">Non esiste in genere un motivo per sostituire il preprocessore Microsoft C/C++, né per specificare opzioni per il preprocessore personalizzate.</span><span class="sxs-lookup"><span data-stu-id="91422-108">There is typically no reason to replace the Microsoft C/C++ preprocessor, nor to specify customized preprocessor switches.</span></span>

<span data-ttu-id="91422-109">Il compilatore MIDL usa un preprocessore C durante l'elaborazione iniziale del file IDL.</span><span class="sxs-lookup"><span data-stu-id="91422-109">The MIDL compiler uses a C preprocessor during initial processing of the IDL file.</span></span> <span data-ttu-id="91422-110">L'ambiente di compilazione utilizzato per la compilazione dei file IDL è associato a un preprocessore di C/C++ predefinito.</span><span class="sxs-lookup"><span data-stu-id="91422-110">The build environment used when compiling the IDL files is associated with a default C/C++ preprocessor.</span></span> <span data-ttu-id="91422-111">Se è necessario usare un preprocessore diverso, l'opzione del compilatore MIDL [**/cpp \_ cmd**](-cpp-cmd.md) Abilita un override del nome predefinito del preprocessore C/C++:</span><span class="sxs-lookup"><span data-stu-id="91422-111">If a different preprocessor is to be used, the MIDL compiler switch [**/cpp\_cmd**](-cpp-cmd.md) enables an override of the default C/C++-preprocessor name:</span></span>

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span data-ttu-id="91422-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*nome del preprocessore \_*</span><span class="sxs-lookup"><span data-stu-id="91422-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*preprocessor\_name*</span></span>
</dt> <dd>

<span data-ttu-id="91422-113">Specifica il nome del preprocessore che deve essere usato da MIDL.</span><span class="sxs-lookup"><span data-stu-id="91422-113">Specifies the name of the preprocessor to be used by MIDL.</span></span> <span data-ttu-id="91422-114">Può essere specificato con un percorso del file binario.</span><span class="sxs-lookup"><span data-stu-id="91422-114">May be specified with a path to the binary.</span></span> <span data-ttu-id="91422-115">L'estensione exe è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="91422-115">The .exe extension is optional.</span></span>

</dd> <dt>

<span data-ttu-id="91422-116"><span id="filename"></span><span id="FILENAME"></span>*filename*</span><span class="sxs-lookup"><span data-stu-id="91422-116"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="91422-117">Specifica il nome del file IDL.</span><span class="sxs-lookup"><span data-stu-id="91422-117">Specifies the name of the IDL file.</span></span>

</dd> </dl>

-   <span data-ttu-id="91422-118">Il compilatore MIDL prevede che qualsiasi preprocessore osservi le convenzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="91422-118">The MIDL compiler expects any preprocessor to observe the following conventions:</span></span>
-   <span data-ttu-id="91422-119">Il file di input viene specificato come ultimo argomento nella riga di comando.</span><span class="sxs-lookup"><span data-stu-id="91422-119">The input file is specified as the last argument on the command line.</span></span>
-   <span data-ttu-id="91422-120">Il preprocessore deve reindirizzare l'output al dispositivo di output standard, stdout.</span><span class="sxs-lookup"><span data-stu-id="91422-120">The preprocessor must redirect output to the standard output device, stdout.</span></span>
-   <span data-ttu-id="91422-121">Nel flusso di output del preprocessore sono presenti le direttive **\# line** che consentono di migliorare i messaggi di diagnostica.</span><span class="sxs-lookup"><span data-stu-id="91422-121">In the output stream of the preprocessor, the **\#line** directives are present to enable better diagnostic messages.</span></span>
-   <span data-ttu-id="91422-122">Le direttive line sono le uniche direttive per il preprocessore nel flusso di output.</span><span class="sxs-lookup"><span data-stu-id="91422-122">The line directives are the only preprocessor directives in the output stream.</span></span>

<span data-ttu-id="91422-123">MIDL presuppone che il preprocessore generato abbia rimosso tutte le direttive del preprocessore dal flusso di input del compilatore, fatta eccezione per le occorrenze della direttiva di riga necessaria per individuare il percorso di origine nei messaggi del compilatore.</span><span class="sxs-lookup"><span data-stu-id="91422-123">MIDL assumes that the spawned preprocessor has removed all preprocessor directives from the input stream of the compiler, with the exception of the occurrences of the line directive necessary for pinpointing source location in compiler messages.</span></span> <span data-ttu-id="91422-124">Quando viene indicato un preprocessore diverso dal preprocessore Microsoft C/C++ o quando si specificano le opzioni del preprocessore con l'opzione [**/cpp \_ opt**](-cpp-opt.md) , è necessario specificare un'opzione del preprocessore appropriata che inserisce le direttive di riga nel flusso di input del compilatore.</span><span class="sxs-lookup"><span data-stu-id="91422-124">When indicating a preprocessor different from the Microsoft C/C++ preprocessor, or when specifying preprocessor options with the [**/cpp\_opt**](-cpp-opt.md) switch, specifying an appropriate preprocessor option that puts the line directives in the input stream of the compiler is required.</span></span> <span data-ttu-id="91422-125">Per il preprocessore Microsoft C/C++, ad esempio, è necessario usare l'opzione **/e** :</span><span class="sxs-lookup"><span data-stu-id="91422-125">For example, for the Microsoft C/C++ preprocessor the **/E** option would have to be used:</span></span>

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

<span data-ttu-id="91422-126">La direttiva **\# line** viene accettata da MIDL in uno dei formati seguenti:</span><span class="sxs-lookup"><span data-stu-id="91422-126">The **\#line** directive is accepted by MIDL in one of the following forms:</span></span>

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

<span data-ttu-id="91422-127">Per una descrizione completa della direttiva line e di altre direttive per il preprocessore, vedere la documentazione relativa al compilatore C usato.</span><span class="sxs-lookup"><span data-stu-id="91422-127">For a complete description of the line directive and other preprocessor directives, see the documentation for the C-compiler being used.</span></span>

<span data-ttu-id="91422-128">MIDL accetta solo la direttiva per il preprocessore line.</span><span class="sxs-lookup"><span data-stu-id="91422-128">MIDL accepts only the line preprocessor directive.</span></span> <span data-ttu-id="91422-129">Di conseguenza, se si usa l'opzione [**\_ cpp/no**](-no-cpp-nocpp.md) , il file di input non deve avere altre direttive per il preprocessore oppure il file di input deve essere stato elaborato prima di richiamare MIDL.</span><span class="sxs-lookup"><span data-stu-id="91422-129">Therefore, if the [**/no\_cpp**](-no-cpp-nocpp.md) switch is used, the input file must not have other preprocessor directives, or the input file must have been processed prior to invoking MIDL.</span></span>

<span data-ttu-id="91422-130">Per ulteriori informazioni, vedere la pagina relativa alla [gestione delle \# definizioni nei file IDL](dealing-with-defines-in-idl-files-2.md).</span><span class="sxs-lookup"><span data-stu-id="91422-130">For more information, see [Dealing with \#defines in IDL Files](dealing-with-defines-in-idl-files-2.md).</span></span>

 

 




