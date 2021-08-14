---
title: API server DVC
description: Le API del server DVC (Dynamic Virtual Channel) vengono implementate dal server Connessione Desktop remoto (RDC) della connessione.
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f43ab4032e4500732e2f9ee6cfa9a2c17f8b1892e55973ba633758792f00bf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353974"
---
# <a name="dvc-server-apis"></a>API server DVC

Le API del server DVC (Dynamic Virtual Channel) vengono implementate dal server Connessione Desktop remoto (RDC) della connessione.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[**IWTSServerChannel**](iwtsserverchannel.md)
</dt> <dd>

Questa interfaccia non è supportata.

</dd> <dt>

[**IWTSServerChannelManager**](iwtsserverchannelmanager.md)
</dt> <dd>

Questa interfaccia non è supportata.

</dd> <dt>

[**TPriority**](tpriority.md)
</dt> <dd>

Questa enumerazione non viene utilizzata.

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a>Modifiche del comportamento per altre API server

-   L'API del server è stata estesa con una chiamata aggiuntiva che apre un canale virtuale dinamico (DVC). La chiamata aggiuntiva viene effettuata usando [**la funzione WTSVirtualChannelOpenEx.**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex)
-   [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    Quando si usa questa API con DVC, verranno sempre anteposti i dati letti con [**CHANNEL \_ PDU \_ HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header). Ciò significa che tutte le operazioni di lettura devono essere eseguite con almeno il blocco di dati **\_ CHANNEL PDU \_ LENGTH** passato come buffer di input.

-   [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    Se l'handle di file per la DVC viene recuperato chiamando [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) con il *parametro WTSVirtualFileHandle*, verrà applicata la stessa regola. Tutte le operazioni di lettura includeranno [**CHANNEL \_ PDU \_ HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)e il buffer di lettura deve avere almeno la dimensione **CHANNEL \_ PDU \_ LENGTH.**

 

 