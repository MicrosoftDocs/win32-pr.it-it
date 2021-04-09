---
title: Sintassi della riga di comando MIDL generale
description: Il compilatore MIDL elabora un file IDL e un file di configurazione dell'applicazione (ACF) facoltativo per generare un set di file di output.
ms.assetid: 1906b374-d0d1-4ec8-9a00-c5228b4c29ca
keywords:
- riferimento alla riga di comando MIDL, sintassi generale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14baa145c7be03467a24bd4298cf2f502d93b6ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856845"
---
# <a name="general-midl-command-line-syntax"></a><span data-ttu-id="77c18-104">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="77c18-104">General MIDL Command-line Syntax</span></span>

<span data-ttu-id="77c18-105">Il compilatore MIDL elabora un file IDL e un file di configurazione dell'applicazione (ACF) facoltativo per generare un set di file di output.</span><span class="sxs-lookup"><span data-stu-id="77c18-105">The MIDL compiler processes an IDL file and an optional application configuration file (ACF) to generate a set of output files.</span></span> <span data-ttu-id="77c18-106">Gli attributi specificati nell'elenco di attributi di interfaccia del file IDL determinano se il compilatore genera file di origine per un'interfaccia RPC o per un'interfaccia OLE personalizzata.</span><span class="sxs-lookup"><span data-stu-id="77c18-106">The attributes specified in the IDL file's interface attribute list determine whether the compiler generates source files for an RPC interface or for a custom OLE interface.</span></span>

## <a name="switch-options"></a><span data-ttu-id="77c18-107">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="77c18-107">Switch Options</span></span>

``` syntax
     midl [command-line-switch [switch-options]] filename
    
```

<dl> <dt>

<span data-ttu-id="77c18-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*opzione della riga di comando*</span><span class="sxs-lookup"><span data-stu-id="77c18-108"><span id="command-line-switch"></span><span id="COMMAND-LINE-SWITCH"></span>*command-line-switch*</span></span>
</dt> <dd>

<span data-ttu-id="77c18-109">Specifica le opzioni della riga di comando del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="77c18-109">Specifies MIDL compiler command-line switches.</span></span> <span data-ttu-id="77c18-110">Le opzioni possono essere visualizzate in qualsiasi sequenza.</span><span class="sxs-lookup"><span data-stu-id="77c18-110">Switches can appear in any sequence.</span></span>

</dd> <dt>

<span data-ttu-id="77c18-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*opzioni switch*</span><span class="sxs-lookup"><span data-stu-id="77c18-111"><span id="switch-options"></span><span id="SWITCH-OPTIONS"></span>*switch-options*</span></span>
</dt> <dd>

<span data-ttu-id="77c18-112">Specifica le opzioni associate a ogni opzione.</span><span class="sxs-lookup"><span data-stu-id="77c18-112">Specifies options associated with each switch.</span></span> <span data-ttu-id="77c18-113">Le opzioni valide sono descritte nella voce di riferimento per ogni opzione del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="77c18-113">Valid options are described in the reference entry for each MIDL compiler switch.</span></span>

</dd> <dt>

<span data-ttu-id="77c18-114"><span id="filename"></span><span id="FILENAME"></span>*filename*</span><span class="sxs-lookup"><span data-stu-id="77c18-114"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="77c18-115">Specifica il nome del file IDL.</span><span class="sxs-lookup"><span data-stu-id="77c18-115">Specifies the name of the IDL file.</span></span> <span data-ttu-id="77c18-116">Questo file contiene in genere l'estensione IDL, ma può avere un altro o nessuno.</span><span class="sxs-lookup"><span data-stu-id="77c18-116">This file usually has the extension .idl, but it can have another or none.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77c18-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="77c18-117">Remarks</span></span>

<span data-ttu-id="77c18-118">Negli elenchi seguenti vengono illustrati i nomi predefiniti dei file generati per un file IDL denominato name. idl.</span><span class="sxs-lookup"><span data-stu-id="77c18-118">The following lists show the default names of the files generated for an IDL file named Name.idl.</span></span> <span data-ttu-id="77c18-119">È possibile utilizzare le opzioni della riga di comando per eseguire l'override di questi nomi predefiniti.</span><span class="sxs-lookup"><span data-stu-id="77c18-119">You can use command-line switches to override these default names.</span></span> <span data-ttu-id="77c18-120">Si noti che il nome del file IDL può avere un'estensione diversa da IDL oppure nessuna estensione.</span><span class="sxs-lookup"><span data-stu-id="77c18-120">Note that the name of the IDL file can have an extension other than .idl, or no extension at all.</span></span>

<span data-ttu-id="77c18-121">Per impostazione predefinita, ovvero se l'elenco di attributi di interfaccia non contiene l' [**oggetto**](object.md) o l'attributo [**locale**](local.md) , il compilatore genera i file seguenti per un' [interfaccia RPC](files-generated-for-an-rpc-interface.md):</span><span class="sxs-lookup"><span data-stu-id="77c18-121">By default (that is, if the interface attribute list does not contain the [**object**](object.md) or [**local**](local.md) attribute), the compiler generates the following files for an [RPC interface](files-generated-for-an-rpc-interface.md):</span></span>

-   <span data-ttu-id="77c18-122">Stub client (nome \_ c. c)</span><span class="sxs-lookup"><span data-stu-id="77c18-122">Client stub (name\_c.c)</span></span>
-   <span data-ttu-id="77c18-123">Stub Server (nome \_ s. c)</span><span class="sxs-lookup"><span data-stu-id="77c18-123">Server stub (name\_s.c)</span></span>
-   <span data-ttu-id="77c18-124">File di intestazione (Name. h)</span><span class="sxs-lookup"><span data-stu-id="77c18-124">Header file (name.h)</span></span>

<span data-ttu-id="77c18-125">Quando l'attributo dell' [**oggetto**](object.md) viene visualizzato nell'elenco di attributi di interfaccia, il compilatore genera i file seguenti per un'interfaccia com:</span><span class="sxs-lookup"><span data-stu-id="77c18-125">When the [**object**](object.md) attribute appears in the interface attribute list, the compiler generates the following files for a COM interface:</span></span>

-   <span data-ttu-id="77c18-126">File proxy di interfaccia (nome \_ p. c)</span><span class="sxs-lookup"><span data-stu-id="77c18-126">Interface proxy file (name\_p.c)</span></span>
-   <span data-ttu-id="77c18-127">File di intestazione dell'interfaccia (Name. h)</span><span class="sxs-lookup"><span data-stu-id="77c18-127">Interface header file (name.h)</span></span>
-   <span data-ttu-id="77c18-128">File UUID dell'interfaccia (nome \_ I. c)</span><span class="sxs-lookup"><span data-stu-id="77c18-128">Interface UUID file (name\_I.c)</span></span>

<span data-ttu-id="77c18-129">Quando l'attributo [**local**](local.md) viene visualizzato nell'elenco di attributi di interfaccia, il compilatore genera solo il file di intestazione dell'interfaccia, Name. h.</span><span class="sxs-lookup"><span data-stu-id="77c18-129">When the [**local**](local.md) attribute appears in the interface attribute list, the compiler generates only the interface header file, Name.h.</span></span>

<span data-ttu-id="77c18-130">Il compilatore MIDL fornito con Microsoft RPC richiama il preprocessore C in base alle esigenze per elaborare il file IDL.</span><span class="sxs-lookup"><span data-stu-id="77c18-130">The MIDL compiler provided with Microsoft RPC invokes the C preprocessor as needed to process the IDL file.</span></span> <span data-ttu-id="77c18-131">Non richiama automaticamente il compilatore C per compilare i file generati.</span><span class="sxs-lookup"><span data-stu-id="77c18-131">It does not automatically invoke the C compiler to compile generated files.</span></span>

> [!Note]  
> <span data-ttu-id="77c18-132">Il compilatore MIDL fornito con Microsoft RPC usa una sintassi della riga di comando diversa da quella del compilatore IDL DCE.</span><span class="sxs-lookup"><span data-stu-id="77c18-132">The MIDL compiler provided with Microsoft RPC uses a different command-line syntax than the DCE IDL compiler.</span></span>

 

<span data-ttu-id="77c18-133">Il compilatore MIDL passa [**/ENV**](-env.md), [**/Server**](-server.md), [**/sstub**](-sstub.md)e [**/out**](-out.md) influisce sul file stub del server.</span><span class="sxs-lookup"><span data-stu-id="77c18-133">The MIDL compiler switches [**/env**](-env.md), [**/server**](-server.md), [**/sstub**](-sstub.md), and [**/out**](-out.md) affect the server stub file.</span></span>

<span data-ttu-id="77c18-134">A partire dalla versione MIDL 6.0.359, l'opzione della riga di comando predefinita per il compilatore MIDL è [**/Oicf**](-oi.md)Â  [**/robust**](-robust.md).</span><span class="sxs-lookup"><span data-stu-id="77c18-134">Starting with MIDL version 6.0.359, the default command line option for the MIDL compiler is [**/Oicf**](-oi.md)Â  [**/robust**](-robust.md).</span></span> <span data-ttu-id="77c18-135">Per disabilitare/robust, specificare l'opzione [**/No \_ Solid**](-no-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="77c18-135">To disable /robust, specify the [**/no\_robust**](-no-robust.md) option.</span></span>

## <a name="the-header-file"></a><span data-ttu-id="77c18-136">Il file di intestazione</span><span class="sxs-lookup"><span data-stu-id="77c18-136">The Header File</span></span>

<span data-ttu-id="77c18-137">Il file di intestazione contiene le definizioni di tutti i tipi di dati e le operazioni dichiarate nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="77c18-137">The header file contains definitions of all the data types and operations declared in the IDL file.</span></span> <span data-ttu-id="77c18-138">Il file di intestazione deve essere incluso in tutti i moduli dell'applicazione che chiamano le operazioni definite, implementano le operazioni definite o modificano i tipi definiti.</span><span class="sxs-lookup"><span data-stu-id="77c18-138">The header file must be included by all application modules that call the defined operations, implement the defined operations, or manipulate the defined types.</span></span>

<span data-ttu-id="77c18-139">Il compilatore MIDL passa [**/header**](-header.md) e [**/out**](-out.md) influisce sul file di intestazione.</span><span class="sxs-lookup"><span data-stu-id="77c18-139">The MIDL compiler switches [**/header**](-header.md) and [**/out**](-out.md) affect the header file.</span></span>

 

 




