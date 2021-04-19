---
description: L'applicazione deve eseguire l'inventario delle risorse di comunicazione disponibili, quindi notificare a TAPI informazioni sulle risorse che utilizzeranno e sul modo in cui vengono usate.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Inventario delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e743934f225fa4f932460eba0bbf895cc1bc21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311877"
---
# <a name="resource-inventory"></a>Inventario delle risorse

L'applicazione deve eseguire l'inventario delle risorse di comunicazione disponibili, quindi notificare a TAPI informazioni sulle risorse che utilizzeranno e sul modo in cui vengono usate. Vedere [controllo del dispositivo](device-control.md) per informazioni aggiuntive sui tipi di risorse e funzionalità a cui un'applicazione può accedere.

**TAPI 2. x:** Le applicazioni ottengono il numero di righe disponibili quando [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) restituisce. Possono quindi eseguire [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) su ogni riga, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) per ogni indirizzo e [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) per ogni riga che verrà usata.

**TAPI 3. x:** Le applicazioni usano gli indirizzi [**ITTAPI:: EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) o [**ITTAPI \_ :: Get**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) per individuare gli indirizzi disponibili. [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) e [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) forniscono informazioni sui tipi di comunicazione possibili per ogni indirizzo. Se implementato dal provider di servizi, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) consente a un'applicazione di accedere a informazioni e controlli aggiuntivi.

 

 
