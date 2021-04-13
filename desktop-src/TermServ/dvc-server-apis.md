---
title: API del server DVC
description: Le API del server del canale virtuale dinamico (DVC) vengono implementate dal server Connessione Desktop remoto (RDC) della connessione.
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bc413cb6bc60f5b6a16f282fe3d4d1aa830272
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399597"
---
# <a name="dvc-server-apis"></a>API del server DVC

Le API del server del canale virtuale dinamico (DVC) vengono implementate dal server Connessione Desktop remoto (RDC) della connessione.

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

## <a name="changes-in-behavior-for-other-server-apis"></a>Modifiche al comportamento per altre API del server

-   L'API server è stata estesa con una chiamata aggiuntiva che apre un canale virtuale dinamico (DVC). La chiamata aggiuntiva viene eseguita utilizzando la funzione [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) .
-   [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    Quando si usa questa API con DVC, viene sempre anteposto i dati letti con [**l' \_ \_ intestazione di Channel PDU**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header). Ciò significa che qualsiasi operazione di lettura deve essere eseguita con almeno il blocco di dati della **\_ \_ lunghezza PDU del canale** passato come buffer di input.

-   [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    Se l'handle di file per DVC viene recuperato chiamando [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) con il parametro *WTSVirtualFileHandle*, verrà applicata la stessa regola. Tutte le letture includeranno [**l' \_ \_ intestazione PDU del canale**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)e il buffer di lettura deve avere una dimensione di lunghezza minima della **\_ PDU \_ del canale** .

 

 