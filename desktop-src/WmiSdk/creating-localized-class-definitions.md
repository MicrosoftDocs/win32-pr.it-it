---
description: La creazione di definizioni di classe localizzate è un processo in tre passaggi.
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: Creazione di definizioni di classi localizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41a183c1478c259b0428cd827088a769e680425
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320844"
---
# <a name="creating-localized-class-definitions"></a><span data-ttu-id="c6b96-103">Creazione di definizioni di classi localizzate</span><span class="sxs-lookup"><span data-stu-id="c6b96-103">Creating Localized Class Definitions</span></span>

<span data-ttu-id="c6b96-104">La creazione di definizioni di classe localizzate è un processo in tre passaggi.</span><span class="sxs-lookup"><span data-stu-id="c6b96-104">Creating localized class definitions is a three-step process.</span></span> <span data-ttu-id="c6b96-105">Si inizia scrivendo codice MOF che definisce le classi, inclusi tutti i qualificatori che devono essere localizzati.</span><span class="sxs-lookup"><span data-stu-id="c6b96-105">You start by writing MOF code that defines the classes, including all qualifiers that must be localized.</span></span> <span data-ttu-id="c6b96-106">Questo file originale è denominato file "Master MOF" perché contiene tutti i qualificatori e le proprietà che definiscono la classe.</span><span class="sxs-lookup"><span data-stu-id="c6b96-106">This original file is called the "master MOF" file because it contains all of the qualifiers and properties that define the class.</span></span>

<span data-ttu-id="c6b96-107">Usare quindi il [compilatore MOF](mofcomp.md) per creare le versioni del file MOF indipendenti dalla lingua e dal linguaggio.</span><span class="sxs-lookup"><span data-stu-id="c6b96-107">Next, use the [MOF compiler](mofcomp.md) to create the language-neutral and language-specific versions of the MOF file.</span></span> <span data-ttu-id="c6b96-108">Il compilatore MOF inserisce la descrizione della classe di base in un nuovo file MOF e crea una versione localizzata del file MOF che contiene solo le proprietà e i qualificatori che devono essere localizzati.</span><span class="sxs-lookup"><span data-stu-id="c6b96-108">The MOF compiler places the basic class description in a new MOF file and creates a localized version of the MOF file that contains only the properties and qualifiers that must be localized.</span></span> <span data-ttu-id="c6b96-109">Sebbene le versioni specifiche del linguaggio e indipendenti dalla lingua del file MOF possano avere lo stesso nome file, è necessario utilizzare un'estensione di file. mfl per indicare che il file contiene informazioni localizzate.</span><span class="sxs-lookup"><span data-stu-id="c6b96-109">Although the language-specific and language-neutral versions of the MOF file can have the same file name, you should use a .mfl file name extension to indicate that the file contains localized information.</span></span> <span data-ttu-id="c6b96-110">Se necessario, è possibile localizzare il file con estensione mfl in altre impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="c6b96-110">You can localize the .mfl file to other locales, if necessary.</span></span> <span data-ttu-id="c6b96-111">L'archiviazione delle definizioni di classe nel repository CIM richiede un passaggio aggiuntivo di utilizzo del compilatore MOF per compilare sia i file MOF indipendenti dalla lingua che quelli specifici della lingua.</span><span class="sxs-lookup"><span data-stu-id="c6b96-111">Storing the class definitions in the CIM repository requires an additional step of using the MOF compiler to compile both the language-neutral and the language-specific MOF files.</span></span>

<span data-ttu-id="c6b96-112">Nei passaggi seguenti viene descritto come creare e archiviare una definizione di classe localizzata.</span><span class="sxs-lookup"><span data-stu-id="c6b96-112">The following steps describe how to create and store a localized class definition.</span></span>

<span data-ttu-id="c6b96-113">**Per creare e archiviare una definizione di classe localizzata**</span><span class="sxs-lookup"><span data-stu-id="c6b96-113">**To create and store a localized class definition**</span></span>

1.  <span data-ttu-id="c6b96-114">Creare il file MOF master che definisce le classi che si desidera localizzare.</span><span class="sxs-lookup"><span data-stu-id="c6b96-114">Create the master MOF file that defines the classes that you want localized.</span></span>

    <span data-ttu-id="c6b96-115">Salvare questo codice MOF in un file denominato Mastermof. mof.</span><span class="sxs-lookup"><span data-stu-id="c6b96-115">Save this MOF code in a file called Mastermof.mof.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root")

    instance of __Namespace
    {
        Name = "TEST" ;
    } ;

    #pragma namespace("\\\\.\\root\\TEST")

    [Description("Localized version of MyClass for American English") 
        : Amended, LOCALE(0x409)] 

    class myclass
    {
        [DisplayName("User Name") : Amended,
        Description("The Name property contains the name of the user") : 
        Amended, key]
         string Name;

        uint64 Value; // non-localized value field

          [DisplayName("Time Stamp") : Amended,
        Description("This property shows when the object was created") : 
        Amended] 
         uint64 Timestamp;
    };
    ```

2.  <span data-ttu-id="c6b96-116">Creare versioni indipendenti dalla lingua e dalla lingua del file MOF compilando il file MasterMOF. mof.</span><span class="sxs-lookup"><span data-stu-id="c6b96-116">Create language-neutral and language-specific versions of the MOF file by compiling the MasterMOF.mof file.</span></span>

    <span data-ttu-id="c6b96-117">Digitare il comando seguente al prompt dei comandi per compilare il file MasterMOF. mof.</span><span class="sxs-lookup"><span data-stu-id="c6b96-117">Type the following command at a command prompt to compile the MasterMOF.mof file.</span></span>

    <span data-ttu-id="c6b96-118">**mofcomp-MOF: Lnmof. mof-MFL: Lsmof. mfl-emendamento: MS \_ 409 Mastermof. mof**</span><span class="sxs-lookup"><span data-stu-id="c6b96-118">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

3.  <span data-ttu-id="c6b96-119">Compilare i file indipendenti dalla lingua (Lnmof. MOF) e specifici della lingua (Lsmof. mfl) e archiviare le informazioni sulla classe nel repository CIM.</span><span class="sxs-lookup"><span data-stu-id="c6b96-119">Compile the language-neutral (Lnmof.mof) and language-specific (Lsmof.mfl) files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="c6b96-120">Digitare i comandi seguenti al prompt dei comandi per archiviare le informazioni sulla classe nel repository CIM.</span><span class="sxs-lookup"><span data-stu-id="c6b96-120">Type the following commands at a command prompt to store the class information in the CIM repository.</span></span>

    <span data-ttu-id="c6b96-121">**Mofcomp Lnmof. mof**</span><span class="sxs-lookup"><span data-stu-id="c6b96-121">**Mofcomp Lnmof.mof**</span></span>

    <span data-ttu-id="c6b96-122">**Mofcomp Lsmof. mfl**</span><span class="sxs-lookup"><span data-stu-id="c6b96-122">**Mofcomp Lsmof.mfl**</span></span>

    <span data-ttu-id="c6b96-123">Dopo la compilazione di questi file, sarà presente una definizione di classe indipendente dal linguaggio nello \\ spazio dei nomi del test radice e una definizione di classe localizzata nello \\ \\ \_ spazio dei nomi MS 409 del test radice.</span><span class="sxs-lookup"><span data-stu-id="c6b96-123">After you compile these files, you will have a language-neutral class definition in the root\\test namespace and a localized class definition in the root\\test\\ms\_409 namespace.</span></span> <span data-ttu-id="c6b96-124">Per ulteriori informazioni sulla compilazione di file MOF localizzati, vedere [compilazione di file MOF localizzati](compiling-localized-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="c6b96-124">For more information about compiling localized MOF files, see [Compiling Localized MOF files](compiling-localized-mof-files.md).</span></span>

 

 



