---
description: Il tipo di indirizzo del dispositivo descrive le forme di indirizzamento consentite su un indirizzo, ad esempio un numero di telefono o un indirizzo IP.
ms.assetid: b474dfca-c4a6-4aab-a4dd-5aec7be3e02a
title: Tipo di indirizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9438c200c9b09dd4f78342ea18d412eaaf23b646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314642"
---
# <a name="address-type"></a><span data-ttu-id="7cb82-103">Tipo di indirizzo</span><span class="sxs-lookup"><span data-stu-id="7cb82-103">Address Type</span></span>

<span data-ttu-id="7cb82-104">Il tipo di indirizzo del dispositivo descrive le forme di indirizzamento consentite su un indirizzo, ad esempio un numero di telefono o un indirizzo IP.</span><span class="sxs-lookup"><span data-stu-id="7cb82-104">The device address type describes the forms of addressing permissible on an address, such as a phone number or an IP address.</span></span> <span data-ttu-id="7cb82-105">Un determinato dispositivo comprenderà uno o più tipi di indirizzi.</span><span class="sxs-lookup"><span data-stu-id="7cb82-105">A given device will understand one or more address types.</span></span> <span data-ttu-id="7cb82-106">Per un elenco di tipi di indirizzi supportati da TAPI, [vedere \_ costanti LINEADDRESSTYPE](lineaddresstype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="7cb82-106">For a list of address types supported by TAPI, see [LINEADDRESSTYPE\_ Constants](lineaddresstype--constants.md).</span></span> <span data-ttu-id="7cb82-107">La [conversione degli indirizzi](initiate-a-session-ovr.md) può essere usata per convertire un indirizzo da un tipo a un altro.</span><span class="sxs-lookup"><span data-stu-id="7cb82-107">[Address translation](initiate-a-session-ovr.md) may be used to convert an address from one type to another.</span></span>

<span data-ttu-id="7cb82-108">Per informazioni generali sugli indirizzi, vedere [Indirizzo](address-ovr.md) in [categorie di dispositivi](device-categories.md).</span><span class="sxs-lookup"><span data-stu-id="7cb82-108">For general information on addresses, see [Address](address-ovr.md) under [Device Categories](device-categories.md).</span></span>

<span data-ttu-id="7cb82-109">Il [tipo di indirizzo per una sessione](address-type-for-a-session-ovr.md) sarà un subset dei tipi di indirizzi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7cb82-109">The [address type for a session](address-type-for-a-session-ovr.md) will be a subset of the device address types.</span></span>

<span data-ttu-id="7cb82-110">**TAPI 2. x:** Vedere [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) e il membro **dwAddressType** di [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).</span><span class="sxs-lookup"><span data-stu-id="7cb82-110">**TAPI 2.x:** See [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) and the **dwAddressType** member of [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).</span></span>

<span data-ttu-id="7cb82-111">**TAPI 3. x:** Vedere [**ITAddressCapabilities:: Get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability)con *AddressCap* impostato sul membro **AC \_ ADDRESSTYPES** della [**\_ funzionalità Address**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).</span><span class="sxs-lookup"><span data-stu-id="7cb82-111">**TAPI 3.x:** See [**ITAddressCapabilities::get\_AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability), with *AddressCap* set to the **AC\_ADDRESSTYPES** member of [**ADDRESS\_CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).</span></span>

 

 
