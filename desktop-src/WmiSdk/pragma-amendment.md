---
description: Indica al compilatore MOF di separare un file MOF in versioni indipendenti dalla lingua e dal linguaggio.
ms.assetid: c1aec33c-b936-4cca-8fcd-7bd088af7116
ms.tgt_platform: multiple
title: modifica pragma
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pragma
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1269ac1a96617b72852e687b2a38ce8d331ab3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753698"
---
# <a name="pragma-amendment"></a><span data-ttu-id="91f7e-103">modifica pragma</span><span class="sxs-lookup"><span data-stu-id="91f7e-103">pragma amendment</span></span>

<span data-ttu-id="91f7e-104">Il comando per il preprocessore **pragma emendamento** indica al compilatore MOF di separare un file MOF in versioni indipendenti dalla lingua e dal linguaggio.</span><span class="sxs-lookup"><span data-stu-id="91f7e-104">The **pragma amendment** preprocessor command directs the MOF compiler to separate a MOF file into language-neutral and language-specific versions.</span></span> <span data-ttu-id="91f7e-105">Il file MOF specifico del linguaggio sposta i qualificatori modificati in uno spazio dei nomi per le impostazioni locali specifiche.</span><span class="sxs-lookup"><span data-stu-id="91f7e-105">The language-specific MOF file moves amended qualifiers to a namespace for a specific locale.</span></span> <span data-ttu-id="91f7e-106">Compilare quindi i file MOF specifici della lingua e della lingua per archiviare le informazioni sulle classi nel repository WMI.</span><span class="sxs-lookup"><span data-stu-id="91f7e-106">You then compile the language-specific and language-neutral MOF files to store class information in the WMI repository.</span></span>

## <a name="examples"></a><span data-ttu-id="91f7e-107">Esempio</span><span class="sxs-lookup"><span data-stu-id="91f7e-107">Examples</span></span>

<span data-ttu-id="91f7e-108">Nell'esempio seguente viene illustrato come creare un file MOF che contiene qualificatori modificati.</span><span class="sxs-lookup"><span data-stu-id="91f7e-108">The following example shows how to create a MOF file that contains amended qualifiers.</span></span> <span data-ttu-id="91f7e-109">È quindi possibile compilare il codice MOF con il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="91f7e-109">You can then compile the MOF code with the following command:</span></span>

<span data-ttu-id="91f7e-110">**mofcomp** **-MOF: Lnmof. mof** **-MFL: Lsmof. mfl** **Mastermof. mof**</span><span class="sxs-lookup"><span data-stu-id="91f7e-110">**mofcomp** **-MOF:Lnmof.mof** **-MFL:Lsmof.mfl** **Mastermof.mof**</span></span>

<span data-ttu-id="91f7e-111">Il comando indica al compilatore MOF di produrre due file MOF dal file Mastermof. mof originale.</span><span class="sxs-lookup"><span data-stu-id="91f7e-111">The command instructs the MOF compiler to produce two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="91f7e-112">Il compilatore MOF produce una versione indipendente dal linguaggio del file MOF, denominata Lnmof. mof, con tutti gli elementi specifici della lingua rimossi.</span><span class="sxs-lookup"><span data-stu-id="91f7e-112">The MOF compiler produces a language-neutral version of the MOF file, called Lnmof.mof, with all language-specific items removed.</span></span> <span data-ttu-id="91f7e-113">Il compilatore crea anche un secondo file MOF specifico del linguaggio denominato Lsmof. mfl che contiene solo gli elementi che è necessario localizzare.</span><span class="sxs-lookup"><span data-stu-id="91f7e-113">The compiler also creates a second, language-specific MOF file called Lsmof.mfl that contains only items that you must localize.</span></span>

> [!Note]  
> <span data-ttu-id="91f7e-114">Quando si suddivide un file MOF con il qualificatore della **modifica** o il comando **pragma emendation** , è necessario specificare le opzioni **-MOF** e **-MFL** .</span><span class="sxs-lookup"><span data-stu-id="91f7e-114">When you are splitting a MOF file with the **amendment** qualifier or the **pragma amendment** command, you must specify the **-MOF** and **-MFL** options.</span></span> <span data-ttu-id="91f7e-115">In caso contrario, il compilatore non genera alcun file di output.</span><span class="sxs-lookup"><span data-stu-id="91f7e-115">Otherwise, the compiler does not generate any output files.</span></span> <span data-ttu-id="91f7e-116">È quindi necessario compilare i due file di output per rendere disponibili le informazioni sulla classe per WMI.</span><span class="sxs-lookup"><span data-stu-id="91f7e-116">You must then compile the two output files to make the class information available to WMI.</span></span>

 


```mof
#pragma amendment ("MS_409")

[Description("Localized version of MyClass" for American English") :
    Amended, LOCALE(0x409)] 

Class myclass
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



## <a name="requirements"></a><span data-ttu-id="91f7e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="91f7e-117">Requirements</span></span>



| <span data-ttu-id="91f7e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="91f7e-118">Requirement</span></span> | <span data-ttu-id="91f7e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="91f7e-119">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="91f7e-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91f7e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="91f7e-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="91f7e-121">Windows Vista</span></span><br/>       |
| <span data-ttu-id="91f7e-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="91f7e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="91f7e-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="91f7e-123">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="91f7e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="91f7e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91f7e-125">Comandi del preprocessore</span><span class="sxs-lookup"><span data-stu-id="91f7e-125">Preprocessor Commands</span></span>](preprocessor-commands.md)
</dt> </dl>

 

 




