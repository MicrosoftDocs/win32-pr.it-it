---
description: Il sistema utilizza le informazioni di configurazione per determinare come avviare il servizio.
ms.assetid: fc8c631e-076c-4745-8db0-90f46a202e6a
title: Service Configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f64b5cef835e1c7efef10c12555c81c132e707c8d1fb2814a7fcb95cf6d71c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889081"
---
# <a name="service-configuration"></a>Service Configuration

Il sistema utilizza le informazioni di configurazione per determinare come avviare il servizio. Le informazioni di configurazione includono anche il nome visualizzato del servizio e la relativa descrizione. Ad esempio, per il servizio DHCP, è possibile usare il nome visualizzato "Dynamic Host Configuration Protocol Service" e la descrizione "Fornisce gli indirizzi Internet per il computer nella rete".

Per modificare le informazioni di configurazione per un oggetto servizio, un programma di configurazione usa la [**funzione ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) [**o ChangeServiceConfig2.**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) Per un esempio, vedere [Modifica di una configurazione del servizio.](changing-a-service-configuration.md)

Per recuperare le informazioni di configurazione per un oggetto servizio, il programma di configurazione usa la [**funzione QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga) o [**QueryServiceConfig2.**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) Per un esempio, vedere [Esecuzione di query sulla configurazione di un servizio.](querying-a-service-s-configuration.md)

Le funzioni di configurazione del servizio [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a) e [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a) supportano l'uso di trigger per controllare l'avvio del servizio.

Per modificare il descrittore di sicurezza per un oggetto SCManager o un oggetto servizio, un programma di configurazione usa la [**funzione SetServiceObjectSecurity.**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity) Per recuperare una copia del descrittore di sicurezza, il programma di configurazione usa la [**funzione QueryServiceObjectSecurity.**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Configurazione di un servizio tramite SC](configuring-a-service-using-sc.md)
</dt> </dl>

 

 
