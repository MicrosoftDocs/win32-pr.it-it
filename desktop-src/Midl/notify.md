---
title: notifica attributo
description: L'attributo \ Notify \ indica al compilatore MIDL di generare una chiamata a una procedura \ Notify \ sul lato server dell'applicazione.
ms.assetid: 24f9887b-04b7-491a-ab6e-7c078b967fbc
keywords:
- notifica attributo MIDL
topic_type:
- apiref
api_name:
- notify
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334223979298f54acb546bd0b9ec913afd92e286
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104516213"
---
# <a name="notify-attribute"></a><span data-ttu-id="886ea-104">notifica attributo</span><span class="sxs-lookup"><span data-stu-id="886ea-104">notify attribute</span></span>

<span data-ttu-id="886ea-105">L'attributo **\[ Notify \]** indica al compilatore MIDL di generare una chiamata a una procedura **\[ Notify \]** sul lato server dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="886ea-105">The **\[notify\]** attribute instructs the MIDL compiler to generate a call to a **\[notify\]** procedure on the server side of the application.</span></span>

``` syntax
[notify] procedure-name();
```

## <a name="parameters"></a><span data-ttu-id="886ea-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="886ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="886ea-107">*nome procedura*</span><span class="sxs-lookup"><span data-stu-id="886ea-107">*procedure-name*</span></span> 
</dt> <dd>

<span data-ttu-id="886ea-108">Nome della procedura remota a cui verrà associata la procedura di notifica.</span><span class="sxs-lookup"><span data-stu-id="886ea-108">The name of the remote procedure with which the notify procedure will be associated.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="886ea-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="886ea-109">Remarks</span></span>

<span data-ttu-id="886ea-110">La procedura di **\[ notifica \]** chiamata come risultato dell'attributo **\[ Notify \]** è associata a una specifica procedura remota nel server.</span><span class="sxs-lookup"><span data-stu-id="886ea-110">The **\[notify\]** procedure called as a result of the **\[notify\]** attribute is associated with a particular remote procedure on the server.</span></span> <span data-ttu-id="886ea-111">Si tratta di un concetto simile a una funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="886ea-111">It is similar in concept to a callback function.</span></span> <span data-ttu-id="886ea-112">Lo stub chiama la procedura **\[ Notify \]** dopo che sono stati sottoposti a marshalling tutti gli argomenti di output della procedura remota a cui è associato ed è stata liberata la memoria associata ai parametri.</span><span class="sxs-lookup"><span data-stu-id="886ea-112">The stub calls the **\[notify\]** procedure after all the output arguments of the remote procedure with which it is associated have been marshaled and any memory associated with the parameters is freed.</span></span> <span data-ttu-id="886ea-113">La routine **\[ Notify \]** viene chiamata se una chiamata ha esito negativo prima dell'esecuzione della routine del server.</span><span class="sxs-lookup"><span data-stu-id="886ea-113">The **\[notify\]** routine is called if a call fails before the server routine executes.</span></span> <span data-ttu-id="886ea-114">Se, ad esempio, si verifica un errore del server durante l'unmarshalling a causa della ricezione di dati non validi dal client, \[ \] viene chiamata la routine di notifica.</span><span class="sxs-lookup"><span data-stu-id="886ea-114">For example, if a server fails during unmarshaling due to receipt of bad data from the client, the \[notify\] routine is called.</span></span>

<span data-ttu-id="886ea-115">L'attributo **\[ Notify \]** è utile per lo sviluppo di applicazioni che acquisiscono risorse in procedure remote.</span><span class="sxs-lookup"><span data-stu-id="886ea-115">The **\[notify\]** attribute is useful to develop applications acquiring resources in remote procedures.</span></span> <span data-ttu-id="886ea-116">Queste risorse vengono quindi liberate nella procedura di **\[ notifica \]** dopo il marshalling completo dei parametri di output della procedura remota.</span><span class="sxs-lookup"><span data-stu-id="886ea-116">These resources are then freed in the **\[notify\]** procedure after the output parameters of the remote procedure are fully marshaled.</span></span>

<span data-ttu-id="886ea-117">Il nome della procedura di **\[ notifica \]** è il nome della procedura remota con suffisso **\_ notifica**.</span><span class="sxs-lookup"><span data-stu-id="886ea-117">The **\[notify\]** procedure name is the name of the remote procedure suffixed by **\_notify**.</span></span> <span data-ttu-id="886ea-118">La procedura di **\_ notifica** non richiede alcun parametro e non restituisce alcun risultato.</span><span class="sxs-lookup"><span data-stu-id="886ea-118">The **\_notify** procedure does not require any parameters and does not return a result.</span></span> <span data-ttu-id="886ea-119">Nel file di intestazione viene anche generato un prototipo di questa procedura.</span><span class="sxs-lookup"><span data-stu-id="886ea-119">A prototype of this procedure is also generated in the header file.</span></span> <span data-ttu-id="886ea-120">Ad esempio, se il file IDL contiene quanto segue:</span><span class="sxs-lookup"><span data-stu-id="886ea-120">For example, if the IDL file contains the following:</span></span>

``` syntax
MyProcedure([in] short S);
```

<span data-ttu-id="886ea-121">Specificare quanto segue in ACF per MIDL per generare la chiamata di **\_ notifica** :</span><span class="sxs-lookup"><span data-stu-id="886ea-121">Specify the following in the ACF for MIDL to generate the **\_notify** call:</span></span>

``` syntax
[notify] MyProcedure();
```

<span data-ttu-id="886ea-122">Il compilatore MIDL genererà il codice stub del server che contiene la chiamata seguente alla procedura **\_ Notify** :</span><span class="sxs-lookup"><span data-stu-id="886ea-122">The MIDL compiler will generate server stub code which contains the following call to the **\_notify** procedure:</span></span>

``` syntax
MyProcedure_notify();
```

<span data-ttu-id="886ea-123">Il file di intestazione conterrà un prototipo:</span><span class="sxs-lookup"><span data-stu-id="886ea-123">The header file will contain a prototype:</span></span>

``` syntax
void MyProcedure_notify(void);
```

## <a name="examples"></a><span data-ttu-id="886ea-124">Esempi</span><span class="sxs-lookup"><span data-stu-id="886ea-124">Examples</span></span>

``` syntax
[notify] MyProcedure();
```

## <a name="see-also"></a><span data-ttu-id="886ea-125">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="886ea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="886ea-126">File di configurazione dell'applicazione (ACF)</span><span class="sxs-lookup"><span data-stu-id="886ea-126">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> </dl>

 

 




