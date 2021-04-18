---
description: Il tipo di supporto (o modalità) di un dispositivo descrive il tipo di informazioni che possono essere scambiate, ad esempio la voce interattiva. Un determinato dispositivo può essere in grado di gestire un solo tipo di supporto oppure può essere in grado di gestire un intervallo di tipi.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Tipo supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369954a4b0d1f78e12f6ea42bcc2ec61ca425012
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320599"
---
# <a name="media-type"></a>Tipo supporto

Il *tipo di supporto* (o modalità) di un dispositivo descrive il tipo di informazioni che possono essere scambiate, ad esempio la voce interattiva. Un determinato dispositivo può essere in grado di gestire un solo tipo di supporto oppure può essere in grado di gestire un intervallo di tipi.

I provider di servizi espongono il tipo o i tipi di supporto supportati dai dispositivi che controllano. Le applicazioni eseguono una query per il tipo di supporto e quindi utilizzano queste informazioni per selezionare un indirizzo appropriato su cui avviare una sessione. La risposta dell'applicazione a una sessione offerta può essere predicata anche per il tipo di supporto.

Una determinata sessione di comunicazione, o chiamata, può coinvolgere diversi tipi di supporto. Per ulteriori informazioni, vedere tipo di supporto per una sessione.

**TAPI 2. x:** Vedere [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), membro **DwAvailableMediaModes** della struttura [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) a cui puntano le [ \_ costanti](./linemediamode--constants.md) *lpAddressCaps*, LINEMEDIAMODE.

**TAPI 3. x:** Vedere [**ITTerminal:: Get \_ mediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE \_ costanti](tapimediatype--constants.md).
