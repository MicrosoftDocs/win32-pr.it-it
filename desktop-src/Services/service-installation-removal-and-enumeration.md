---
description: Un programma di configurazione utilizza la funzione CreateService per installare un nuovo servizio nel database SCM.
ms.assetid: 554b9983-4e49-4b11-b420-a4754123d854
title: Installazione, rimozione ed enumerazione del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1069bba094205efd3257063a89c74326b2806455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751058"
---
# <a name="service-installation-removal-and-enumeration"></a>Installazione, rimozione ed enumerazione del servizio

Un programma di configurazione utilizza la funzione [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) per installare un nuovo servizio nel database SCM. Questa funzione specifica il nome del servizio e fornisce le informazioni di configurazione archiviate nel database. Per una descrizione delle informazioni archiviate nel database per ogni servizio, vedere [database of installato Services](database-of-installed-services.md). Per il codice di esempio, vedere [installazione di un servizio](installing-a-service.md).

Un programma di configurazione utilizza la funzione [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice) per rimuovere un servizio installato dal database. Per ulteriori informazioni, vedere [eliminazione di un servizio](deleting-a-service.md).

Per ottenere il nome del servizio, chiamare la funzione [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea) . Il nome visualizzato del servizio, usato nell'applet del pannello di controllo dei servizi, può essere ottenuto chiamando la funzione [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea) .

Un programma di configurazione del servizio può usare la funzione [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa) per enumerare tutti i servizi e i relativi stati. Può inoltre utilizzare la funzione [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa) per enumerare i servizi che dipendono da un oggetto servizio specificato.

 

 



