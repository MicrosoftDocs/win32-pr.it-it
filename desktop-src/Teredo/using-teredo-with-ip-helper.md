---
title: Uso di Teredo con helper IP
description: L'API helper protocollo Internet (helper IP) viene utilizzata da un'applicazione per raccogliere e fornire informazioni importanti sulla configurazione di rete del computer locale.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5936ce9987262fe24cfd6cf718a426b6123b89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728479"
---
# <a name="using-teredo-with-ip-helper"></a>Uso di Teredo con helper IP

L'API [Helper protocollo Internet](/windows/desktop/IpHlp/about-ip-helper) (helper IP) viene utilizzata da un'applicazione per raccogliere e fornire informazioni importanti sulla configurazione di rete del computer locale. Quando si opera sulla piattaforma Windows Vista, queste informazioni includono la porta UDP dinamica assegnata all'interfaccia Teredo e le modifiche che possono verificarsi nella porta designata.

Le funzioni seguenti vengono utilizzate dall'API helper IP per semplificare l'utilizzo dell'interfaccia Teredo:

-   [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 