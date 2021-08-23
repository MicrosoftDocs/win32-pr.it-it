---
description: La maggior parte delle operazioni get e set si occupa solo di un componente delle informazioni. La funzione phoneGetStatus restituisce informazioni complete sullo stato di un dispositivo telefonico a un'applicazione.
ms.assetid: ca38396c-6f97-4c1c-99fb-2bd64c74c626
title: Stato (API Di telefonia)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32fd9191d4b1808ca2dc5ff20ce509b58ad27a78a354aeca4ca83f8aa60dafa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118861828"
---
# <a name="status-telephony-api"></a>Stato (API Di telefonia)

La maggior parte delle operazioni get e set si occupa solo di un componente delle informazioni. La [**funzione phoneGetStatus**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatus) restituisce informazioni complete sullo stato di un dispositivo telefonico a un'applicazione.

Come accennato in precedenza, ogni volta che un elemento di stato cambia nel dispositivo telefonico, viene inviato un messaggio [**PHONE \_ STATE**](phone-state.md) alla funzione dell'applicazione. I parametri di questo messaggio includono un handle per il dispositivo telefonico e un'indicazione dell'elemento di stato modificato.

Un'applicazione può [**usare phoneSetStatusMessages**](/windows/desktop/api/Tapi/nf-tapi-phonesetstatusmessages) per selezionare le modifiche di stato specifiche per cui vuole ricevere una notifica. Di conseguenza, [**phoneGetStatusMessages restituisce**](/windows/desktop/api/Tapi/nf-tapi-phonegetstatusmessages) le modifiche di stato per le quali l'applicazione vuole ricevere una notifica.

 

 



