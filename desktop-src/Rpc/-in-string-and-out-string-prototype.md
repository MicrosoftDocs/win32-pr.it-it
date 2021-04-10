---
title: " in, String e out, prototipo di stringa"
description: Il prototipo di funzione seguente usa due parametri, ovvero un parametro \ in, String \ parameter e un parametro \ out, String \.
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963398"
---
# <a name="in-string-and-out-string-prototype"></a><span data-ttu-id="a01cc-103">\[in, String \] e \[ out, \] prototipo di stringa</span><span class="sxs-lookup"><span data-stu-id="a01cc-103">\[in, string\] and \[out, string\] Prototype</span></span>

<span data-ttu-id="a01cc-104">Il prototipo di funzione seguente usa due parametri: un \[ parametro in, un parametro [**di**](/windows/desktop/Midl/in) [**stringa**](/windows/desktop/Midl/string) \] e un \[ parametro [**out**](/windows/desktop/Midl/out-idl), **String** \] .</span><span class="sxs-lookup"><span data-stu-id="a01cc-104">The following function prototype uses two parameters: an \[[**in**](/windows/desktop/Midl/in), [**string**](/windows/desktop/Midl/string)\] parameter and an \[[**out**](/windows/desktop/Midl/out-idl), **string**\] parameter.</span></span>

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

<span data-ttu-id="a01cc-105">Il primo parametro è \[ solo [**in**](/windows/desktop/Midl/in) \] .</span><span class="sxs-lookup"><span data-stu-id="a01cc-105">The first parameter is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="a01cc-106">Questa stringa di input viene trasmessa solo dal client al server.</span><span class="sxs-lookup"><span data-stu-id="a01cc-106">This input string is only transmitted from the client to the server.</span></span> <span data-ttu-id="a01cc-107">Il server lo utilizza come base per l'ulteriore elaborazione.</span><span class="sxs-lookup"><span data-stu-id="a01cc-107">The server uses it as the basis for further processing.</span></span> <span data-ttu-id="a01cc-108">La stringa non viene modificata e non è richiesta nuovamente dal client, pertanto non è necessario che venga restituita al client.</span><span class="sxs-lookup"><span data-stu-id="a01cc-108">The string is not modified and is not required again by the client, so it does not have to be returned to the client.</span></span>

<span data-ttu-id="a01cc-109">Il secondo parametro, che rappresenta la risposta del dottore, è \[ [](/windows/desktop/Midl/out-idl) \] solo out.</span><span class="sxs-lookup"><span data-stu-id="a01cc-109">The second parameter, representing the doctor's response, is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="a01cc-110">Questa stringa di risposta viene trasmessa solo dal server al client.</span><span class="sxs-lookup"><span data-stu-id="a01cc-110">This response string is only transmitted from the server to the client.</span></span> <span data-ttu-id="a01cc-111">Le dimensioni di allocazione vengono fornite in modo che gli stub del server possano allocare memoria.</span><span class="sxs-lookup"><span data-stu-id="a01cc-111">The allocation size is provided so that the server stubs can allocate memory for it.</span></span> <span data-ttu-id="a01cc-112">Poiché *pszOutput* è un \[ puntatore [**ref**](/windows/desktop/Midl/ref) \] , il client deve disporre di memoria sufficiente allocata per la stringa prima della chiamata.</span><span class="sxs-lookup"><span data-stu-id="a01cc-112">Since *pszOutput* is a \[[**ref**](/windows/desktop/Midl/ref)\] pointer, the client must have sufficient memory allocated for the string before the call.</span></span> <span data-ttu-id="a01cc-113">La stringa di risposta viene scritta in questa area di memoria quando la procedura remota restituisce.</span><span class="sxs-lookup"><span data-stu-id="a01cc-113">The response string is written into this area of memory when the remote procedure returns.</span></span>

 

 