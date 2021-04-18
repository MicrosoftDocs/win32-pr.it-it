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
# <a name="address-type"></a>Tipo di indirizzo

Il tipo di indirizzo del dispositivo descrive le forme di indirizzamento consentite su un indirizzo, ad esempio un numero di telefono o un indirizzo IP. Un determinato dispositivo comprenderà uno o più tipi di indirizzi. Per un elenco di tipi di indirizzi supportati da TAPI, [vedere \_ costanti LINEADDRESSTYPE](lineaddresstype--constants.md). La [conversione degli indirizzi](initiate-a-session-ovr.md) può essere usata per convertire un indirizzo da un tipo a un altro.

Per informazioni generali sugli indirizzi, vedere [Indirizzo](address-ovr.md) in [categorie di dispositivi](device-categories.md).

Il [tipo di indirizzo per una sessione](address-type-for-a-session-ovr.md) sarà un subset dei tipi di indirizzi del dispositivo.

**TAPI 2. x:** Vedere [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) e il membro **dwAddressType** di [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps).

**TAPI 3. x:** Vedere [**ITAddressCapabilities:: Get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability)con *AddressCap* impostato sul membro **AC \_ ADDRESSTYPES** della [**\_ funzionalità Address**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability).

 

 
