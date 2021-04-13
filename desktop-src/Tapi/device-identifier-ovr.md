---
description: Un ID dispositivo è un identificatore indipendente dall'applicazione per un dispositivo di comunicazione specifico.
ms.assetid: c7ca72a6-97fa-441f-92ce-a4c77a53765c
title: Identificatore dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aeb9c88820ecfe26d3ecd971489d709a34af10f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529077"
---
# <a name="device-identifier"></a>Identificatore dispositivo

Un *ID dispositivo* è un identificatore indipendente dall'applicazione per un dispositivo di comunicazione specifico. È in genere necessario solo quando un'applicazione TAPI deve passare parte dell'elaborazione che interessa una sessione di comunicazione con le funzioni di un'API diversa. Ad esempio, le applicazioni TAPI 2,2 potrebbero non essere in grado di accedere direttamente a un flusso multimediale e potrebbero usare l'API Wave.

**TAPI 2. x:** Vedere [**lineGetID**](/windows/win32/api/tapi/nf-tapi-linegetid).

**TAPI 3. x:** Vedere [**ITAddressCapabilities:: Get \_ AddressCapability**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapability) (*AddressCap* impostato sul membro **AC \_ PERMANENTDEVICEID** della [**\_ funzionalità Address**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_capability)).

 

 
