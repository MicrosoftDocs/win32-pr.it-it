---
title: version (attributo)
description: L'attributo \ Version \ Interface identifica una particolare versione tra più versioni di un'interfaccia RPC. Con l'attributo Version è possibile garantire che solo le versioni compatibili del software client e server siano consentite per l'associazione.
ms.assetid: 66ac5cf3-2230-44fd-aaf6-8013e4a4ae81
keywords:
- attributo Version MIDL
topic_type:
- apiref
api_name:
- version
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bacbf7478ebfb745e5fc9b5e50959d0f1587dedf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045766"
---
# <a name="version-attribute"></a><span data-ttu-id="a7103-105">version (attributo)</span><span class="sxs-lookup"><span data-stu-id="a7103-105">version attribute</span></span>

<span data-ttu-id="a7103-106">L'attributo **\[ version \]** Interface identifica una particolare versione tra più versioni di un'interfaccia RPC.</span><span class="sxs-lookup"><span data-stu-id="a7103-106">The **\[version\]** interface attribute identifies a particular version among multiple versions of an RPC interface.</span></span> <span data-ttu-id="a7103-107">Con l'attributo Version è possibile garantire che solo le versioni compatibili del software client e server siano consentite per l'associazione.</span><span class="sxs-lookup"><span data-stu-id="a7103-107">With the version attribute, you ensure that only compatible versions of client and server software are allowed to bind.</span></span>

``` syntax
version ( major-value[[. minor-value]] )
```

## <a name="parameters"></a><span data-ttu-id="a7103-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a7103-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7103-109">*valore principale*</span><span class="sxs-lookup"><span data-stu-id="a7103-109">*major-value*</span></span> 
</dt> <dd>

<span data-ttu-id="a7103-110">Specifica un Unsigned Integer breve compreso tra zero e 65.535, inclusi, che rappresenta il numero di versione principale.</span><span class="sxs-lookup"><span data-stu-id="a7103-110">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the major version number.</span></span>

</dd> <dt>

<span data-ttu-id="a7103-111">*valore secondario*</span><span class="sxs-lookup"><span data-stu-id="a7103-111">*minor-value*</span></span> 
</dt> <dd>

<span data-ttu-id="a7103-112">Specifica un Unsigned Integer breve compreso tra zero e 65.535, inclusi, che rappresenta il numero della versione secondaria.</span><span class="sxs-lookup"><span data-stu-id="a7103-112">Specifies a short unsigned integer between zero and 65,535, inclusive, that represents the minor version number.</span></span> <span data-ttu-id="a7103-113">Il valore della versione secondaria è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a7103-113">The minor version value is optional.</span></span> <span data-ttu-id="a7103-114">Se presente, il valore della versione secondaria è separato dal numero di versione principale per un carattere punto (.).</span><span class="sxs-lookup"><span data-stu-id="a7103-114">If present, the minor version value is separated from the major version number by a period character (.).</span></span> <span data-ttu-id="a7103-115">Se non è specificato, il valore della versione secondaria è zero.</span><span class="sxs-lookup"><span data-stu-id="a7103-115">If not specified, the minor version value is zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7103-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="a7103-116">Remarks</span></span>

<span data-ttu-id="a7103-117">Il compilatore MIDL non supporta più versioni di un'interfaccia COM.</span><span class="sxs-lookup"><span data-stu-id="a7103-117">The MIDL compiler does not support multiple versions of a COM interface.</span></span> <span data-ttu-id="a7103-118">Di conseguenza, un elenco di attributi di interfaccia che include l'attributo dell' **\[** [**oggetto**](object.md) **\]** non può includere l'attributo **\[ version \]** .</span><span class="sxs-lookup"><span data-stu-id="a7103-118">As a result, an interface attribute list that includes the **\[**[**object**](object.md)**\]** attribute cannot include the **\[version\]** attribute.</span></span> <span data-ttu-id="a7103-119">Per creare una nuova versione di un'interfaccia COM esistente, usare l'ereditarietà dell'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a7103-119">To create a new version of an existing COM interface, use interface inheritance.</span></span> <span data-ttu-id="a7103-120">Un'interfaccia COM derivata ha un UUID diverso ma eredita le funzioni membro di interfaccia, i codici di stato e gli attributi di interfaccia dell'interfaccia di base.</span><span class="sxs-lookup"><span data-stu-id="a7103-120">A derived COM interface has a different UUID but inherits the interface member functions, status codes, and interface attributes of the base interface.</span></span>

<span data-ttu-id="a7103-121">In combinazione con il **\[** [](uuid.md) **\]** valore UUID, il valore della **\[ versione \]** identifica in modo univoco l'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a7103-121">In combination with the **\[**[**uuid**](uuid.md)**\]** value, the **\[version\]** value uniquely identifies the interface.</span></span> <span data-ttu-id="a7103-122">La libreria di run-time passa i valori di **\[ versione \]** e **\[ UUID \]** al server quando il client chiama una funzione remota.</span><span class="sxs-lookup"><span data-stu-id="a7103-122">The run-time library passes the **\[version\]** and **\[uuid\]** values to the server when the client calls a remote function.</span></span> <span data-ttu-id="a7103-123">Un client può eseguire l'associazione a un server per una data interfaccia se:</span><span class="sxs-lookup"><span data-stu-id="a7103-123">A client can bind to a server for a given interface if:</span></span>

-   <span data-ttu-id="a7103-124">Il valore **\[ UUID \]** è lo stesso.</span><span class="sxs-lookup"><span data-stu-id="a7103-124">The **\[uuid\]** value is the same.</span></span>
-   <span data-ttu-id="a7103-125">Il numero di versione principale è lo stesso.</span><span class="sxs-lookup"><span data-stu-id="a7103-125">The major version number is the same.</span></span>
-   <span data-ttu-id="a7103-126">Il numero di versione secondario del client è minore o uguale al numero di versione secondario del server.</span><span class="sxs-lookup"><span data-stu-id="a7103-126">The client's minor version number is less than or equal to the server's minor version number.</span></span>

<span data-ttu-id="a7103-127">Si tratta del vantaggio e del vantaggio degli utenti per mantenere la compatibilità verso l'alto tra versionsÂ, per modificare l'interfaccia in modo che solo il numero di versione secondario venga modificato.</span><span class="sxs-lookup"><span data-stu-id="a7103-127">It is to your benefit and your users' benefit to retain upward compatibility among versionsÂ that is, to modify the interface so that only the minor version number changes.</span></span> <span data-ttu-id="a7103-128">È possibile mantenere la compatibilità con l'alto quando si aggiungono nuovi tipi di dati che non vengono utilizzati dalle funzioni esistenti e quando si aggiungono nuove funzioni senza modificare la specifica dell'interfaccia per le funzioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="a7103-128">You can retain upward compatibility when you add new data types that are not used by existing functions and when you add new functions without changing the interface specification for existing functions.</span></span>

<span data-ttu-id="a7103-129">Modificare il numero di versione principale se si verifica una delle condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7103-129">Change the major version number if any one of the following conditions apply:</span></span>

-   <span data-ttu-id="a7103-130">Se si modifica un tipo di dati utilizzato da una funzione esistente.</span><span class="sxs-lookup"><span data-stu-id="a7103-130">If you change a data type that is used by an existing function.</span></span>
-   <span data-ttu-id="a7103-131">Se si modifica la specifica dell'interfaccia per una funzione esistente (ad esempio l'aggiunta o la rimozione di un parametro).</span><span class="sxs-lookup"><span data-stu-id="a7103-131">If you change the interface specification for an existing function (such as adding or removing a parameter).</span></span>
-   <span data-ttu-id="a7103-132">Se si aggiungono callback chiamati da funzioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="a7103-132">If you add callbacks that are called by existing functions.</span></span>

<span data-ttu-id="a7103-133">Modificare il numero di versione secondario se si verificano tutte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="a7103-133">Change the minor version number if all of the following conditions apply:</span></span>

-   <span data-ttu-id="a7103-134">Se si aggiungono le definizioni o le costanti di tipo non utilizzate da funzioni o callback esistenti.</span><span class="sxs-lookup"><span data-stu-id="a7103-134">If you add type definitions or constants that are not used by any existing functions or callbacks.</span></span>
-   <span data-ttu-id="a7103-135">Se non si modificano funzioni esistenti e si aggiungono nuove funzioni all'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a7103-135">If you do not change any existing functions and you add new functions to the interface.</span></span>
-   <span data-ttu-id="a7103-136">Se si aggiungono callback che non vengono chiamati da funzioni esistenti e i nuovi callback seguono tutte le funzioni esistenti.</span><span class="sxs-lookup"><span data-stu-id="a7103-136">If you add callbacks that are not called by any existing functions and the new callbacks follow any existing functions.</span></span>

<span data-ttu-id="a7103-137">Se le modifiche sono qualificate come una modifica compatibile con le versioni successive dell'interfaccia, attenersi alla procedura riportata di seguito.</span><span class="sxs-lookup"><span data-stu-id="a7103-137">If your modifications qualify as an upward-compatible change to the interface, use the following procedure.</span></span>

<span data-ttu-id="a7103-138">**Per modificare il file dell'interfaccia (IDL)**</span><span class="sxs-lookup"><span data-stu-id="a7103-138">**To modify the interface (IDL) file**</span></span>

1.  <span data-ttu-id="a7103-139">Aggiungere nuove definizioni di costanti e tipi al file di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a7103-139">Add new constant and type definitions to the interface file.</span></span>
2.  <span data-ttu-id="a7103-140">Aggiungere funzioni di callback alla fine del file di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a7103-140">Add callback functions to the end of the interface file.</span></span>
3.  <span data-ttu-id="a7103-141">Aggiungere nuove funzioni alla fine del file di interfaccia.</span><span class="sxs-lookup"><span data-stu-id="a7103-141">Add new functions to the end of the interface file.</span></span>

<span data-ttu-id="a7103-142">L'attributo **\[ version \]** può essere presente al massimo una volta nell'intestazione Interface.</span><span class="sxs-lookup"><span data-stu-id="a7103-142">The **\[version\]** attribute can occur at most once in the interface header.</span></span>

<span data-ttu-id="a7103-143">Quando l'attributo Version non è presente, l'interfaccia ha la versione predefinita 0,0.</span><span class="sxs-lookup"><span data-stu-id="a7103-143">When the version attribute is not present, the interface has a default version of 0.0.</span></span>

<span data-ttu-id="a7103-144">Il carattere punto tra i numeri principali e secondari è un delimitatore e non rappresenta un separatore decimale.</span><span class="sxs-lookup"><span data-stu-id="a7103-144">The period character between the major and minor numbers is a delimiter and does not represent a decimal point.</span></span> <span data-ttu-id="a7103-145">Il numero secondario viene considerato come un numero intero.</span><span class="sxs-lookup"><span data-stu-id="a7103-145">The minor number is treated as an integer.</span></span> <span data-ttu-id="a7103-146">Gli zeri iniziali non sono significativi.</span><span class="sxs-lookup"><span data-stu-id="a7103-146">Leading zeroes are not significant.</span></span> <span data-ttu-id="a7103-147">Gli zeri finali sono significativi.</span><span class="sxs-lookup"><span data-stu-id="a7103-147">Trailing zeroes are significant.</span></span>

<span data-ttu-id="a7103-148">Ad esempio, l'impostazione della versione 1,11 rappresenta un valore principale di uno e un valore secondario pari a undici.</span><span class="sxs-lookup"><span data-stu-id="a7103-148">For example, the version setting 1.11 represents a major value of one and a minor value of eleven.</span></span> <span data-ttu-id="a7103-149">La versione 1,11 non rappresenta un valore compreso tra 1,1 e 1,2.</span><span class="sxs-lookup"><span data-stu-id="a7103-149">Version 1.11 does not represent a value between 1.1 and 1.2.</span></span>

## <a name="see-also"></a><span data-ttu-id="a7103-150">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a7103-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7103-151">File di definizione dell'interfaccia (IDL)</span><span class="sxs-lookup"><span data-stu-id="a7103-151">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a7103-152">**interfaccia**</span><span class="sxs-lookup"><span data-stu-id="a7103-152">**interface**</span></span>](interface.md)
</dt> <dt>

[<span data-ttu-id="a7103-153">**oggetto**</span><span class="sxs-lookup"><span data-stu-id="a7103-153">**object**</span></span>](object.md)
</dt> <dt>

[<span data-ttu-id="a7103-154">**uuid**</span><span class="sxs-lookup"><span data-stu-id="a7103-154">**uuid**</span></span>](uuid.md)
</dt> </dl>

 

 




