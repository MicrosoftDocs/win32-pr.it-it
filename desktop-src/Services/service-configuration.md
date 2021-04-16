---
description: Il sistema utilizza le informazioni di configurazione per determinare come avviare il servizio.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Service Configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5019469e17fdd0807aa101c7d1e4d6f6019da783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525824"
---
# <a name="service-configuration"></a>Service Configuration

Il sistema utilizza le informazioni di configurazione per determinare come avviare il servizio. Le informazioni di configurazione includono anche il nome visualizzato del servizio e la relativa descrizione. Per il servizio DHCP, ad esempio, è possibile usare il nome visualizzato "servizio Dynamic Host Configuration Protocol" e la descrizione "fornisce indirizzi Internet per il computer nella rete".

Per modificare le informazioni di configurazione per un oggetto servizio, un programma di configurazione utilizza la funzione [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) o [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) . Per un esempio, vedere [modifica di una configurazione del servizio](changing-a-service-configuration.md).

Per recuperare le informazioni di configurazione per un oggetto servizio, il programma di configurazione utilizza la funzione [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) o [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) . Per un esempio, vedere [esecuzione di query sulla configurazione di un servizio](querying-a-service-s-configuration.md).

Le funzioni di configurazione del servizio [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) supportano l'utilizzo di trigger per controllare l'avvio del servizio.

Per modificare il descrittore di sicurezza per un oggetto SCManager o un oggetto servizio, un programma di configurazione utilizza la funzione [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) . Per recuperare una copia del descrittore di sicurezza, il programma di configurazione utilizza la funzione [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione di un servizio con SC](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
