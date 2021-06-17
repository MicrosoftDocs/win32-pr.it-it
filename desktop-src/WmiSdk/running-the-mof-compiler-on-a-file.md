---
description: "Durante la compilazione di un file MOF sono disponibili due opzioni: l'uso dell'utilità della riga di comando o l'uso di un'interfaccia a livello di codice."
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Esecuzione del compilatore MOF in un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f62834944e995c3e7f3763c460d72f9f70aa66
ms.sourcegitcommit: 7eadd92b1da5eb4eab7d516a5a768e7f7fc02d4c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/16/2021
ms.locfileid: "112230248"
---
# <a name="running-the-mof-compiler-on-a-file"></a><span data-ttu-id="de94f-103">Esecuzione del compilatore MOF in un file</span><span class="sxs-lookup"><span data-stu-id="de94f-103">Running the MOF Compiler on a File</span></span>

<span data-ttu-id="de94f-104">Durante la compilazione di un file MOF sono disponibili due opzioni: l'uso dell'utilità della riga di comando o l'uso di un'interfaccia a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="de94f-104">You have two choices when compiling a MOF file: using the command-line utility or using a programmatic interface.</span></span>

<span data-ttu-id="de94f-105">Fino a quando non si esegue il compilatore MOF, [**Mofcomp.exe**](mofcomp.md), un provider non è registrato con WMI e le classi create nel file MOF non sono disponibili nel [*repository WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="de94f-105">Until you run the MOF compiler, [**Mofcomp.exe**](mofcomp.md), a provider is not registered with WMI and the classes it created in the MOF file are not available in the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="de94f-106">La procedura seguente descrive come compilare un file MOF.</span><span class="sxs-lookup"><span data-stu-id="de94f-106">The following procedure describes how to compile a MOF file.</span></span>

<span data-ttu-id="de94f-107">**Per eseguire il compilatore MOF in un file dalla riga di comando**</span><span class="sxs-lookup"><span data-stu-id="de94f-107">**To run the MOF compiler on a file from the command line**</span></span>

1.  <span data-ttu-id="de94f-108">Chiamare il compilatore MOF dalla riga di comando usando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="de94f-108">Call the MOF compiler from the command line, using the following syntax.</span></span>

    <span data-ttu-id="de94f-109">**mofcomp** _MOFfile_**.mof**</span><span class="sxs-lookup"><span data-stu-id="de94f-109">**mofcomp** _MOFfile_**.mof**</span></span>

    <span data-ttu-id="de94f-110">Il compilatore MOF supporta un'ampia gamma di opzioni per controllare situazioni di elaborazione speciali.</span><span class="sxs-lookup"><span data-stu-id="de94f-110">The MOF compiler supports a variety of switches to control special processing situations.</span></span> <span data-ttu-id="de94f-111">Tutte le opzioni sono facoltative ed è consentita qualsiasi combinazione di opzioni.</span><span class="sxs-lookup"><span data-stu-id="de94f-111">All of the switches are optional, and any combination of switches is allowed.</span></span> <span data-ttu-id="de94f-112">Tuttavia, non ha senso usare alcune opzioni in combinazione con altre.</span><span class="sxs-lookup"><span data-stu-id="de94f-112">However, it does not make sense to use some of the switches in combination with others.</span></span> <span data-ttu-id="de94f-113">Ad esempio, per combinare le opzioni **-class:updateonly** e **-class:createonly,** il compilatore non esegue alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="de94f-113">For example, to combine the **-class:updateonly** and **-class:createonly** switches results in the compiler not performing any action.</span></span>

    <span data-ttu-id="de94f-114">Per impostazione predefinita, Mofcomp.exe le classi compilate nello spazio dei \\ nomi WMI predefinito radice.</span><span class="sxs-lookup"><span data-stu-id="de94f-114">By default, Mofcomp.exe stores the compiled classes in the root\\default WMI namespace.</span></span> <span data-ttu-id="de94f-115">Si noti che lo spazio dei nomi predefinito Mofcomp.exe non corrisponde allo spazio dei nomi predefinito per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="de94f-115">Note that the default namespace for Mofcomp.exe is not the same as the default namespace for scripting.</span></span> <span data-ttu-id="de94f-116">Lo spazio dei nomi predefinito per lo scripting viene specificato nel controllo WMI nella scheda Avanzate . Per altre informazioni, vedere [Impostazione della sicurezza dello spazio dei nomi con il controllo WMI.](setting-namespace-security-with-the-wmi-control.md)</span><span class="sxs-lookup"><span data-stu-id="de94f-116">The default namespace for scripting is specified in the WMI Control on the Advanced tab. For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

    <span data-ttu-id="de94f-117">È possibile modificare lo spazio dei nomi che riceve le classi in due modi.</span><span class="sxs-lookup"><span data-stu-id="de94f-117">You can change the namespace that receives the classes in two ways.</span></span>

    1.  <span data-ttu-id="de94f-118">Usare **l'opzione -N** per il **comando mofcomp.**</span><span class="sxs-lookup"><span data-stu-id="de94f-118">Use the **-N** switch for the **mofcomp** command.</span></span>
    2.  <span data-ttu-id="de94f-119">Inserire lo spazio dei nomi pragma del \# [**comando del**](pragma-namespace.md) preprocessore nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="de94f-119">Insert the preprocessor command \#[**pragma namespace**](pragma-namespace.md) in the MOF file.</span></span>

2.  <span data-ttu-id="de94f-120">Facoltativamente, è possibile compilare un file MOF a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="de94f-120">Optionally, you can compile a MOF file programmatically.</span></span> <span data-ttu-id="de94f-121">Per altre informazioni, vedere [**IMofCompiler.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)</span><span class="sxs-lookup"><span data-stu-id="de94f-121">For more information, see [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span></span>

## <a name="related-topics"></a><span data-ttu-id="de94f-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="de94f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de94f-123">Compilazione di file MOF</span><span class="sxs-lookup"><span data-stu-id="de94f-123">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="de94f-124">**mofcomp**</span><span class="sxs-lookup"><span data-stu-id="de94f-124">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="de94f-125">Comandi del preprocessore</span><span class="sxs-lookup"><span data-stu-id="de94f-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



