---
title: opzione/Protocol
description: L'opzione/Protocol Specifica il protocollo wire supportato dallo stub generato.
ms.assetid: b565b30c-72e5-442b-9588-324b9041524b
keywords:
- /Protocol switch MIDL
topic_type:
- apiref
api_name:
- /protocol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9770fa94d010e21dcbd2a5574a0cffe29273a23
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334660"
---
# <a name="protocol-switch"></a><span data-ttu-id="c29f3-104">opzione/Protocol</span><span class="sxs-lookup"><span data-stu-id="c29f3-104">/protocol switch</span></span>

<span data-ttu-id="c29f3-105">L'opzione **/Protocol** specifica il protocollo wire supportato dallo stub generato.</span><span class="sxs-lookup"><span data-stu-id="c29f3-105">The **/protocol** switch specifies which wire protocol is supported by the generated stub.</span></span>

``` syntax
midl /protocol (dce | ndr64 | all)
```

## <a name="switch-options"></a><span data-ttu-id="c29f3-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="c29f3-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="dce"></span><span id="DCE"></span>

<span data-ttu-id="c29f3-107"><span id="dce"></span><span id="DCE"></span>DCE \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="c29f3-107"><span id="dce"></span><span id="DCE"></span>\*\*\*\*dce\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="c29f3-108">Lo stub generato supporta solo il protocollo DCE.</span><span class="sxs-lookup"><span data-stu-id="c29f3-108">The generated stub supports DCE protocol only.</span></span>

</dd> <dt>

<span id="ndr64"></span><span id="NDR64"></span>

<span data-ttu-id="c29f3-109"><span id="ndr64"></span><span id="NDR64"></span>ndr64\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c29f3-109"><span id="ndr64"></span><span id="NDR64"></span>\*\*\*\*ndr64\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="c29f3-110">Lo stub generato supporta solo il protocollo Microsoft NDR64.</span><span class="sxs-lookup"><span data-stu-id="c29f3-110">The generated stub supports Microsoft NDR64 protocol only.</span></span>

</dd> <dt>

<span id="all"></span><span id="ALL"></span>

<span data-ttu-id="c29f3-111"><span id="all"></span><span id="ALL"></span>tutti i \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="c29f3-111"><span id="all"></span><span id="ALL"></span>\*\*\*\*all\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="c29f3-112">Lo stub generato supporta tutti i protocolli disponibili per un determinato ambiente.</span><span class="sxs-lookup"><span data-stu-id="c29f3-112">The generated stub supports all available protocols for a given environment.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c29f3-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c29f3-113">Remarks</span></span>

<span data-ttu-id="c29f3-114">RPC esegue il marshalling e l'unmarshalling dei dati in base a un protocollo di transito rigido, detto anche sintassi di trasferimento, che definisce la rappresentazione Wire di dati, ad esempio l'ordine in cui i membri dati vengono sottoposti a marshalling, l'allineamento dei dati in transito, informazioni aggiuntive incluse con i dati, tra gli altri.</span><span class="sxs-lookup"><span data-stu-id="c29f3-114">RPC marshals and unmarshals data according to a strict wire protocol, also called transfer syntax, that defines data wire representation such as the order in which data members are marshaled, the alignment of data on the wire, additional information included with the data, among others.</span></span> <span data-ttu-id="c29f3-115">Microsoft RPC è compatibile con il protocollo OSF DCE (Network Data rappresentazione).</span><span class="sxs-lookup"><span data-stu-id="c29f3-115">Microsoft RPC is compatible with OSF DCE's NDR (network data representation) protocol.</span></span> <span data-ttu-id="c29f3-116">Nella versione a 64 bit di Windows XP, Microsoft introduce un protocollo sperimentale NDR64 ottimizzato per il trasferimento dei dati a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="c29f3-116">In the 64-bit release of Windows XP, Microsoft introduces an experimental protocol NDR64 that is optimized for transferring 64-bit data.</span></span> <span data-ttu-id="c29f3-117">NDR64 non è compatibile con le versioni precedenti del protocollo DCE.</span><span class="sxs-lookup"><span data-stu-id="c29f3-117">NDR64 is not backward compatible with the DCE protocol.</span></span>

<span data-ttu-id="c29f3-118">Il protocollo **DCE** è compatibile con la sintassi di trasferimento NDR di OSF DCE.</span><span class="sxs-lookup"><span data-stu-id="c29f3-118">The **dce** protocol is compatible with OSF DCE's NDR transfer syntax.</span></span> <span data-ttu-id="c29f3-119">Questo protocollo è ottimizzato per il trasferimento di dati a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="c29f3-119">This protocol is optimized for transferring 32-bit data.</span></span>

<span data-ttu-id="c29f3-120">Il protocollo **ndr64** è attualmente supportato solo se usato in combinazione con l'opzione [**/Win64**](-win64.md) .</span><span class="sxs-lookup"><span data-stu-id="c29f3-120">The **ndr64** protocol is currently supported only when used in conjunction with the [**/win64**](-win64.md) switch.</span></span> <span data-ttu-id="c29f3-121">Se un client solo ndr64 tenta di connettersi a un server solo DCE, o viceversa, la chiamata viene rifiutata con la \_ \_ transazione SYN non supportata di RPC \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c29f3-121">If a ndr64 only client tries to connect to a dce-only server, or vice versa, the call is rejected with RPC\_S\_UNSUPPORTED\_TRANS\_SYN.</span></span>

<span data-ttu-id="c29f3-122">L'opzione **All** crea uno stub che può utilizzare qualsiasi protocollo disponibile.</span><span class="sxs-lookup"><span data-stu-id="c29f3-122">The **all** option creates a stub that may use any available protocol.</span></span> <span data-ttu-id="c29f3-123">Per gli stub a 32 bit, l'unico protocollo attualmente disponibile è DCE.</span><span class="sxs-lookup"><span data-stu-id="c29f3-123">For 32-bit stubs, the only protocol currently available is DCE.</span></span> <span data-ttu-id="c29f3-124">Per gli stub a 64 bit creati con l'opzione [**/Win64**](-win64.md) , sono disponibili sia DCE che NDR64.</span><span class="sxs-lookup"><span data-stu-id="c29f3-124">For 64-bit stubs, created using the [**/win64**](-win64.md) switch, both DCE and NDR64 are available.</span></span>

## <a name="examples"></a><span data-ttu-id="c29f3-125">Esempio</span><span class="sxs-lookup"><span data-stu-id="c29f3-125">Examples</span></span>

<span data-ttu-id="c29f3-126">**MIDL/Protocol all/Win64 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="c29f3-126">**midl /protocol all /win64 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c29f3-127">Vedere anche</span><span class="sxs-lookup"><span data-stu-id="c29f3-127">See also</span></span>

<dl> <dt>

[**/<system>**](-system-.md)
</dt> </dl>

 

 




