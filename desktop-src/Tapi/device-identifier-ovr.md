---
description: Un ID dispositivo è un identificatore indipendente dall'applicazione per un dispositivo di comunicazione specifico.
ms.assetid: c7ca72a6-97fa-441f-92ce-a4c77a53765c
title: Identificatore dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19078b7d2774fb2b71d951fade9c7a560a597a188ac4d87982ee2a6f2bfc9416
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117945999"
---
# <a name="device-identifier"></a>Identificatore dispositivo

Un *ID dispositivo* è un identificatore indipendente dall'applicazione per un dispositivo di comunicazione specifico. È in genere necessario solo quando un'applicazione TAPI deve consegnare parte dell'elaborazione che interessa in una sessione di comunicazione alle funzioni di un'API diversa. Ad esempio, le applicazioni TAPI 2.2 potrebbero non essere in grado di accedere direttamente a un flusso multimediale e potrebbero usare l'API Wave.

**TAPI 2.x:** Vedere [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).

**TAPI 3.x:** Vedere [**ITAddressCapabilities::get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* impostato sul membro **AC \_ PERMANENTDEVICEID** [**di ADDRESS \_ CAPABILITY**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).

 

 
