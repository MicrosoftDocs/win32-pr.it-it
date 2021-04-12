---
description: "Per la compilazione di un file MOF sono disponibili due opzioni: utilizzo dell'utilità da riga di comando o di un'interfaccia a livello di codice."
ms.assetid: 1760f1bd-7027-4201-97a2-ca902f945b52
ms.tgt_platform: multiple
title: Esecuzione del compilatore MOF in un file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad1605544e05f59670f9e6fd73fcd8c01862b46c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226830"
---
# <a name="running-the-mof-compiler-on-a-file"></a><span data-ttu-id="199f0-103">Esecuzione del compilatore MOF in un file</span><span class="sxs-lookup"><span data-stu-id="199f0-103">Running the MOF Compiler on a File</span></span>

<span data-ttu-id="199f0-104">Per la compilazione di un file MOF sono disponibili due opzioni: utilizzo dell'utilità da riga di comando o di un'interfaccia a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="199f0-104">You have two choices when compiling a MOF file: using the command-line utility or using a programmatic interface.</span></span>

<span data-ttu-id="199f0-105">Fino a quando non si esegue il compilatore MOF, [**Mofcomp.exe**](mofcomp.md), un provider non è registrato con WMI e le classi create nel file MOF non sono disponibili nel [*repository WMI*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="199f0-105">Until you run the MOF compiler, [**Mofcomp.exe**](mofcomp.md), a provider is not registered with WMI and the classes it created in the MOF file are not available in the [*WMI repository*](gloss-w.md).</span></span> <span data-ttu-id="199f0-106">Nella procedura seguente viene descritto come compilare un file MOF.</span><span class="sxs-lookup"><span data-stu-id="199f0-106">The following procedure describes how to compile a MOF file.</span></span>

<span data-ttu-id="199f0-107">**Per eseguire il compilatore MOF in un file dalla riga di comando**</span><span class="sxs-lookup"><span data-stu-id="199f0-107">**To run the MOF compiler on a file from the command line**</span></span>

1.  <span data-ttu-id="199f0-108">Chiamare il compilatore MOF dalla riga di comando, usando la sintassi seguente.</span><span class="sxs-lookup"><span data-stu-id="199f0-108">Call the MOF compiler from the command line, using the following syntax.</span></span>

    <span data-ttu-id="199f0-109">**mofcomp** *MOFfile \* \* *. mof**</span><span class="sxs-lookup"><span data-stu-id="199f0-109">**mofcomp** *MOFfile\*\*\*.mof*\*</span></span>

    <span data-ttu-id="199f0-110">Il compilatore MOF supporta un'ampia gamma di opzioni per il controllo di particolari situazioni di elaborazione.</span><span class="sxs-lookup"><span data-stu-id="199f0-110">The MOF compiler supports a variety of switches to control special processing situations.</span></span> <span data-ttu-id="199f0-111">Tutte le opzioni sono facoltative ed è consentita qualsiasi combinazione di opzioni.</span><span class="sxs-lookup"><span data-stu-id="199f0-111">All of the switches are optional, and any combination of switches is allowed.</span></span> <span data-ttu-id="199f0-112">Tuttavia, non ha senso usare alcuni dei commutatori in combinazione con altri.</span><span class="sxs-lookup"><span data-stu-id="199f0-112">However, it does not make sense to use some of the switches in combination with others.</span></span> <span data-ttu-id="199f0-113">Ad esempio, per combinare le opzioni **-Class: updateonly** e **-Class: createonly** i risultati del compilatore non eseguono alcuna azione.</span><span class="sxs-lookup"><span data-stu-id="199f0-113">For example, to combine the **-class:updateonly** and **-class:createonly** switches results in the compiler not performing any action.</span></span>

    <span data-ttu-id="199f0-114">Per impostazione predefinita, Mofcomp.exe archivia le classi compilate nello \\ spazio dei nomi WMI predefinito radice.</span><span class="sxs-lookup"><span data-stu-id="199f0-114">By default, Mofcomp.exe stores the compiled classes in the root\\default WMI namespace.</span></span> <span data-ttu-id="199f0-115">Si noti che lo spazio dei nomi predefinito per Mofcomp.exe non corrisponde allo spazio dei nomi predefinito per lo scripting.</span><span class="sxs-lookup"><span data-stu-id="199f0-115">Note that the default namespace for Mofcomp.exe is not the same as the default namespace for scripting.</span></span> <span data-ttu-id="199f0-116">Lo spazio dei nomi predefinito per lo scripting è specificato nel controllo WMI nella scheda Avanzate. Per ulteriori informazioni, vedere [impostazione della sicurezza dello spazio dei nomi con il controllo WMI](setting-namespace-security-with-the-wmi-control.md).</span><span class="sxs-lookup"><span data-stu-id="199f0-116">The default namespace for scripting is specified in the WMI Control on the Advanced tab. For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

    <span data-ttu-id="199f0-117">È possibile modificare lo spazio dei nomi che riceve le classi in due modi.</span><span class="sxs-lookup"><span data-stu-id="199f0-117">You can change the namespace that receives the classes in two ways.</span></span>

    1.  <span data-ttu-id="199f0-118">Utilizzare l'opzione **-N** per il comando **mofcomp** .</span><span class="sxs-lookup"><span data-stu-id="199f0-118">Use the **-N** switch for the **mofcomp** command.</span></span>
    2.  <span data-ttu-id="199f0-119">Inserire lo \# [**spazio dei nomi pragma**](pragma-namespace.md) del comando per il preprocessore nel file MOF.</span><span class="sxs-lookup"><span data-stu-id="199f0-119">Insert the preprocessor command \#[**pragma namespace**](pragma-namespace.md) in the MOF file.</span></span>

2.  <span data-ttu-id="199f0-120">Facoltativamente, è possibile compilare un file MOF a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="199f0-120">Optionally, you can compile a MOF file programmatically.</span></span> <span data-ttu-id="199f0-121">Per ulteriori informazioni, vedere [**IMOFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span><span class="sxs-lookup"><span data-stu-id="199f0-121">For more information, see [**IMofCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler).</span></span>

## <a name="related-topics"></a><span data-ttu-id="199f0-122">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="199f0-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="199f0-123">Compilazione di file MOF</span><span class="sxs-lookup"><span data-stu-id="199f0-123">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="199f0-124">**mofcomp**</span><span class="sxs-lookup"><span data-stu-id="199f0-124">**mofcomp**</span></span>](mofcomp.md)
</dt> <dt>

[<span data-ttu-id="199f0-125">Comandi del preprocessore</span><span class="sxs-lookup"><span data-stu-id="199f0-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 



