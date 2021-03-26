---
description: Indica se un indirizzo di rete è conforme a un tipo e un formato specificati.
title: Messaggio NCM_GETADDRESS (Shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 733CD62D-614C-4ac2-986D-CCFCFF4B1B4D
api_name:
- NCM_GETADDRESS
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d5effa69a23a61a602efaf1172de09a09889e32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977879"
---
# <a name="ncm_getaddress-message"></a><span data-ttu-id="81ede-103">NCM \_ GETaddress-messaggio</span><span class="sxs-lookup"><span data-stu-id="81ede-103">NCM\_GETADDRESS message</span></span>

<span data-ttu-id="81ede-104">Indica se un indirizzo di rete è conforme a un tipo e un formato specificati.</span><span class="sxs-lookup"><span data-stu-id="81ede-104">Indicates whether a network address conforms to a specified type and format.</span></span>


```C++
NCM_GETADDRESS

    wParam = (WPARAM) (PNC_ADDRESS) pv;

    lParam = 0;            

            
```



## <a name="parameters"></a><span data-ttu-id="81ede-105">Parametri</span><span class="sxs-lookup"><span data-stu-id="81ede-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81ede-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="81ede-106">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="81ede-107">Deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="81ede-107">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="81ede-108">*PV* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="81ede-108">*pv* \[in, out\]</span></span>
</dt> <dd><span data-ttu-id="81ede-109">Puntatore a una struttura di <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> per ricevere le informazioni sugli indirizzi di rete in forma analizzata, se il formato dell'indirizzo e il tipo nel controllo specificato da *HWND* sono convalidati.</span><span class="sxs-lookup"><span data-stu-id="81ede-109">A pointer to an <a href="/windows/win32/api/shellapi/ns-shellapi-nc_address">NC_ADDRESS</a> structure to receive network address information in parsed form, if the address format and type in the control specified by *hwnd* are validated.</span></span> <span data-ttu-id="81ede-110">L'applicazione chiamante è responsabile dell'allocazione della memoria per questa struttura.</span><span class="sxs-lookup"><span data-stu-id="81ede-110">The calling application is responsible for allocating the memory for this structure.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81ede-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="81ede-111">Return value</span></span>

<span data-ttu-id="81ede-112">Restituisce uno dei valori seguenti di tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="81ede-112">Returns one of the following values of type **HRESULT**.</span></span>



| <span data-ttu-id="81ede-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="81ede-113">Return code</span></span>                                                                                                | <span data-ttu-id="81ede-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81ede-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="81ede-115"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="81ede-115"><dt>**E\_INVALIDARG**</dt></span></span> </dl>               | <span data-ttu-id="81ede-116">L'applicazione chiamante non è riuscita ad allocare una struttura dell' [**\_ Indirizzo NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) .</span><span class="sxs-lookup"><span data-stu-id="81ede-116">The calling application failed to allocate a [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure.</span></span><br/> |
| <dl> <span data-ttu-id="81ede-117"><dt>**ERRORE \_ buffer insufficiente \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81ede-117"><dt>**ERROR\_INSUFFICIENT\_BUFFER**</dt></span></span> </dl> | <span data-ttu-id="81ede-118">Il buffer di uscita è troppo piccolo per mantenere l'indirizzo di rete analizzato.</span><span class="sxs-lookup"><span data-stu-id="81ede-118">The out buffer is too small to hold the parsed network address.</span></span><br/>                           |
| <dl> <span data-ttu-id="81ede-119"><dt>**ERRORE \_ parametro non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="81ede-119"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>   | <span data-ttu-id="81ede-120">La stringa dell'indirizzo di rete non è di alcun tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="81ede-120">The network address string is not of any type specified.</span></span><br/>                                  |
| <dl> <span data-ttu-id="81ede-121"><dt>**ERRORE \_ riuscito**</dt></span><span class="sxs-lookup"><span data-stu-id="81ede-121"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>              | <span data-ttu-id="81ede-122">L'operazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="81ede-122">The operation was successful.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="81ede-123"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="81ede-123"><dt>**S\_FALSE**</dt></span></span> </dl>                    | <span data-ttu-id="81ede-124">Nessun indirizzo nel controllo indirizzo di rete da convalidare.</span><span class="sxs-lookup"><span data-stu-id="81ede-124">There is no address in the network address control to validate.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="81ede-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="81ede-125">Remarks</span></span>

<span data-ttu-id="81ede-126">Usare il messaggio **NCM \_ GetAddress** per convalidare un indirizzo di rete in un controllo degli indirizzi di rete rispetto a una maschera di tipo indirizzo di rete preimpostata.</span><span class="sxs-lookup"><span data-stu-id="81ede-126">Use the **NCM\_GETADDRESS** message to validate a network address in a network address control against a preset network address type mask.</span></span> <span data-ttu-id="81ede-127">Per creare un'istanza di, usare la classe **msctls \_ Netaddress** definita in Shellapi. h.</span><span class="sxs-lookup"><span data-stu-id="81ede-127">To instantiate, use the class **msctls\_netaddress** defined in Shellapi.h.</span></span> <span data-ttu-id="81ede-128">Chiamare [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) in fase di esecuzione prima di inviare questo messaggio.</span><span class="sxs-lookup"><span data-stu-id="81ede-128">Call [**InitNetworkAddressControl**](/windows/desktop/api/Shellapi/nf-shellapi-initnetworkaddresscontrol) at run time before sending this message.</span></span> <span data-ttu-id="81ede-129">Viene inizializzata la libreria di controlli comuni che contiene il controllo degli indirizzi di rete.</span><span class="sxs-lookup"><span data-stu-id="81ede-129">This initializes the common controls library that contains the network address control.</span></span>

<span data-ttu-id="81ede-130">Questo messaggio ottiene la stringa dell'indirizzo di rete da un controllo indirizzo di rete, analizza la stringa e controlla se la stringa corrisponde a una maschera di tipo indirizzo di rete.</span><span class="sxs-lookup"><span data-stu-id="81ede-130">This message gets the network address string from a network address control, parses the string, and checks whether the string matches a network address type mask.</span></span> <span data-ttu-id="81ede-131">Se la stringa corrisponde alla maschera, il messaggio restituisce S \_ OK e restituisce la stringa in formato analizzato all'applicazione chiamante (inclusi il numero di porta, la lunghezza del prefisso e altre informazioni sull'indirizzo), usando la struttura dell' [**\_ Indirizzo NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) a cui punta *PV*.</span><span class="sxs-lookup"><span data-stu-id="81ede-131">If the string matches the mask, the message returns S\_OK and returns the string in parsed form to the calling application (including the port number, prefix length, and other address information), using the [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) structure pointed to by *pv*.</span></span> <span data-ttu-id="81ede-132">Questo messaggio restituisce E \_ INVALIDARG se l'applicazione chiamante non riesce ad allocare la struttura a cui punta *PV*.</span><span class="sxs-lookup"><span data-stu-id="81ede-132">This message returns E\_INVALIDARG if the calling application fails to allocate the structure pointed to by *pv*.</span></span>

<span data-ttu-id="81ede-133">Le rappresentazioni di indirizzi IP (Internet Protocol) versioni 4 e 6 (V4/V6) per servizi e reti, oltre ad indirizzi Internet e servizi denominati che usano il formato Domain Name System (DNS) vengono analizzate.</span><span class="sxs-lookup"><span data-stu-id="81ede-133">Representations of Internet Protocol (IP) address versions 4 and 6 (v4/v6) for services and networks, as well as named Internet addresses and services using Domain Name System (DNS) format are parsed.</span></span> <span data-ttu-id="81ede-134">Se la stringa dell'indirizzo di rete rappresenta un nome host (DNS) o un servizio denominato, il valore restituito nel membro **LunghezzaPrefisso** dell' [**\_ Indirizzo NC**](/windows/win32/api/shellapi/ns-shellapi-nc_address) è zero.</span><span class="sxs-lookup"><span data-stu-id="81ede-134">If the network address string represents a named host name (DNS) or service, the value returned in the **PrefixLength** member of [**NC\_ADDRESS**](/windows/win32/api/shellapi/ns-shellapi-nc_address) is zero.</span></span>

<span data-ttu-id="81ede-135">Impostare il tipo di indirizzo di rete mask usando il messaggio [**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md) prima di inviare la macro **NCM \_ GetAddress** .</span><span class="sxs-lookup"><span data-stu-id="81ede-135">Set the network address type mask using the [**NCM\_SETALLOWTYPE**](ncm-setallowtype.md) message before you send the **NCM\_GETADDRESS** macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="81ede-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="81ede-136">Requirements</span></span>



| <span data-ttu-id="81ede-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="81ede-137">Requirement</span></span> | <span data-ttu-id="81ede-138">Valore</span><span class="sxs-lookup"><span data-stu-id="81ede-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="81ede-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81ede-139">Minimum supported client</span></span><br/> | <span data-ttu-id="81ede-140">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="81ede-140">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="81ede-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="81ede-141">Minimum supported server</span></span><br/> | <span data-ttu-id="81ede-142">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="81ede-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="81ede-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="81ede-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="81ede-144"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="81ede-144"><dt>Shellapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81ede-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="81ede-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81ede-146">**NCM \_ GETALLOWTYPE**</span><span class="sxs-lookup"><span data-stu-id="81ede-146">**NCM\_GETALLOWTYPE**</span></span>](ncm-getallowtype.md)
</dt> <dt>

[<span data-ttu-id="81ede-147">**NetAddr \_ GetAddress**</span><span class="sxs-lookup"><span data-stu-id="81ede-147">**NetAddr\_GetAddress**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_getaddress)
</dt> </dl>

 

 




