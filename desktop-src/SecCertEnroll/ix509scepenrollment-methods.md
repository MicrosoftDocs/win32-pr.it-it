---
description: L'interfaccia IX509SCEPEnrollment espone i metodi seguenti.
ms.assetid: B45B68D2-A14D-4D14-AF5F-1A1BB9921A0D
title: Metodi IX509SCEPEnrollment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15fc7de6392c49bd38381771956685ba6c8427b3562e7c81c372c1bab61db49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993541"
---
# <a name="ix509scepenrollment-methods"></a>Metodi IX509SCEPEnrollment

[**L'interfaccia IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment) espone i metodi seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                                              | Descrizione                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Metodo CreateRequestMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createrequestmessage)<br/>                         | Creare un messaggio di richiesta PKCS10 con una password di richiesta. Il messaggio di richiesta è in un file PKCS7 in busta crittografato con il certificato di crittografia del server SCEP e firmato dal certificato di firma del server.<br/> |
| [**Metodo CreateRetrieveCertificateMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievecertificatemessage)<br/> | Recuperare un certificato emesso in precedenza.<br/>                                                                                                                                                                   |
| [**Metodo CreateRetrievePendingMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-createretrievependingmessage)<br/>         | Creare un messaggio per il polling dei certificati (registrazione manuale).<br/>                                                                                                                                               |
| [**Metodo DeleteRequest**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-deleterequest)<br/>                                       | Eliminare eventuali certificati o chiavi creati per la richiesta.<br/>                                                                                                                                                    |
| [**Metodo Initialize**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initialize)<br/>                                             | Inizializzare l'istanza in preparazione di una nuova richiesta.<br/>                                                                                                                                                   |
| [**Metodo InitializeForPending**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-initializeforpending)<br/>                         | Inizializzare l'istanza di per preparare la generazione di un messaggio per recuperare un certificato emesso o installare una risposta per una richiesta precedente da parte dell'autorità emittente.<br/>                                              |
| [**Metodo ProcessResponseMessage**](/windows/desktop/api/Certenroll/nf-certenroll-ix509scepenrollment-processresponsemessage)<br/>                     | Elaborare un messaggio di risposta e restituire la disposizione del messaggio.<br/>                                                                                                                                       |



 

 

 




