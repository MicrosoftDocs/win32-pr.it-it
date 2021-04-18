---
title: /backward_compat opzione
description: Il \_ commutatore di compatibilità/backward indica al compilatore MIDL di disattivare alcune funzionalità avanzate quando generano stub RPC/com.
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b558d01b33b99f7d1d9279f729b923ff58df0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297965"
---
# <a name="backward_compat-switch"></a><span data-ttu-id="be070-103">\_opzione/backward compat</span><span class="sxs-lookup"><span data-stu-id="be070-103">/backward\_compat Switch</span></span>

<span data-ttu-id="be070-104">Il \_ commutatore di compatibilità/backward indica al compilatore MIDL di disattivare alcune funzionalità avanzate quando generano stub RPC/com.</span><span class="sxs-lookup"><span data-stu-id="be070-104">The /backward\_compat switch directs the MIDL compiler to turn off some advanced features when generating RPC/COM stubs.</span></span>

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a><span data-ttu-id="be070-105">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="be070-105">Switch Options</span></span>

<span data-ttu-id="be070-106">*\_dimensioni MAYBENULL*</span><span class="sxs-lookup"><span data-stu-id="be070-106">*maybenull\_sizeis*</span></span><dl> <span data-ttu-id="be070-107">Applica l'attributo [ \[ Disable \_ \_ verifica \] coerenza](disable-consistence-check.md) a un'intera compilazione MIDL.</span><span class="sxs-lookup"><span data-stu-id="be070-107">Applies the [\[disable\_consistency\_check\]](disable-consistence-check.md) attribute to an entire MIDL compilation.</span></span>  
</dl>

<span data-ttu-id="be070-108">*azzeramento \_ alignmentgap*</span><span class="sxs-lookup"><span data-stu-id="be070-108">*zeroout\_alignmentgap*</span></span><dl> <span data-ttu-id="be070-109">Disattiva lo zero dei gap nel buffer sottoposto a marshalling.</span><span class="sxs-lookup"><span data-stu-id="be070-109">Turns off zeroing out gaps in the marshaled buffer.</span></span>  
</dl>

<span data-ttu-id="be070-110">*\_Escape BSTR byValue \_*</span><span class="sxs-lookup"><span data-stu-id="be070-110">*BSTR\_byvalue\_escaping*</span></span><dl> <span data-ttu-id="be070-111">Indica al compilatore MIDL di rispettare le sequenze di escape, ad esempio â € ̃ \\ nâ™ o â € ̃ \\ tâ €™ in BSTRS.</span><span class="sxs-lookup"><span data-stu-id="be070-111">Directs the MIDL compiler to honor escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in BSTRs.</span></span>  
</dl>

<span data-ttu-id="be070-112">*stringa \_ DefaultValue*</span><span class="sxs-lookup"><span data-stu-id="be070-112">*string\_defaultvalue*</span></span><dl> <span data-ttu-id="be070-113">Impone al compilatore MIDL di forzare le stringhe negli attributi [**\[ DEFAULTVALUE \]**](defaultvalue.md) in Variant. Tipo di VT \_ I4 prima di assegnare il valore al tipo corretto.</span><span class="sxs-lookup"><span data-stu-id="be070-113">Forces the MIDL compiler to coerce strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span>  
</dl>

<span data-ttu-id="be070-114">*\_WCHAR \_ t firmato*</span><span class="sxs-lookup"><span data-stu-id="be070-114">*signed\_wchar\_t*</span></span><dl> <span data-ttu-id="be070-115">Indica a MIDL di considerare il \_ Tipo wchar t come firmato per la compatibilità con Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="be070-115">Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>  
</dl>

## <a name="remarks"></a><span data-ttu-id="be070-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="be070-116">Remarks</span></span>

-   <span data-ttu-id="be070-117">*\_ dimensioni MAYBENULL*: vedere \[ disabilitare la \_ Verifica della coerenza \_ \] .</span><span class="sxs-lookup"><span data-stu-id="be070-117">*maybenull\_sizeis*: See \[disable\_consistency\_check\].</span></span>
-   <span data-ttu-id="be070-118">*azzeramento \_ alignmentgap*: quando IDLs vengono compilati con la destinazione nt60 o una versione successiva, MIDL creerà gli stub che azzerano i gap di allineamento tra i membri o una struttura nel buffer di transito.</span><span class="sxs-lookup"><span data-stu-id="be070-118">*zeroout\_alignmentgap*: When IDLs are compiled with â€“target NT60 or higher, MIDL will create stubs that zero out any alignment gaps between members or a structure in the wire buffer.</span></span> <span data-ttu-id="be070-119">L'opzione della riga di comando */Backward \_ compat zero \_ alignmentgap* indirizza MIDL per disabilitare questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="be070-119">The command line switch */backward\_compat zeroout\_alignmentgap* directs MIDL to disable this feature.</span></span>

    <span data-ttu-id="be070-120">Nella struttura di esempio seguente, il buffer di trasmissione contiene un gap di allineamento a 7 byte per allineare il membro Hyper a 8 dopo il membro Char.</span><span class="sxs-lookup"><span data-stu-id="be070-120">In the following example structure, the wire buffer contains a 7 byte alignment gap to align the hyper member to 8 after the char member.</span></span> <span data-ttu-id="be070-121">Con la destinazione NT60 o versione successiva, MIDL Azzera tale gap a meno che non venga usata l'opzione.</span><span class="sxs-lookup"><span data-stu-id="be070-121">With â€“target NT60 or higher, MIDL will zero out that gap unless the switch is used.</span></span>

    <span data-ttu-id="be070-122">File IDL:</span><span class="sxs-lookup"><span data-stu-id="be070-122">IDL file:</span></span>

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    <span data-ttu-id="be070-123">Questa opzione può offrire un lieve miglioramento delle prestazioni con un aumento potenzialmente significativo del rischio di divulgazione.</span><span class="sxs-lookup"><span data-stu-id="be070-123">This switch can provide a slight performance improvement with potentially significant increases in disclosure risk.</span></span>

-   <span data-ttu-id="be070-124">*\_ \_ Escape di BSTR byValue*: per impostazione predefinita, il compilatore MIDL non elabora sequenze di escape, ad esempio â € ̃ \\ NÂ™ o â € ̃ \\ tâ €™ nelle costanti di stringa per l'automazione OLE durante la conversione di una costante di stringa nei tipi VT \_ LPSTR o VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="be070-124">*BSTR\_byvalue\_escaping*: By default, the MIDL compiler does not process escape sequences such as â€˜\\nâ€™ or â€˜\\tâ€™ in string constants for OLE Automation when converting a string constant to types VT\_LPSTR or VT\_LPWSTR.</span></span> <span data-ttu-id="be070-125">Con questa opzione per la compatibilità con le versioni precedenti, vengono valutate le sequenze di escape.</span><span class="sxs-lookup"><span data-stu-id="be070-125">With this backward compatibility switch option, the escape sequences are evaluated.</span></span>
-   <span data-ttu-id="be070-126">*String \_ DefaultValue*: impone al compilatore MIDL di assegnare le stringhe numeriche negli attributi [**\[ \] DefaultValue**](defaultvalue.md) a Variant. Tipo di VT \_ I4 prima di assegnare il valore al tipo corretto.</span><span class="sxs-lookup"><span data-stu-id="be070-126">*string\_defaultvalue*: Forces the MIDL compiler to coerce numeric strings in [**\[defaultvalue\]**](defaultvalue.md) attributes into VARIANT.VT\_I4 type before coercing the value into the correct type.</span></span> <span data-ttu-id="be070-127">Questo può causare una perdita di precisione in alcuni casi, pertanto questa opzione non è consigliata.</span><span class="sxs-lookup"><span data-stu-id="be070-127">This can lead to loss of precision in some cases, so this switch option is not recommended.</span></span>
-   <span data-ttu-id="be070-128">con *segno \_ WCHAR \_ t*: indica a MIDL di considerare il \_ Tipo wchar t come firmato per la compatibilità con Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="be070-128">*signed\_wchar\_t*: Directs MIDL to treat the wchar\_t type as signed for compatibility with Visual Basic.</span></span>

 

 




