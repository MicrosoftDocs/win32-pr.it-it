---
title: DllSurrogateExecutable
description: Consente l'esecuzione dei server DLL in un processo surrogato personalizzato, insieme al valore del registro di sistema DllSurrogate. Se DllSurrogateExecutable viene omesso, COM passa NULL come valore per il primo parametro della funzione CreateProcess.
ms.assetid: faf5dde3-bd67-447b-a88c-e8660dc5228e
keywords:
- Valore DllSurrogateExecutable del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877297673b0a518006ecf903f447984f9023da34
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "106300555"
---
# <a name="dllsurrogateexecutable"></a><span data-ttu-id="1e454-105">DllSurrogateExecutable</span><span class="sxs-lookup"><span data-stu-id="1e454-105">DllSurrogateExecutable</span></span>

<span data-ttu-id="1e454-106">Consente l'esecuzione dei server DLL in un processo surrogato personalizzato, insieme al valore del registro di sistema [**DllSurrogate**](dllsurrogate.md) .</span><span class="sxs-lookup"><span data-stu-id="1e454-106">Enables DLL servers to run in a custom surrogate process, in conjunction with the [**DllSurrogate**](dllsurrogate.md) registry value.</span></span> <span data-ttu-id="1e454-107">Se **DllSurrogateExecutable** viene omesso, com passa **null** come valore per il primo parametro della funzione [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="1e454-107">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="1e454-108">Voce del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="1e454-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      DllSurrogateExecutable = file
```

## <a name="remarks"></a><span data-ttu-id="1e454-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="1e454-109">Remarks</span></span>

<span data-ttu-id="1e454-110">Questo valore è di tipo **reg \_ SZ**.</span><span class="sxs-lookup"><span data-stu-id="1e454-110">This value is of type **REG\_SZ**.</span></span> <span data-ttu-id="1e454-111">Funziona insieme al valore [**DllSurrogate**](dllsurrogate.md) per evitare ambiguità quando si usa la funzione [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="1e454-111">It works in conjunction with the [**DllSurrogate**](dllsurrogate.md) value to prevent any ambiguity when using the [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) function.</span></span> <span data-ttu-id="1e454-112">**DllSurrogate** indica se è necessario usare un surrogato personalizzato e queste informazioni vengono passate come primo parametro per **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="1e454-112">**DllSurrogate** indicates whether a custom surrogate needs to be used, and this information is passed as the first parameter for **CreateProcess**.</span></span> <span data-ttu-id="1e454-113">A seconda dell'implementazione di **CreateProcess**, le informazioni potrebbero essere ambigue.</span><span class="sxs-lookup"><span data-stu-id="1e454-113">Depending on the implementation of **CreateProcess**, this information might be ambiguous.</span></span> <span data-ttu-id="1e454-114">Se viene specificato **DllSurrogateExecutable** , com passa il valore come primo parametro di **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="1e454-114">If **DllSurrogateExecutable** is specified, COM passes the value as the first parameter of **CreateProcess**.</span></span> <span data-ttu-id="1e454-115">Se **DllSurrogateExecutable** viene omesso, com passa **null** come valore per il primo parametro di **CreateProcess**.</span><span class="sxs-lookup"><span data-stu-id="1e454-115">If **DllSurrogateExecutable** is not specified, COM passes **NULL** as the value for the first parameter of **CreateProcess**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e454-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="1e454-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e454-117">**CoRegisterSurrogate**</span><span class="sxs-lookup"><span data-stu-id="1e454-117">**CoRegisterSurrogate**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate)
</dt> <dt>

[<span data-ttu-id="1e454-118">Surrogati DLL</span><span class="sxs-lookup"><span data-stu-id="1e454-118">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> <dt>

[<span data-ttu-id="1e454-119">**DllSurrogate**</span><span class="sxs-lookup"><span data-stu-id="1e454-119">**DllSurrogate**</span></span>](dllsurrogate.md)
</dt> <dt>

[<span data-ttu-id="1e454-120">**ISurrogate**</span><span class="sxs-lookup"><span data-stu-id="1e454-120">**ISurrogate**</span></span>](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate)
</dt> </dl>

 

 