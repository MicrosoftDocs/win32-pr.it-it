---
title: Uso Teredo con l'helper IP
description: L'API Internet Protocol Helper (HELPER IP) viene utilizzata da un'applicazione per raccogliere e fornire informazioni importanti sulla configurazione di rete del computer locale.
ms.assetid: 67dbe639-aff5-4628-9471-63f50504962d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e977dd585f9759a4eef93daca55e0ff95abdc98085393577afabb4ae6e5908ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119990801"
---
# <a name="using-teredo-with-ip-helper"></a>Uso Teredo con l'helper IP

L'API Internet [Protocol Helper](/windows/desktop/IpHlp/about-ip-helper) (HELPER IP) viene utilizzata da un'applicazione per raccogliere e fornire informazioni importanti sulla configurazione di rete del computer locale. Quando si opera sulla piattaforma Windows Vista, queste informazioni includono la porta UDP dinamica assegnata all'interfaccia Teredo e le modifiche che possono verificarsi alla porta designata.

Le funzioni seguenti vengono usate dall'API helper IP per facilitare l'uso dell'Teredo interfaccia:

-   [**GetTeredoPort**](/windows/desktop/api/netioapi/nf-netioapi-getteredoport)
-   [**NotifyTeredoPortChange**](/windows/desktop/api/netioapi/nf-netioapi-notifyteredoportchange)
-   [**NotifyStableUnicastIpAddressTable**](/windows/desktop/api/netioapi/nf-netioapi-notifystableunicastipaddresstable)

 

 