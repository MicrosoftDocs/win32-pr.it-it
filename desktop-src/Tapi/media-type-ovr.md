---
description: Il tipo di supporto (o modalità) di un dispositivo descrive il tipo di informazioni che possono essere scambiate, ad esempio la voce interattiva. Un determinato dispositivo potrebbe essere in grado di gestire un solo tipo di supporto o di gestire un intervallo di tipi.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Tipo supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf79b97adb9df491aef1ff86be62fb838246c85a45b5ce251f5c0e88df5814f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002889"
---
# <a name="media-type"></a>Tipo supporto

Il *tipo di* supporto (o modalità) di un dispositivo descrive il tipo di informazioni che possono essere scambiate, ad esempio la voce interattiva. Un determinato dispositivo potrebbe essere in grado di gestire un solo tipo di supporto o di gestire un intervallo di tipi.

I provider di servizi espongono il tipo di supporto o i tipi supportati dai dispositivi che controllano. Le applicazioni e interrogano il tipo di supporto e quindi usano queste informazioni per selezionare un indirizzo appropriato in cui avviare una sessione. Anche la risposta dell'applicazione a una sessione offerta può essere predicata sul tipo di supporto.

Una determinata sessione di comunicazione, o chiamata, può coinvolgere diversi tipi di supporti. Per altre informazioni, vedere Tipo di supporto per una sessione.

**TAPI 2.x:** Vedere [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **dwAvailableMediaModes** membro della struttura [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) a cui punta *lpAddressCaps*, [Costanti LINEMEDIAMODE \_](./linemediamode--constants.md).

**TAPI 3.x:** Vedere [**ITTerminal::get \_ MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [Costanti TAPIMEDIATYPE \_](tapimediatype--constants.md).
