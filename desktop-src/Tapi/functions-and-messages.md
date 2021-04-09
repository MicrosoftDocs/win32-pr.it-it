---
description: La funzione phoneDevSpecific e il \_ messaggio DEVSPECIFIC Phone associato consentono a un'applicazione di accedere alle funzionalità del telefono specifiche del dispositivo che non sono disponibili tramite i servizi di telefonia comuni per telefoni.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Funzioni e messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f85e2ea57ac11da8150d4d0a183c7c4fd2c88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967467"
---
# <a name="functions-and-messages"></a>Funzioni e messaggi

La funzione [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) e il messaggio [**\_ DEVSPECIFIC Phone**](phone-devspecific.md) associato consentono a un'applicazione di accedere alle funzionalità del telefono specifiche del dispositivo che non sono disponibili tramite i servizi di telefonia comuni per telefoni. In altre parole, **phoneDevSpecific** è la funzione di escape specifica del dispositivo che consente le estensioni dipendenti dal fornitore, mentre Phone \_ DEVSPECIFIC è il messaggio specifico del dispositivo che viene inviato all'applicazione.

Il profilo del parametro della funzione [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) è generico in quanto la minima interpretazione dei parametri viene eseguita da TAPI. L'interpretazione dei parametri è invece definita dal provider di servizi e deve essere riconosciuta da un'applicazione che li utilizza. I parametri vengono semplicemente passati tramite TAPI dall'applicazione al provider di servizi. Un'applicazione che si basa su estensioni specifiche del dispositivo non funziona in genere con altri provider di servizi, ma le applicazioni scritte nei servizi telefonici telefonici comuni funzioneranno con il provider di servizi esteso.

 

 



