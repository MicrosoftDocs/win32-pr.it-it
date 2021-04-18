---
description: Il tipo di indirizzo identifica il formato necessario per un indirizzo. Ad esempio, se il tipo è LINEADDRESSTYPE \_ PhoneNumber, l'indirizzo usato per comporre la sessione deve essere un numero di telefono.
ms.assetid: bea48bde-927a-400a-9a7e-a77e30ba35eb
title: Tipo di indirizzo per una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42499c19a08d67ce2e6e7ea5741053686c32aa6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312734"
---
# <a name="address-type-for-a-session"></a><span data-ttu-id="08d12-104">Tipo di indirizzo per una sessione</span><span class="sxs-lookup"><span data-stu-id="08d12-104">Address Type for a Session</span></span>

<span data-ttu-id="08d12-105">Il [**tipo di indirizzo**](lineaddresstype--constants.md) identifica il formato necessario per un indirizzo.</span><span class="sxs-lookup"><span data-stu-id="08d12-105">The [**address type**](lineaddresstype--constants.md) identifies the format required for an address.</span></span> <span data-ttu-id="08d12-106">Ad esempio, se il tipo è LINEADDRESSTYPE \_ PhoneNumber, l'indirizzo usato per comporre la sessione deve essere un numero di telefono.</span><span class="sxs-lookup"><span data-stu-id="08d12-106">For example, if the type is LINEADDRESSTYPE\_PHONENUMBER, the address used to dial on the session must be a phone number.</span></span>

<span data-ttu-id="08d12-107">Un determinato provider di servizi e dispositivi supporta uno o più tipi di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="08d12-107">A given device and service provider supports one or more address types.</span></span> <span data-ttu-id="08d12-108">Per informazioni su come eseguire il polling di un dispositivo per i formati di indirizzi supportati, vedere [tipi di indirizzi per un dispositivo](address-type-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="08d12-108">See the [address types for a device](address-type-ovr.md) for information on how to poll a device for the address formats it supports.</span></span>

<span data-ttu-id="08d12-109">**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), membro **dwAddressType** di [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span><span class="sxs-lookup"><span data-stu-id="08d12-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwAddressType** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span></span>

<span data-ttu-id="08d12-110">**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), chiamato con il **membro \_ CIL CALLERIDADDRESSTYPE**, **CIL \_ CALLEDIDADDRESSTYPE** o **CIL \_ CONNECTEDIDADDRESSTYPE** di [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="08d12-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with the **CIL\_CALLERIDADDRESSTYPE**, **CIL\_CALLEDIDADDRESSTYPE**, or **CIL\_CONNECTEDIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

 

 
