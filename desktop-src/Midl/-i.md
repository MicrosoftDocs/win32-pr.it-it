---
title: Opzione/i
description: L'opzione/I specifica le directory in cui ricercare i file IDL importati, i file di intestazione inclusi e i file ACF.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- /I switch MIDL
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ee48ad1e66caf5ed8facbf09ebf2c517c8c895
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045836"
---
# <a name="i-switch"></a><span data-ttu-id="74a4c-104">Opzione/i</span><span class="sxs-lookup"><span data-stu-id="74a4c-104">/I switch</span></span>

<span data-ttu-id="74a4c-105">L'opzione **/i** specifica le directory in cui ricercare i file IDL importati, i file di intestazione inclusi e i file ACF.</span><span class="sxs-lookup"><span data-stu-id="74a4c-105">The **/I** switch specifies directories to be searched for imported IDL files, included header files, and ACF files.</span></span>

``` syntax
midl /I include_path
```

## <a name="switch-options"></a><span data-ttu-id="74a4c-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="74a4c-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="74a4c-107">*Includi \_ percorso*</span><span class="sxs-lookup"><span data-stu-id="74a4c-107">*include\_path*</span></span> 
</dt> <dd>

<span data-ttu-id="74a4c-108">Specifica una o più directory che contengono file di importazione, inclusione e ACF.</span><span class="sxs-lookup"><span data-stu-id="74a4c-108">Specifies one or more directories that contain import, include, and ACF files.</span></span> <span data-ttu-id="74a4c-109">Gli spazi vuoti tra l'opzione **/i** e il *\_ percorso di inclusione* sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="74a4c-109">White space between the **/I** switch and *include\_path* is optional.</span></span> <span data-ttu-id="74a4c-110">Separare più directory con un carattere punto e virgola (;).</span><span class="sxs-lookup"><span data-stu-id="74a4c-110">Separate multiple directories with a semicolon character (;).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="74a4c-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="74a4c-111">Remarks</span></span>

<span data-ttu-id="74a4c-112">È possibile visualizzare più directory con ogni opzione **/i** e più di un'opzione **/i** può comparire con ogni chiamata del compilatore MIDL.</span><span class="sxs-lookup"><span data-stu-id="74a4c-112">More than one directory can appear with each **/I** switch, and more than one **/I** switch can appear with each MIDL compiler invocation.</span></span> <span data-ttu-id="74a4c-113">Viene eseguita la ricerca nelle directory nell'ordine in cui sono specificate.</span><span class="sxs-lookup"><span data-stu-id="74a4c-113">Directories are searched in the order they are specified.</span></span>

<span data-ttu-id="74a4c-114">L'impostazione dell'opzione **/i** viene passata anche dal compilatore MIDL al preprocessore c del compilatore c.</span><span class="sxs-lookup"><span data-stu-id="74a4c-114">The **/I** switch setting is also passed by the MIDL compiler to the C compiler's C preprocessor.</span></span> <span data-ttu-id="74a4c-115">Quando è presente l'opzione [**\_ cmd/cpp**](-cpp-cmd.md) e l' [**opzione \_ /cpp opz**](-cpp-opt.md) non è, il compilatore MIDL concatena la stringa specificata dall'opzione **\_ cmd di/cpp** con le opzioni **/i**, [**/d**](-d.md)e [**/U**](-u.md) e usa questa stringa concatenata per richiamare il preprocessore C per ogni file di origine IDL e ACF.</span><span class="sxs-lookup"><span data-stu-id="74a4c-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the **/I**, [**/D**](-d.md), and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="74a4c-116">L'opzione del compilatore MIDL **/i** non viene passata al preprocessore quando si specifica l'opzione del compilatore MIDL **/No \_ cpp** o **/cpp \_ opz** .</span><span class="sxs-lookup"><span data-stu-id="74a4c-116">The MIDL compiler switch **/I** is not passed to the preprocessor when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

<span data-ttu-id="74a4c-117">Negli ambienti del sistema operativo Microsoft (Windows a 64 bit, Windows a 32 bit, Windows a 16 bit e MS-DOS), le directory vengono ricercate nella sequenza seguente:</span><span class="sxs-lookup"><span data-stu-id="74a4c-117">In Microsoft operating-system environments (64-bit Windows, 32-bit Windows, 16-bit Windows, and MS-DOS), directories are searched in the following sequence:</span></span>

1.  <span data-ttu-id="74a4c-118">La directory corrente</span><span class="sxs-lookup"><span data-stu-id="74a4c-118">Current directory</span></span>
2.  <span data-ttu-id="74a4c-119">Directory specificate dall'opzione **/i** (nell'ordine in cui seguono l'opzione)</span><span class="sxs-lookup"><span data-stu-id="74a4c-119">Directories specified by the **/I** switch (in the order they follow the switch)</span></span>
3.  <span data-ttu-id="74a4c-120">Directory specificate dalla variabile di ambiente INCLUDE</span><span class="sxs-lookup"><span data-stu-id="74a4c-120">Directories specified by the INCLUDE environment variable</span></span>

<span data-ttu-id="74a4c-121">Quando si specificano le directory con l'opzione **/i** , l'opzione [**/No \_ def \_ Idir**](-no-def-idir.md) indica al compilatore MIDL di ignorare la directory corrente, ignorare le directory specificate dalla variabile di ambiente include e cercare solo le directory specificate.</span><span class="sxs-lookup"><span data-stu-id="74a4c-121">When directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to ignore the current directory, ignore the directories specified by the INCLUDE environment variable, and search only the specified directories.</span></span>

<span data-ttu-id="74a4c-122">Quando non viene specificata alcuna directory con l'opzione **/i** , l'opzione [**/No \_ def \_ Idir**](-no-def-idir.md) indica al compilatore MIDL di eseguire la ricerca solo nella directory corrente.</span><span class="sxs-lookup"><span data-stu-id="74a4c-122">When no directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="74a4c-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="74a4c-123">Examples</span></span>

<span data-ttu-id="74a4c-124">**MIDL/I c: \\ include; c: \\ Includi \\ h/i \\ INCLUDE2 nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="74a4c-124">**midl /I c:\\include;c:\\include\\h /I\\include2 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="74a4c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74a4c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74a4c-126">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="74a4c-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="74a4c-127">**/acf**</span><span class="sxs-lookup"><span data-stu-id="74a4c-127">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="74a4c-128">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="74a4c-128">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="74a4c-129">**/cpp \_ opt**</span><span class="sxs-lookup"><span data-stu-id="74a4c-129">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="74a4c-130">**/No \_ def \_ Idir**</span><span class="sxs-lookup"><span data-stu-id="74a4c-130">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 




