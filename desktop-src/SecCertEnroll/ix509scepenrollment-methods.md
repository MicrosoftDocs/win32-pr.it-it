---
description: L'interfaccia IX509SCEPEnrollment espone i metodi seguenti.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Metodi IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a33c3bdee14b865211b53649075dec6d4617a4c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314714"
---
# <a name="ix509scepenrollment-methods"></a>Metodi IX509SCEPEnrollment

L'interfaccia [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) espone i metodi seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                              | Descrizione                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Metodo CreateRequestMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | Creare un messaggio di richiesta PKCS10 con una password di verifica. Il messaggio di richiesta si trova in una busta di PKCS7 crittografata con il certificato di crittografia del server SCEP e firmata dal certificato di firma del server.<br/> |
| [**Metodo CreateRetrieveCertificateMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | Recuperare un certificato emesso in precedenza.<br/>                                                                                                                                                                   |
| [**Metodo CreateRetrievePendingMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | Creare un messaggio per il polling del certificato (registrazione manuale).<br/>                                                                                                                                               |
| [**Metodo DeleteRequest**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | Eliminare tutti i certificati o le chiavi create per la richiesta.<br/>                                                                                                                                                    |
| [**Initialize (metodo)**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | Inizializzare l'istanza di in preparazione per una nuova richiesta.<br/>                                                                                                                                                   |
| [**Metodo InitializeForPending**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | Inizializzare l'istanza di per preparare la generazione di un messaggio per recuperare un certificato emesso o per installare una risposta per una richiesta precedente da parte dell'emittente.<br/>                                              |
| [**Metodo ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | Elaborare un messaggio di risposta e restituire la disposizione del messaggio.<br/>                                                                                                                                       |



 

 

 




