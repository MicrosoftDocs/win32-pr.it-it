---
title: /D (opzione)
description: L'opzione/D definisce un nome e un valore facoltativo da passare al preprocessore C come se fosse una direttiva \ define. In una riga di comando è possibile usare più direttive/D.
ms.assetid: 65642bf6-8e25-400b-8b1c-43513ab6b313
keywords:
- /D opzione MIDL
topic_type:
- apiref
api_name:
- /D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d51cdcbecb5386acb1a97d933be8b25f68720ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104117088"
---
# <a name="d-switch"></a><span data-ttu-id="6e3d0-105">/D (opzione)</span><span class="sxs-lookup"><span data-stu-id="6e3d0-105">/D switch</span></span>

<span data-ttu-id="6e3d0-106">L'opzione **/d** definisce un nome e un valore facoltativo da passare al preprocessore C come se fosse una direttiva **\# define** .</span><span class="sxs-lookup"><span data-stu-id="6e3d0-106">The **/D** switch defines a name and an optional value to be passed to the C preprocessor as if by a **\#define** directive.</span></span> <span data-ttu-id="6e3d0-107">In una riga di comando è possibile usare più direttive **/d** .</span><span class="sxs-lookup"><span data-stu-id="6e3d0-107">Multiple **/D** directives can be used in a command line.</span></span>

``` syntax
midl /Dname[=definition]
```

## <a name="switch-options"></a><span data-ttu-id="6e3d0-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="6e3d0-108">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="6e3d0-109">*nome*</span><span class="sxs-lookup"><span data-stu-id="6e3d0-109">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="6e3d0-110">Specifica un nome definito che viene passato al preprocessore C quando è presente l'opzione [**\_ cmd/cpp**](-cpp-cmd.md) e l'opzione [**/cpp \_ opt**](-cpp-opt.md) non è presente.</span><span class="sxs-lookup"><span data-stu-id="6e3d0-110">Specifies a defined name that is passed to the C preprocessor when the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not present.</span></span>

</dd> <dt>

<span data-ttu-id="6e3d0-111">*definizione*</span><span class="sxs-lookup"><span data-stu-id="6e3d0-111">*definition*</span></span> 
</dt> <dd>

<span data-ttu-id="6e3d0-112">Specifica un valore associato al nome definito.</span><span class="sxs-lookup"><span data-stu-id="6e3d0-112">Specifies a value associated with the defined name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6e3d0-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e3d0-113">Remarks</span></span>

<span data-ttu-id="6e3d0-114">Gli spazi vuoti tra l'opzione **/d** e il nome definito sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="6e3d0-114">White space between the **/D** switch and the defined name is optional.</span></span>

<span data-ttu-id="6e3d0-115">Quando è presente l'opzione [**\_ cmd/cpp**](-cpp-cmd.md) e l' [**opzione \_ /cpp opz**](-cpp-opt.md) non è, il compilatore MIDL concatena la stringa specificata dall'opzione **\_ cmd di/cpp** con le opzioni [**/i**](-i.md), **/d** e [**/U**](-u.md) e usa questa stringa concatenata per richiamare il preprocessore C per ogni file di origine IDL e ACF.</span><span class="sxs-lookup"><span data-stu-id="6e3d0-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the [**/I**](-i.md), **/D**, and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span>

<span data-ttu-id="6e3d0-116">L'opzione del compilatore MIDL **/d** viene ignorata quando si specifica l'opzione del compilatore MIDL [/No \_ cpp](-no-cpp-nocpp.md) o [**/cpp \_ opz**](-cpp-opt.md) .</span><span class="sxs-lookup"><span data-stu-id="6e3d0-116">The MIDL compiler switch **/D** is ignored when the MIDL compiler switch [/no\_cpp](-no-cpp-nocpp.md) or [**/cpp\_opt**](-cpp-opt.md) is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="6e3d0-117">Esempio</span><span class="sxs-lookup"><span data-stu-id="6e3d0-117">Examples</span></span>

<span data-ttu-id="6e3d0-118">**MIDL-DUNICODE nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="6e3d0-118">**midl -DUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="6e3d0-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e3d0-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e3d0-120">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="6e3d0-120">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="6e3d0-121">**/cpp \_ opt**</span><span class="sxs-lookup"><span data-stu-id="6e3d0-121">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="6e3d0-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="6e3d0-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="6e3d0-123">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="6e3d0-123">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="6e3d0-124">**\_cpp/No**</span><span class="sxs-lookup"><span data-stu-id="6e3d0-124">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="6e3d0-125">**/U**</span><span class="sxs-lookup"><span data-stu-id="6e3d0-125">**/U**</span></span>](-u.md)
</dt> </dl>

 

 




