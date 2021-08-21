---
description: Un programma di configurazione usa la funzione CreateService per installare un nuovo servizio nel database SCM.
ms.assetid: 554b9983-4e49-4b11-b420-a4754123d854
title: Installazione, rimozione ed enumerazione del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d285c87d7c331135b6991899200fd77a080f439d590880473293772dadbb2c21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967442"
---
# <a name="service-installation-removal-and-enumeration"></a>Installazione, rimozione ed enumerazione del servizio

Un programma di configurazione usa [**la funzione CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) per installare un nuovo servizio nel database SCM. Questa funzione specifica il nome del servizio e fornisce informazioni di configurazione archiviate nel database. Per una descrizione delle informazioni archiviate nel database per ogni servizio, vedere [Database dei servizi installati](database-of-installed-services.md). Per il codice di esempio, [vedere Installazione di un servizio](installing-a-service.md).

Un programma di configurazione usa [**la funzione DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) per rimuovere un servizio installato dal database. Per altre informazioni, vedere [Eliminazione di un servizio](deleting-a-service.md).

Per ottenere il nome del servizio, chiamare la [**funzione GetServiceKeyName.**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) Il nome visualizzato del servizio, usato nell'applet del pannello di controllo Servizi, può essere ottenuto chiamando la [**funzione GetServiceDisplayName.**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea)

Un programma di configurazione del servizio può usare la [**funzione EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) per enumerare tutti i servizi e i relativi stati. Può anche usare la [**funzione EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) per enumerare i servizi dipendenti da un oggetto servizio specificato.

 

 



