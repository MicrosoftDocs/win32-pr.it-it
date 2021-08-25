---
description: L'applicazione deve eseguire l'inventario delle risorse di comunicazione disponibili, quindi inviare una notifica a TAPI sulle risorse che userà e su come le userà.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Inventario delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13436479877f63255ce6132a5907f97a511efea16dd5e21db41b0e41000beb8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773421"
---
# <a name="resource-inventory"></a>Inventario delle risorse

L'applicazione deve eseguire l'inventario delle risorse di comunicazione disponibili, quindi inviare una notifica a TAPI sulle risorse che userà e su come le userà. Per [altre informazioni sui](device-control.md) tipi di risorse e sulle funzionalità a cui un'applicazione può accedere, vedere Controllo dispositivo.

**TAPI 2.x:** Le applicazioni ottengono il numero di righe disponibili quando [**lineInitializeEx restituisce**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) . Possono quindi eseguire [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) in ogni riga, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) per ogni indirizzo e [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) per ogni riga che verrà usata.

**TAPI 3.x:** Le applicazioni [**usano gli indirizzi ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) [**o ITTAPI::get \_ per**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) individuare gli indirizzi disponibili. [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) e [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) forniscono informazioni sui tipi di comunicazione possibili per ogni indirizzo. Se implementato dal provider di servizi, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) consente a un'applicazione di accedere a informazioni e controlli aggiuntivi.

 

 
