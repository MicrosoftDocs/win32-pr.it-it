---
description: È necessario compilare il file MOF master per creare i file MOF indipendenti dalla lingua e dal linguaggio.
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: Compilazione di file MOF localizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ab1341a37269ba98fdbbdecaa64b5e5a119703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346766"
---
# <a name="compiling-localized-mof-files"></a><span data-ttu-id="df8e1-103">Compilazione di file MOF localizzati</span><span class="sxs-lookup"><span data-stu-id="df8e1-103">Compiling Localized MOF Files</span></span>

<span data-ttu-id="df8e1-104">È necessario compilare il file MOF master per creare i file MOF indipendenti dalla lingua e dal linguaggio.</span><span class="sxs-lookup"><span data-stu-id="df8e1-104">You must compile your master MOF file to create the language-neutral and language-specific MOF files.</span></span>

<span data-ttu-id="df8e1-105">Digitare il comando seguente al prompt dei comandi per compilare un file MOF master.</span><span class="sxs-lookup"><span data-stu-id="df8e1-105">Type the following command at a command prompt to compile a master MOF file.</span></span>

<span data-ttu-id="df8e1-106">**mofcomp-MOF: Lnmof. mof-MFL: Lsmof. mfl-emendamento: MS \_ 409 Mastermof. mof**</span><span class="sxs-lookup"><span data-stu-id="df8e1-106">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

<span data-ttu-id="df8e1-107">Quando si esegue questo comando, il compilatore MOF crea due file MOF dal file Mastermof. mof originale.</span><span class="sxs-lookup"><span data-stu-id="df8e1-107">When you run this command, the MOF compiler creates two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="df8e1-108">Il compilatore MOF produce una versione indipendente dalla lingua, Lnmof. mof, in cui vengono rimossi tutti gli elementi specifici della lingua.</span><span class="sxs-lookup"><span data-stu-id="df8e1-108">The MOF compiler produces a language-neutral version, Lnmof.mof, in which all language-specific items are removed.</span></span> <span data-ttu-id="df8e1-109">Viene creata anche una seconda versione specifica del linguaggio, Lsmof. mof. Questo file contiene solo gli elementi contrassegnati con la versione del qualificatore [**modificata**](qualifier-flavors.md) nel file Mastermof. mof.</span><span class="sxs-lookup"><span data-stu-id="df8e1-109">A second, language-specific version, Lsmof.mof, is also created; this file contains only items that were marked with the [**Amended**](qualifier-flavors.md) Qualifier Flavor in the Mastermof.mof file.</span></span>

<span data-ttu-id="df8e1-110">Nell'esempio di codice seguente viene illustrato il contenuto del file MOF indipendente dalla lingua (Lnmof. MOF) generato.</span><span class="sxs-lookup"><span data-stu-id="df8e1-110">The following code example shows the contents of the language-neutral MOF file (Lnmof.mof) that is generated.</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

Instance of __Namespace
{
  Name = "TEST";
};
#pragma namespace("\\\\.\\root\\TEST")

[LOCALE(1033)] 
class myclass
{
  [key] string Name;
  uint64 Value;
  uint64 Timestamp;
};
```

<span data-ttu-id="df8e1-111">Nell'esempio di codice seguente viene illustrato il contenuto del file MOF specifico del linguaggio (Lsmof. mfl) generato.</span><span class="sxs-lookup"><span data-stu-id="df8e1-111">The following code example shows the contents of the language-specific MOF file (Lsmof.mfl) that is generated.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\TEST")
instance of __namespace{ name="ms_409";};
#pragma namespace("\\\\.\\root\\TEST\\ms_409")

[Description("Localized version of MyClass for American English") :
    Amended, LOCALE(0x409)] 

class myclass
{
    [DisplayName("User Name") : Amended,
    Description("The Name property contains the name of the user") : 
    Amended, key]
     string Name;

    [DisplayName("Time Stamp") : Amended,
    Description("This property shows when the object was created") : 
    Amended] 
     uint64 Timestamp;
};
```

<span data-ttu-id="df8e1-112">La compilazione di un file MOF con il qualificatore [**modificato**](qualifier-flavors.md) genera solo file MOF indipendenti dalla lingua e dalla lingua specifici; il repository CIM non viene aggiornato con le informazioni sulla nuova classe.</span><span class="sxs-lookup"><span data-stu-id="df8e1-112">Compiling a MOF file with the [**Amended**](qualifier-flavors.md) qualifier only generates separate language-neutral and language-specific MOF files; the CIM repository is not updated with the new class information.</span></span> <span data-ttu-id="df8e1-113">È necessario utilizzare il compilatore MOF per compilare i due file MOF creati dalla prima compilazione prima che tutte le informazioni sulle classi siano disponibili per WMI.</span><span class="sxs-lookup"><span data-stu-id="df8e1-113">You must use the MOF compiler to compile the two MOF files that the first compilation produced before any class information is available to WMI.</span></span>

<span data-ttu-id="df8e1-114">Quando si compila un file MOF Master, solo i qualificatori con la [**versione modificata**](qualifier-flavors.md) vengono spostati nel file MOF specifico della lingua.</span><span class="sxs-lookup"><span data-stu-id="df8e1-114">When you compile a master MOF file, only qualifiers with the [**Amended**](qualifier-flavors.md) flavor are moved to the language-specific MOF file.</span></span> <span data-ttu-id="df8e1-115">I qualificatori che non dispongono della **versione modificata** non sono localizzati e sono presenti solo nella definizione della classe di base nel file MOF indipendente dalla lingua.</span><span class="sxs-lookup"><span data-stu-id="df8e1-115">Qualifiers that do not have the **Amended** flavor are not localized and only exist in the basic class definition in the language-neutral MOF file.</span></span> <span data-ttu-id="df8e1-116">Se non sono disponibili descrizioni localizzate, è possibile usare i qualificatori non localizzati per le descrizioni predefinite.</span><span class="sxs-lookup"><span data-stu-id="df8e1-116">Nonlocalized qualifiers can be used for default descriptions if localized descriptions are not available.</span></span>

<span data-ttu-id="df8e1-117">È possibile usare il comando [pragma emendation](pragma-amendment.md) anziché specificare [**emendato**](qualifier-flavors.md) come passaggio al compilatore MOF.</span><span class="sxs-lookup"><span data-stu-id="df8e1-117">You can use the [pragma amendment](pragma-amendment.md) command instead of specifying [**Amended**](qualifier-flavors.md) as a switch to the MOF compiler.</span></span> <span data-ttu-id="df8e1-118">Una di queste opzioni equivale a richiedere versioni specifiche della lingua e indipendenti dalla lingua di un file MOF.</span><span class="sxs-lookup"><span data-stu-id="df8e1-118">Either of these options are equivalent to requesting language-specific and language-neutral versions of a MOF file.</span></span> <span data-ttu-id="df8e1-119">Se si usa il comando di modifica pragma o l'opzione della riga di comando **modificata** , è necessario specificare il nome dei file di output usando le opzioni **-MFL** e **-MOF** al prompt dei comandi.</span><span class="sxs-lookup"><span data-stu-id="df8e1-119">If you use either the pragma amendment command or the **Amended** command-line option, you must specify the name of the output files using the **-MFL** and **-MOF** options at the command prompt.</span></span>

> [!Note]  
> <span data-ttu-id="df8e1-120">Il file MOF indipendente dalla lingua generato dal compilatore MOF contiene l'equivalente decimale dell'ID delle impostazioni locali, anche se questo valore è stato immesso in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="df8e1-120">The language-neutral MOF file that the MOF compiler generates contains the decimal equivalent of the locale ID, even if this value was entered in hexadecimal.</span></span> <span data-ttu-id="df8e1-121">Nell'esempio precedente il compilatore ha convertito il valore 0x409 nel numero decimale 1033 per il file di output Lnmof. mof.</span><span class="sxs-lookup"><span data-stu-id="df8e1-121">In the example above, the compiler has converted the value 0x409 to the decimal number 1033 for the Lnmof.mof output file.</span></span>

 

 

 



