---
title: /no_robust opzione
description: Il com/notore \_ affidabile indica al compilatore MIDL di disabilitare in modo esplicito la funzionalità della riga di comando di/robust. L'opzione della riga di comando/robust e le funzionalità associate sono le impostazioni predefinite del compilatore per MIDL Version 6.0.359 e versioni successive.
ms.assetid: 17ece05a-d39d-4465-8553-199a45c8c073
keywords:
- /no_robust switch MIDL
topic_type:
- apiref
api_name:
- /no_robust
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90691aede68f8e43ae95a4bd6c6f7fb4e2ecad29
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718772"
---
# <a name="no_robust-switch"></a><span data-ttu-id="067bf-105">\_Switch affidabile/no</span><span class="sxs-lookup"><span data-stu-id="067bf-105">/no\_robust switch</span></span>

<span data-ttu-id="067bf-106">Il **com/notore \_ affidabile** indica al compilatore MIDL di disabilitare in modo esplicito la funzionalità della riga di comando di [**/robust**](-robust.md) .</span><span class="sxs-lookup"><span data-stu-id="067bf-106">The **/no\_robust** switch directs the MIDL compiler to explicitly disable the [**/robust**](-robust.md) command line feature.</span></span> <span data-ttu-id="067bf-107">L'opzione della riga di comando **/robust** e le funzionalità associate sono le impostazioni predefinite del compilatore per MIDL Version 6.0.359 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="067bf-107">The **/robust** command line switch and its associated features is the default compiler setting for MIDL version 6.0.359 and later.</span></span>

``` syntax
midl /no_robust
```

## <a name="switch-options"></a><span data-ttu-id="067bf-108">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="067bf-108">Switch Options</span></span>

<span data-ttu-id="067bf-109">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="067bf-109">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="067bf-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="067bf-110">Remarks</span></span>

<span data-ttu-id="067bf-111">Con MIDL Version 6.0.359 e versioni successive, il compilatore MIDL imposta [**/robust**](-robust.md) per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="067bf-111">With MIDL version 6.0.359 and later, the MIDL compiler sets [**/robust**](-robust.md) by default.</span></span> <span data-ttu-id="067bf-112">È necessario usare l'opzione della riga di comando **/No \_ robusta** per disabilitare la funzionalità **/robust** se è necessario eseguire stub generati in Microsoft Windows NT, Windows 95/98 o Windows me.</span><span class="sxs-lookup"><span data-stu-id="067bf-112">The **/no\_robust** command line switch must be used to disable the **/robust** feature if generated stubs need to run on Microsoft WindowsÂ NT, WindowsÂ 95/98, or WindowsÂ Me.</span></span>

## <a name="examples"></a><span data-ttu-id="067bf-113">Esempio</span><span class="sxs-lookup"><span data-stu-id="067bf-113">Examples</span></span>

<span data-ttu-id="067bf-114">**MIDL/No \_ Solid filename. idl**</span><span class="sxs-lookup"><span data-stu-id="067bf-114">**midl /no\_robust filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="067bf-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="067bf-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="067bf-116">Sintassi della riga di comando MIDL generale</span><span class="sxs-lookup"><span data-stu-id="067bf-116">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="067bf-117">**/Robust**</span><span class="sxs-lookup"><span data-stu-id="067bf-117">**/robust**</span></span>](-robust.md)
</dt> </dl>

 

 




