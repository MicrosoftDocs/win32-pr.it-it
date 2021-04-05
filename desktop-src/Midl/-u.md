---
title: Switch/u
description: L'opzione/U rimuove tutte le definizioni precedenti di un nome passando il nome al preprocessore C come se fosse una direttiva \ undefine.
ms.assetid: 3c253fb3-9448-4b55-bfd5-852e6feec280
keywords:
- /U switch MIDL
topic_type:
- apiref
api_name:
- /U
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d018d47dd5cbcc8192dee490965bd06c56d0e3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104117041"
---
# <a name="u-switch"></a><span data-ttu-id="fefde-104">Switch/u</span><span class="sxs-lookup"><span data-stu-id="fefde-104">/U switch</span></span>

<span data-ttu-id="fefde-105">L'opzione **/u** rimuove tutte le definizioni precedenti di un nome passando il nome al preprocessore C come se fosse una direttiva **\# undefine** .</span><span class="sxs-lookup"><span data-stu-id="fefde-105">The **/U** switch removes any previous definition of a name by passing the name to the C preprocessor as if by a **\#undefine** directive.</span></span>

``` syntax
midl /U name
```

## <a name="switch-options"></a><span data-ttu-id="fefde-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="fefde-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="fefde-107">*nome*</span><span class="sxs-lookup"><span data-stu-id="fefde-107">*name*</span></span> 
</dt> <dd>

<span data-ttu-id="fefde-108">Specifica un nome definito da passare al preprocessore C come se fosse una direttiva **\# undefine** .</span><span class="sxs-lookup"><span data-stu-id="fefde-108">Specifies a defined name to be passed to the C preprocessor as if by a **\#undefine** directive.</span></span> <span data-ttu-id="fefde-109">Il nome è predefinito dal preprocessore C o definito in precedenza dall'utente.</span><span class="sxs-lookup"><span data-stu-id="fefde-109">The name is predefined by the C preprocessor or previously defined by the user.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fefde-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="fefde-110">Remarks</span></span>

<span data-ttu-id="fefde-111">In una riga di comando è possibile usare più direttive **/u** .</span><span class="sxs-lookup"><span data-stu-id="fefde-111">Multiple **/U** directives can be used in a command line.</span></span> <span data-ttu-id="fefde-112">Gli spazi vuoti tra l'opzione **/u** e il nome non definito sono facoltativi.</span><span class="sxs-lookup"><span data-stu-id="fefde-112">White space between the **/U** switch and the undefined name is optional.</span></span>

<span data-ttu-id="fefde-113">Quando è presente l'opzione [**\_ cmd/cpp**](-cpp-cmd.md) e l'opzione [**/cpp \_ opz**](-cpp-opt.md) non è, il compilatore MIDL concatena la stringa specificata dall' \_ opzione cmd di/cpp con le opzioni [**/i**](-i.md), [**/d**](-d.md)e **/u** e usa questa stringa concatenata per richiamare il preprocessore C per ogni file di origine IDL e ACF.</span><span class="sxs-lookup"><span data-stu-id="fefde-113">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the /cpp\_cmd switch with the [**/I**](-i.md), [**/D**](-d.md), and **/U** options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="fefde-114">L'opzione **/u** del compilatore MIDL viene ignorata quando si specifica l'opzione del compilatore MIDL **/No \_ cpp** o **/cpp \_ opz** .</span><span class="sxs-lookup"><span data-stu-id="fefde-114">The MIDL compiler switch **/U** is ignored when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

## <a name="examples"></a><span data-ttu-id="fefde-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="fefde-115">Examples</span></span>

<span data-ttu-id="fefde-116">**MIDL/UUNICODE nomefile. idl**</span><span class="sxs-lookup"><span data-stu-id="fefde-116">**midl /UUNICODE filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="fefde-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fefde-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fefde-118">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="fefde-118">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="fefde-119">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="fefde-119">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="fefde-120">**/cpp \_ opt**</span><span class="sxs-lookup"><span data-stu-id="fefde-120">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="fefde-121">**/D**</span><span class="sxs-lookup"><span data-stu-id="fefde-121">**/D**</span></span>](-d.md)
</dt> <dt>

[<span data-ttu-id="fefde-122">**/I**</span><span class="sxs-lookup"><span data-stu-id="fefde-122">**/I**</span></span>](-i.md)
</dt> <dt>

[<span data-ttu-id="fefde-123">**\_cpp/No**</span><span class="sxs-lookup"><span data-stu-id="fefde-123">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 




