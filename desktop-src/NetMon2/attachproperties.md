---
description: La funzione di esportazione AttachProperties esegue il mapping delle proprietà a una posizione all'interno di una parte dei dati riconosciuti. AttachProperties deve essere implementato per ogni parser supportato dalla DLL del parser.
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: Funzione di callback AttachProperties (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 3b3cb4be93b8d960b39f0f5c5cf2b5a4809573cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311642"
---
# <a name="attachproperties-callback-function"></a><span data-ttu-id="c5ff9-104">Funzione di callback AttachProperties</span><span class="sxs-lookup"><span data-stu-id="c5ff9-104">AttachProperties callback function</span></span>

<span data-ttu-id="c5ff9-105">La funzione di esportazione **AttachProperties** esegue il mapping delle proprietà a una posizione all'interno di una parte dei dati riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-105">The **AttachProperties** export function maps the properties to a location within a piece of recognized data.</span></span> <span data-ttu-id="c5ff9-106">**AttachProperties** deve essere implementato per ogni parser supportato dalla dll del parser.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-106">**AttachProperties** must be implemented for each parser that the parser DLL supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5ff9-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c5ff9-107">Syntax</span></span>


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a><span data-ttu-id="c5ff9-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="c5ff9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ff9-109">*hFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5ff9-109">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ff9-110">Handle del frame da analizzare.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-110">Handle of the frame that is being parsed.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff9-111">*lpFrame* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5ff9-111">*lpFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ff9-112">Puntatore al primo byte in un frame.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-112">Pointer to the first byte in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff9-113">*lpProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5ff9-113">*lpProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ff9-114">Puntatore all'inizio dei dati riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-114">Pointer to the start of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff9-115">*MacType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5ff9-115">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ff9-116">Valore MAC del primo protocollo in un frame.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-116">MAC value of the first protocol in a frame.</span></span> <span data-ttu-id="c5ff9-117">*MacType* può essere uno dei seguenti:</span><span class="sxs-lookup"><span data-stu-id="c5ff9-117">The *MacType* can be one of the following:</span></span>



| <span data-ttu-id="c5ff9-118">Valore</span><span class="sxs-lookup"><span data-stu-id="c5ff9-118">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="c5ff9-119">Significato</span><span class="sxs-lookup"><span data-stu-id="c5ff9-119">Meaning</span></span>                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <span data-ttu-id="c5ff9-120"><dt>**\_Ethernet di tipo Mac \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ff9-120"><dt>**MAC\_TYPE\_ETHERNET**</dt></span></span> </dl>    | <span data-ttu-id="c5ff9-121">802.3</span><span class="sxs-lookup"><span data-stu-id="c5ff9-121">802.3</span></span> <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <span data-ttu-id="c5ff9-122"><dt>**\_Tokenring di tipo Mac \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ff9-122"><dt>**MAC\_TYPE\_TOKENRING**</dt></span></span> </dl> | <span data-ttu-id="c5ff9-123">802.5</span><span class="sxs-lookup"><span data-stu-id="c5ff9-123">802.5</span></span> <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <span data-ttu-id="c5ff9-124"><dt>**\_FDDI di tipo Mac \_**</dt></span><span class="sxs-lookup"><span data-stu-id="c5ff9-124"><dt>**MAC\_TYPE\_FDDI**</dt></span></span> </dl>                | <span data-ttu-id="c5ff9-125">ANSI X3T 9.5</span><span class="sxs-lookup"><span data-stu-id="c5ff9-125">ANSI X3T9.5</span></span> <br/> |



 

</dd> <dt>

<span data-ttu-id="c5ff9-126">*BytesLeft* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5ff9-126">*BytesLeft* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ff9-127">Numero rimanente di byte in un frame a partire dall'inizio dei dati riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-127">The remaining number of bytes in a frame   starting at the beginning of the recognized data.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff9-128">*hPreviousProtocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5ff9-128">*hPreviousProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ff9-129">Handle del protocollo precedente.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-129">Handle of the previous protocol.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff9-130">*nPreviousProtocolOffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5ff9-130">*nPreviousProtocolOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ff9-131">Offset del protocollo precedente a partire dall'inizio del frame.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-131">Offset of the previous protocol   starting at the beginning of the frame.</span></span>

</dd> <dt>

<span data-ttu-id="c5ff9-132">*lpInstData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c5ff9-132">*lpInstData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ff9-133">Puntatore ai dati dell'istanza forniti dal protocollo precedente.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-133">Pointer to the instance data that the previous protocol provides.</span></span> <span data-ttu-id="c5ff9-134">I dati dell'istanza non possono essere più lunghi di un \_ ptr DWORD di lunghezza.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-134">Instance data cannot be longer than a DWORD\_PTR in length.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ff9-135">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c5ff9-135">Return value</span></span>

<span data-ttu-id="c5ff9-136">Se la funzione ha esito positivo, il valore restituito è un puntatore al primo byte dopo i dati riconosciuti in un frame o **null** se i dati riconosciuti sono l'ultima parte di dati di un frame.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-136">If the function is successful, the return value is a pointer to the first byte after the recognized data in a frame or **NULL** if the recognized data is the last piece of data in a frame.</span></span>

<span data-ttu-id="c5ff9-137">Se la funzione ha esito negativo, il valore restituito è un puntatore ai dati riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-137">If the function is unsuccessful, the return value is a pointer to the recognized data.</span></span> <span data-ttu-id="c5ff9-138">Il parametro *lpProtocol* passa il puntatore alla DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-138">The *lpProtocol* parameter passes the pointer to the parser DLL.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ff9-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="c5ff9-139">Remarks</span></span>

<span data-ttu-id="c5ff9-140">Network Monitor chiama la funzione **AttachProperties** per ogni parser che riconosce una porzione di dati in un frame.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-140">Network Monitor calls the **AttachProperties** function for each parser that recognizes a piece of data in a frame.</span></span> <span data-ttu-id="c5ff9-141">Si noti che il parser determina quali proprietà sono presenti nei dati riconosciuti e dove si trova ogni proprietà.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-141">Note that the parser determines which properties exist in the recognized data, and where each property is located.</span></span>

<span data-ttu-id="c5ff9-142">Durante l'implementazione di **AttachProperties**, chiamare [AttachPropertyInstance](attachpropertyinstance.md) per usare i dati esistenti nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-142">During the implementation of **AttachProperties**, call [AttachPropertyInstance](attachpropertyinstance.md) to use the data as it exists in the capture.</span></span> <span data-ttu-id="c5ff9-143">È anche possibile chiamare la funzione [AttachPropertyInstanceEx](attachpropertyinstanceex.md) per modificare i dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-143">You can also call [AttachPropertyInstanceEx](attachpropertyinstanceex.md) function to modify the property data.</span></span> <span data-ttu-id="c5ff9-144">Tuttavia, si consiglia di usare i dati esistenti nell'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-144">However, it is advised that you use the data as it exists in the capture.</span></span>

<span data-ttu-id="c5ff9-145">Le funzioni **AttachPropertyInstanceEx** e **AttachPropertyInstance** vengono chiamate solo per le proprietà presenti nei dati riconosciuti.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-145">The **AttachPropertyInstanceEx** and **AttachPropertyInstance** functions are called only for the properties that exist in the recognized data.</span></span> <span data-ttu-id="c5ff9-146">Si noti che Network Monitor dispone di un [*database delle proprietà*](p.md) per il parser che contiene una descrizione di tutte le proprietà supportate dal parser.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-146">Note that Network Monitor has a [*property database*](p.md) for the parser that contains a description of all the properties that the parser supports.</span></span>

<span data-ttu-id="c5ff9-147">**Dati dell'istanza**</span><span class="sxs-lookup"><span data-stu-id="c5ff9-147">**Instance data**</span></span>

<span data-ttu-id="c5ff9-148">I dati dell'istanza sono informazioni passate da un parser a un altro.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-148">Instance data is information that is passed from one parser to another.</span></span> <span data-ttu-id="c5ff9-149">I dati dell'istanza possono essere dati di lunghezza minore o uguale a un \_ ptr DWORD o un puntatore ai dati, ad esempio dati di frame non elaborati, che non devono essere allocati o liberati dal parser.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-149">Instance data can be any data that is less than or equal to a DWORD\_PTR in length, or a pointer to data, such as raw frame data, that does not need to be allocated by or freed by the parser.</span></span> <span data-ttu-id="c5ff9-150">Nel parametro *lpInstData* delle funzioni **AttachProperties** e [RecognizeFrame](recognizeframe.md) Network Monitor fornisce un puntatore ai dati dell'istanza del protocollo precedente.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-150">In the *lpInstData* parameter of the **AttachProperties** and [RecognizeFrame](recognizeframe.md) functions, Network Monitor provides a pointer to the instance data of the previous protocol.</span></span> <span data-ttu-id="c5ff9-151">È possibile impostare i dati dell'istanza per il parser durante l'implementazione di **RecognizeFrame**.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-151">You can set the instance data for your parser during your implementation of **RecognizeFrame**.</span></span>



| <span data-ttu-id="c5ff9-152">Per informazioni su</span><span class="sxs-lookup"><span data-stu-id="c5ff9-152">For information on</span></span>                                          | <span data-ttu-id="c5ff9-153">Vedere</span><span class="sxs-lookup"><span data-stu-id="c5ff9-153">See</span></span>                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="c5ff9-154">Quali sono i parser e come funzionano con Network Monitor.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-154">What parsers are, and how they work with Network Monitor.</span></span>   | [<span data-ttu-id="c5ff9-155">Parser</span><span class="sxs-lookup"><span data-stu-id="c5ff9-155">Parsers</span></span>](parsers.md)                                             |
| <span data-ttu-id="c5ff9-156">Punti di ingresso inclusi nella DLL del parser.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-156">What entry points are included in the parser DLL.</span></span>           | [<span data-ttu-id="c5ff9-157">Architettura DLL parser</span><span class="sxs-lookup"><span data-stu-id="c5ff9-157">Parser DLL Architecture</span></span>](parser-dll-architecture.md)             |
| <span data-ttu-id="c5ff9-158">Come riconoscere i dati.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-158">How to recognize data.</span></span>                                      | [<span data-ttu-id="c5ff9-159">Implementazione di RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="c5ff9-159">Implementing RecognizeFrame</span></span>](implementing-recognizeframe.md)     |
| <span data-ttu-id="c5ff9-160">Come creare un database di proprietà.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-160">How to create a property database.</span></span>                          | [<span data-ttu-id="c5ff9-161">Implementazione del registro</span><span class="sxs-lookup"><span data-stu-id="c5ff9-161">Implementing Register</span></span>](implementing-register.md)                 |
| <span data-ttu-id="c5ff9-162">L'implementazione di **AttachProperties**  include un esempio.</span><span class="sxs-lookup"><span data-stu-id="c5ff9-162">How to implement **AttachProperties**  includes an example.</span></span> | [<span data-ttu-id="c5ff9-163">Implementazione di AttachProperties</span><span class="sxs-lookup"><span data-stu-id="c5ff9-163">Implementing AttachProperties</span></span>](implementing-attachproperties.md) |



 

## <a name="requirements"></a><span data-ttu-id="c5ff9-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c5ff9-164">Requirements</span></span>



| <span data-ttu-id="c5ff9-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5ff9-165">Requirement</span></span> | <span data-ttu-id="c5ff9-166">Valore</span><span class="sxs-lookup"><span data-stu-id="c5ff9-166">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ff9-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5ff9-167">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ff9-168">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c5ff9-168">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="c5ff9-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c5ff9-169">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ff9-170">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="c5ff9-170">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c5ff9-171">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c5ff9-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5ff9-172"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5ff9-172"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5ff9-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c5ff9-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5ff9-174">AttachPropertyInstance</span><span class="sxs-lookup"><span data-stu-id="c5ff9-174">AttachPropertyInstance</span></span>](attachpropertyinstance.md)
</dt> <dt>

[<span data-ttu-id="c5ff9-175">AttachPropertyInstanceEx</span><span class="sxs-lookup"><span data-stu-id="c5ff9-175">AttachPropertyInstanceEx</span></span>](attachpropertyinstanceex.md)
</dt> <dt>

[<span data-ttu-id="c5ff9-176">RecognizeFrame</span><span class="sxs-lookup"><span data-stu-id="c5ff9-176">RecognizeFrame</span></span>](recognizeframe.md)
</dt> </dl>

 

 




