---
title: opzione/ACF
description: L'opzione/ACF consente all'utente di specificare un nome di file ACF esplicito. L'opzione consente inoltre l'utilizzo di nomi di interfaccia diversi nei file IDL e ACF.
ms.assetid: 8f0833ec-1dbc-4c8a-af7e-3de42169af8d
keywords:
- /ACF switch MIDL
topic_type:
- apiref
api_name:
- /acf
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e24d66982628fbd0052e8a3f573901c430e8b8b1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103955995"
---
# <a name="acf-switch"></a><span data-ttu-id="6ed81-105">opzione/ACF</span><span class="sxs-lookup"><span data-stu-id="6ed81-105">/acf switch</span></span>

<span data-ttu-id="6ed81-106">L'opzione **/ACF** consente all'utente di specificare un nome di file ACF esplicito.</span><span class="sxs-lookup"><span data-stu-id="6ed81-106">The **/acf** switch allows the user to supply an explicit ACF file name.</span></span> <span data-ttu-id="6ed81-107">L'opzione consente inoltre l'utilizzo di nomi di interfaccia diversi nei file IDL e ACF.</span><span class="sxs-lookup"><span data-stu-id="6ed81-107">The switch also allows the use of different interface names in the IDL and ACF files.</span></span>

``` syntax
midl /acf acf_filename
```

## <a name="switch-options"></a><span data-ttu-id="6ed81-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="6ed81-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="6ed81-109">*\_nome file ACF*</span><span class="sxs-lookup"><span data-stu-id="6ed81-109">*acf\_filename*</span></span> 
</dt> <dd>

<span data-ttu-id="6ed81-110">Specifica il nome dell'oggetto ACF.</span><span class="sxs-lookup"><span data-stu-id="6ed81-110">Specifies the name of the ACF.</span></span> <span data-ttu-id="6ed81-111">Gli spazi vuoti possono essere presenti tra l'opzione **/ACF** e il nome file.</span><span class="sxs-lookup"><span data-stu-id="6ed81-111">White space may or may not be present between the **/acf** switch and the file name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ed81-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ed81-112">Remarks</span></span>

<span data-ttu-id="6ed81-113">Per impostazione predefinita, il compilatore MIDL costruisce il nome dell'ACF sostituendo l'estensione del nome file IDL (in genere IDL) con. ACF.</span><span class="sxs-lookup"><span data-stu-id="6ed81-113">By default, the MIDL compiler constructs the name of the ACF by replacing the IDL file name extension (usually .idl) with .acf.</span></span> <span data-ttu-id="6ed81-114">Quando l'opzione **/ACF** è presente, l'ACF prende il nome dal nome file specificato.</span><span class="sxs-lookup"><span data-stu-id="6ed81-114">When the **/acf** switch is present, the ACF takes its name from the specified file name.</span></span> <span data-ttu-id="6ed81-115">L'opzione **/ACF** si applica solo al file idl specificato nella riga di comando del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="6ed81-115">The **/acf** switch applies only to the IDL file specified on the MIDL compiler command line.</span></span> <span data-ttu-id="6ed81-116">Non si applica ai file importati.</span><span class="sxs-lookup"><span data-stu-id="6ed81-116">It does not apply to imported files.</span></span>

<span data-ttu-id="6ed81-117">Quando si usa l'opzione **/ACF** , il nome dell'interfaccia in ACF non deve corrispondere al nome dell'interfaccia MIDL.</span><span class="sxs-lookup"><span data-stu-id="6ed81-117">When the **/acf** switch is used, the interface name in the ACF need not match the MIDL interface name.</span></span> <span data-ttu-id="6ed81-118">Questa funzionalità consente alle interfacce di condividere una specifica ACF.</span><span class="sxs-lookup"><span data-stu-id="6ed81-118">This feature allows interfaces to share an ACF specification.</span></span>

<span data-ttu-id="6ed81-119">Quando non viene specificato un percorso assoluto di un ACF, il compilatore MIDL Cerca nella directory corrente le directory fornite dall'opzione [**/i**](-i.md) e le directory nel percorso di inclusione.</span><span class="sxs-lookup"><span data-stu-id="6ed81-119">When an absolute path to an ACF is not specified, the MIDL compiler searches in the current directory, directories supplied by the [**/I**](-i.md) option, and directories in the INCLUDE path.</span></span>

<span data-ttu-id="6ed81-120">Se l'ACF non viene trovato, il compilatore MIDL presuppone che non esista alcun ACF per questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6ed81-120">If the ACF is not found, the MIDL compiler assumes there is no ACF for this interface.</span></span> <span data-ttu-id="6ed81-121">Per ulteriori informazioni sulla sequenza di directory, vedere le voci di riferimento per le opzioni [**/i**](-i.md) e [**/No \_ def \_ Idir**](-no-def-idir.md) .</span><span class="sxs-lookup"><span data-stu-id="6ed81-121">For more information about the sequence of directories, see the reference entries for the [**/I**](-i.md) and [**/no\_def\_idir**](-no-def-idir.md) switches.</span></span> <span data-ttu-id="6ed81-122">Per ulteriori informazioni relative a **/ACF**, vedere [file di definizione dell'interfaccia (IDL)](interface-definition-idl-file.md).</span><span class="sxs-lookup"><span data-stu-id="6ed81-122">For more information relating to **/acf**, see [Interface Definition (IDL) File](interface-definition-idl-file.md).</span></span>

## <a name="examples"></a><span data-ttu-id="6ed81-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="6ed81-123">Examples</span></span>

<span data-ttu-id="6ed81-124">**MIDL/ACF bar. ACF nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="6ed81-124">**midl /acf bar.acf filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="6ed81-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ed81-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ed81-126">**/I**</span><span class="sxs-lookup"><span data-stu-id="6ed81-126">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="6ed81-127">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="6ed81-127">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="6ed81-128">**/No \_ def \_ Idir**</span><span class="sxs-lookup"><span data-stu-id="6ed81-128">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 




