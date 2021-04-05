---
title: attributo notify_flag
description: L'attributo \ Notify \_ flag \ fornisce una notifica che identifica se viene chiamata una routine del server.
ms.assetid: a40b7114-d2e3-40c1-a0b1-599428188611
keywords:
- attributo notify_flag MIDL
topic_type:
- apiref
api_name:
- notify_flag
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af61999f0527b599cf358c38288a8c67473445a9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045566"
---
# <a name="notify_flag-attribute"></a><span data-ttu-id="fc920-104">notifica \_ flag-attributo</span><span class="sxs-lookup"><span data-stu-id="fc920-104">notify\_flag attribute</span></span>

<span data-ttu-id="fc920-105">L'attributo **\[ Notify \_ flag \]** fornisce una notifica che identifica se viene chiamata una routine del server.</span><span class="sxs-lookup"><span data-stu-id="fc920-105">The **\[notify\_flag\]** attribute provides notification identifying whether a server routine is called.</span></span>

``` syntax
[notify_flag] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="fc920-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fc920-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc920-107">*nome procedura*</span><span class="sxs-lookup"><span data-stu-id="fc920-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="fc920-108">Nome della procedura remota a cui \_ è associata la procedura relativa al flag di notifica.</span><span class="sxs-lookup"><span data-stu-id="fc920-108">Name of the remote procedure with which the notify\_flag procedure is associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc920-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="fc920-109">Remarks</span></span>

<span data-ttu-id="fc920-110">L'attributo **\[ Notify \_ flag \]** è simile nell'utilizzo dell'attributo **\[ Notify \]** .</span><span class="sxs-lookup"><span data-stu-id="fc920-110">The **\[notify\_flag\]** attribute is similar in usage to the **\[notify\]** attribute.</span></span>

<span data-ttu-id="fc920-111">Il nome della procedura del **\[ \_ flag \] di notifica** è il nome della procedura remota con suffisso per **\_ notifica \_ flag**.</span><span class="sxs-lookup"><span data-stu-id="fc920-111">The **\[notify\_flag\]** procedure name is the name of the remote procedure suffixed by **\_notify\_flag**.</span></span> <span data-ttu-id="fc920-112">La procedura di **\_ notifica del \_ flag** non richiede alcun parametro e non restituisce alcun risultato.</span><span class="sxs-lookup"><span data-stu-id="fc920-112">The **\_notify\_flag** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="fc920-113">Nel file di intestazione viene anche generato un prototipo di questa procedura.</span><span class="sxs-lookup"><span data-stu-id="fc920-113">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="fc920-114">Ad esempio, se il file IDL contiene quanto segue:</span><span class="sxs-lookup"><span data-stu-id="fc920-114">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="fc920-115">Specificare quanto segue in ACF per MIDL per generare la chiamata al **\_ \_ flag di notifica** :</span><span class="sxs-lookup"><span data-stu-id="fc920-115">Specify the following in the ACF for MIDL to generate the **\_notify\_flag** call:</span></span>

``` syntax
[notify_flag] MyProcedure();
```

<span data-ttu-id="fc920-116">Il compilatore MIDL genererà il codice stub del server che contiene la chiamata seguente alla procedura relativa al **\_ \_ flag di notifica** :</span><span class="sxs-lookup"><span data-stu-id="fc920-116">The MIDL compiler will generate server stub code which contains the following call to the **\_notify\_flag** procedure:</span></span>

``` syntax
MyProcedure_notify_flag();
```

<span data-ttu-id="fc920-117">Il file di intestazione conterrà un prototipo:</span><span class="sxs-lookup"><span data-stu-id="fc920-117">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify_flag(boolean __MIDL_NotifyFlag);
```

<span data-ttu-id="fc920-118">**\_ MIDL \_ PARETE NOTIFYFLAG** è **true** se viene chiamata la routine del server.</span><span class="sxs-lookup"><span data-stu-id="fc920-118">**\_MIDL\_NotifyFlag** is **TRUE** if the server routine is called.</span></span>

## <a name="examples"></a><span data-ttu-id="fc920-119">Esempi</span><span class="sxs-lookup"><span data-stu-id="fc920-119">Examples</span></span>

``` syntax
[notify_flag] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="fc920-120">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="fc920-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc920-121">**comunica**</span><span class="sxs-lookup"><span data-stu-id="fc920-121">**notify**</span></span>](notify.md)
</dt> </dl>

 

 




