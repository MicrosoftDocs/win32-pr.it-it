---
title: Async (attributo)
description: L'attributo \ Async \ ACF definisce una chiamata di procedura remota come operazione asincrona.
ms.assetid: 8002980a-94be-4d45-99d7-dfa4eae7f102
keywords:
- MIDL dell'attributo asincrono
topic_type:
- apiref
api_name:
- async
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 562b157f26078c6f4d5b3cffe47417fa18fe608d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103956415"
---
# <a name="async-attribute"></a><span data-ttu-id="dff9d-104">Async (attributo)</span><span class="sxs-lookup"><span data-stu-id="dff9d-104">async attribute</span></span>

<span data-ttu-id="dff9d-105">L' \[ attributo **asincrono** \] ACF definisce una chiamata di procedura remota come operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="dff9d-105">The \[**async**\] ACF attribute defines a remote procedure call as an asynchronous operation.</span></span>

``` syntax
[async, opt-acf-attributes] function-name (param-list)
```

## <a name="parameters"></a><span data-ttu-id="dff9d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dff9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dff9d-107">*opz-ACF-attributi*</span><span class="sxs-lookup"><span data-stu-id="dff9d-107">*opt-acf-attributes*</span></span> 
</dt> <dd>

<span data-ttu-id="dff9d-108">Specifica gli attributi facoltativi di configurazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="dff9d-108">Specifies optional application configuration attributes.</span></span>

</dd> <dt>

<span data-ttu-id="dff9d-109">*Nome funzione*</span><span class="sxs-lookup"><span data-stu-id="dff9d-109">*function-name*</span></span> 
</dt> <dd>

<span data-ttu-id="dff9d-110">Specifica il nome della funzione nel file IDL.</span><span class="sxs-lookup"><span data-stu-id="dff9d-110">Specifies the name of the function in the IDL file.</span></span>

</dd> <dt>

<span data-ttu-id="dff9d-111">*param-list*</span><span class="sxs-lookup"><span data-stu-id="dff9d-111">*param-list*</span></span> 
</dt> <dd>

<span data-ttu-id="dff9d-112">Specifica un elenco di parametri facoltativo.</span><span class="sxs-lookup"><span data-stu-id="dff9d-112">Specifies an optional parameter list.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dff9d-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="dff9d-113">Remarks</span></span>

<span data-ttu-id="dff9d-114">Questo attributo non è applicabile nelle interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="dff9d-114">This attribute is not applicable in COM interfaces.</span></span>

<span data-ttu-id="dff9d-115">Per dichiarare una funzione RPC come asincrona, dichiarare prima la funzione come parte della definizione di un'interfaccia in un file IDL.</span><span class="sxs-lookup"><span data-stu-id="dff9d-115">To declare an RPC function as asynchronous, first declare the function as part of an interface definition in an IDL file.</span></span> <span data-ttu-id="dff9d-116">Modificare quindi la dichiarazione di funzione, all'interno del file di configurazione dell'applicazione (ACF), applicando l' \[  \] attributo Async.</span><span class="sxs-lookup"><span data-stu-id="dff9d-116">Then modify that function declaration, within the application configuration file (ACF), by applying the \[**async**\] attribute.</span></span> <span data-ttu-id="dff9d-117">Si noti che la dichiarazione di funzione non fa menzione dell'handle asincrono e che l'handle di associazione è il primo parametro.</span><span class="sxs-lookup"><span data-stu-id="dff9d-117">Note that the function declaration makes no mention of the asynchronous handle and that the binding handle is the first parameter.</span></span> <span data-ttu-id="dff9d-118">L'applicazione dell' \[ attributo **Async** \] nel file ACF genera il codice appropriato in modo che quando viene chiamata questa funzione, il server asincrono prevede di ricevere un handle asincrono prima degli altri parametri.</span><span class="sxs-lookup"><span data-stu-id="dff9d-118">Applying the \[**async**\] attribute in the ACF file generates the appropriate code so that when this function is called, the asynchronous server expects to receive an asynchronous handle before the other parameters.</span></span>

> [!Note]  
> <span data-ttu-id="dff9d-119">L'attributo Async non può essere usato con l'opzione della riga di comando [**/OSF**](-osf.md) .</span><span class="sxs-lookup"><span data-stu-id="dff9d-119">The async attribute cannot be used with the [**/osf**](-osf.md) command line switch.</span></span>

 

## <a name="examples"></a><span data-ttu-id="dff9d-120">Esempi</span><span class="sxs-lookup"><span data-stu-id="dff9d-120">Examples</span></span>

``` syntax
//file:Xasync.idl
interface AsyncIface 
{
    HRESULT MyAsyncFunc (
        handle_t hBinding,
        [in] int a,
        [in] int b,
        [out] int *c) ;
//other interface definitions
}
//end XAsync.idl

// file: Xasync.acf
interface AsyncIface
{
    [async] MyAsyncFunc () ;
    //any other ACF definitions
}
//end Xasync.acf
```

## <a name="see-also"></a><span data-ttu-id="dff9d-121">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="dff9d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dff9d-122">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="dff9d-122">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="dff9d-123">RPC asincrona</span><span class="sxs-lookup"><span data-stu-id="dff9d-123">Asynchronous RPC</span></span>](/windows/desktop/Rpc/asynchronous-rpc)
</dt> </dl>

 

 