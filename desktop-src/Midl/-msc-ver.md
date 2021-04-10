---
title: /msc_ver opzione
description: L' \_ opzione/MSC ver viene utilizzata per consentire a MIDL di generare codice che include ottimizzazioni per versioni diverse dei compilatori Microsoft C/C++.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver switch MIDL
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3620b3c8ffb1315a4d34eb0b4b2497c1cb3d805
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857545"
---
# <a name="msc_ver-switch"></a><span data-ttu-id="a652b-104">\_opzione ver/MSC</span><span class="sxs-lookup"><span data-stu-id="a652b-104">/msc\_ver switch</span></span>

<span data-ttu-id="a652b-105">L'opzione **/MSC \_ ver** viene utilizzata per consentire a MIDL di generare codice che include ottimizzazioni per versioni diverse dei compilatori Microsoft C/C++.</span><span class="sxs-lookup"><span data-stu-id="a652b-105">The **/msc\_ver** switch is used to allow MIDL to generate code that includes optimizations for different versions of Microsoft C/C++ compilers.</span></span>

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a><span data-ttu-id="a652b-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="a652b-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="a652b-107">*numero di versione \_*</span><span class="sxs-lookup"><span data-stu-id="a652b-107">*version\_number*</span></span> 
</dt> <dd>

<span data-ttu-id="a652b-108">Specifica un numero di versione Integer del compilatore Microsoft Visual C++ che verrà usato per compilare gli stub client e server dell'applicazione distribuita.</span><span class="sxs-lookup"><span data-stu-id="a652b-108">Specifies an integer version number of the Microsoft Visual C++ compiler that will be used to compile the client and server stubs of the distributed application.</span></span> <span data-ttu-id="a652b-109">Il numero di versione predefinito è 1100, che corrisponde a Visual C++ versione 5,0.</span><span class="sxs-lookup"><span data-stu-id="a652b-109">The default version number is 1100, which corresponds to Visual C++ version 5.0.</span></span> <span data-ttu-id="a652b-110">Il numero di versione 1200 corrisponde a Visual C++ versione 6,0 e così via.</span><span class="sxs-lookup"><span data-stu-id="a652b-110">The version number 1200 corresponds to Visual C++ version 6.0, and so on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a652b-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="a652b-111">Remarks</span></span>

<span data-ttu-id="a652b-112">In particolare, i valori di versione 1100 o superiore fanno sì che il compilatore MIDL generi codice usando la direttiva **\_ \_ declspec (UUID)** .</span><span class="sxs-lookup"><span data-stu-id="a652b-112">In particular, version values of 1100 or greater cause the MIDL compiler to generate code utilizing the **\_\_declspec(uuid())** directive.</span></span> <span data-ttu-id="a652b-113">Attiva inoltre le macro che usano le direttive **\_ \_ declspec (selectany)** e **\_ \_ declspec (novtable)** .</span><span class="sxs-lookup"><span data-stu-id="a652b-113">It also activates macros that use the **\_\_declspec(selectany)** and **\_\_declspec(novtable)** directives.</span></span>

 

 




