---
title: Verifica delle opzioni del preprocessore
description: Il compilatore MIDL richiama in modo implicito il preprocessore e non Visualizza le opzioni del preprocessore.
ms.assetid: 2f402af4-18d7-480c-a8d2-d16f402ef87a
keywords:
- MIDL Compiler MIDL, verifica delle opzioni del preprocessore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19a047980c9f2f9dc8deffdcf85de767e4dc8705
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856322"
---
# <a name="verifying-preprocessor-options"></a><span data-ttu-id="723c1-104">Verifica delle opzioni del preprocessore</span><span class="sxs-lookup"><span data-stu-id="723c1-104">Verifying Preprocessor Options</span></span>

<span data-ttu-id="723c1-105">Il compilatore MIDL richiama in modo implicito il preprocessore e non Visualizza le opzioni del preprocessore.</span><span class="sxs-lookup"><span data-stu-id="723c1-105">The MIDL compiler implicitly invokes the preprocessor and does not display its preprocessor switches.</span></span> <span data-ttu-id="723c1-106">In assenza del commutatore [**/cpp \_**](-cpp-opt.md) di MIDL, la riga di comando del preprocessore è costituita da tutte le opzioni [**/I**](-i.md), [**/d**](-d.md) e [**/u**](-u.md) usate nella riga di comando MIDL, oltre che dalle opzioni **/e** e [**/nologo**](-nologo.md) .</span><span class="sxs-lookup"><span data-stu-id="723c1-106">In the absence of the MIDL [**/cpp\_opt**](-cpp-opt.md) switch, the preprocessor command line is composed of all the [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) switches used in the MIDL command line, as well as **/E** and [**/nologo**](-nologo.md) switches.</span></span> <span data-ttu-id="723c1-107">Per visualizzare le opzioni passate al preprocessore, usare l'opzione [**/Confirm**](-confirm.md) del compilatore.</span><span class="sxs-lookup"><span data-stu-id="723c1-107">To see the switches passed on to the preprocessor, use the compiler's [**/confirm**](-confirm.md) switch.</span></span>

<span data-ttu-id="723c1-108">Ad esempio, la riga seguente</span><span class="sxs-lookup"><span data-stu-id="723c1-108">For example, the following line</span></span>

<span data-ttu-id="723c1-109">**midl.exe-D \_ Win32 \_ WinNT = 0x501-Solid-DNTENV = 1-ID: \\ NT \\ public \\ SDK \\ Inc-Confirm-Oicf-ENV Win32-out x86 stub. idl**</span><span class="sxs-lookup"><span data-stu-id="723c1-109">**midl.exe -D\_WIN32\_WINNT=0x501 -robust -DNTENV=1 -Id:\\nt\\public\\sdk\\inc -confirm -Oicf -env win32 -out x86 stub.idl**</span></span>

<span data-ttu-id="723c1-110">produce l'output seguente:</span><span class="sxs-lookup"><span data-stu-id="723c1-110">produces the following output:</span></span>

``` syntax
32 bit arguments
          input file -  stub.idl
          app_config -  No
               c_ext -  Yes
              client -  stub
                char -  signed
             confirm -  Yes
             cpp_cmd -  cl.exe
             cpp_opt -  -Id:\nt\public\sdk\inc -D_WIN32_WINNT=0x501 -DNTENV=1  -
E -nologo
             msc_ver -  1100
               cstub -  i386\stub_c.c
                   D -  -D_WIN32_WINNT=0x501 -DNTENV=1
                 env -  win32
            append64 -  No
               rpcss -  No
             use_epv -  No
      no_default_epv -  No
               error -  allocation ref bounds_check enum stub_data
              header -  i386\stub.h
                   I -  -Id:\nt\public\sdk\inc
              nologo -  No
              ms_ext -  Yes
            ms_union -  No
       no_format_opt -  No
            oldnames -  No
                 out -  i386\
              server -  stub
               sstub -  i386\stub_s.c
                   O -  interpreted stubs
                   W -  1
                  Zp -  8
```

 

 




