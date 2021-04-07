---
description: La maggior parte delle operazioni get e set occupano solo un componente di informazioni. La funzione phoneGetStatus restituisce informazioni complete sullo stato di un dispositivo telefonico a un'applicazione.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: Stato (API di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44a9a93fdd97d32b477545ba0fb9f73f10b45021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881642"
---
# <a name="status-telephony-api"></a>Stato (API di telefonia)

La maggior parte delle operazioni get e set occupano solo un componente di informazioni. La funzione [**phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) restituisce informazioni complete sullo stato di un dispositivo telefonico a un'applicazione.

Come indicato in precedenza, ogni volta che un elemento di stato viene modificato sul dispositivo telefonico, viene inviato un messaggio di [**\_ stato telefonico**](phone-state.md) alla funzione dell'applicazione. I parametri di questo messaggio includono un handle per il dispositivo telefonico e un'indicazione dell'elemento di stato modificato.

Un'applicazione può usare [**phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) per selezionare le modifiche di stato specifiche per le quali si vuole ricevere una notifica. In modo corrispondente, [**phoneGetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) restituisce le modifiche dello stato per le quali l'applicazione vuole ricevere una notifica.

 

 



