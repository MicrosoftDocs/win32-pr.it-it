---
description: La funzione phoneDevSpecific e il messaggio PHONE DEVSPECIFIC associato consentono a un'applicazione di accedere alle funzionalità del telefono specifiche del dispositivo che non sono disponibili tramite i servizi di \_ telefonia comuni per i telefoni.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Funzioni e messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cabdc271548e42b20de695296321f5f5ab0fdbe45a246be2b7ccb1993ee5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660736"
---
# <a name="functions-and-messages"></a>Funzioni e messaggi

La [**funzione phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) e il messaggio [**PHONE \_ DEVSPECIFIC**](phone-devspecific.md) associato consentono a un'applicazione di accedere alle funzionalità del telefono specifiche del dispositivo che non sono disponibili tramite i servizi di telefonia comuni per i telefoni. In altre parole, **phoneDevSpecific** è la funzione di escape specifica del dispositivo che consente estensioni dipendenti dal fornitore e PHONE DEVSPECIFIC è il messaggio specifico del dispositivo inviato \_ all'applicazione.

Il profilo dei parametri della [**funzione phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) è generico in questa piccola interpretazione dei parametri effettuata da TAPI. L'interpretazione dei parametri è invece definita dal provider di servizi e deve essere compresa da un'applicazione che li usa. I parametri vengono semplicemente passati tramite TAPI dall'applicazione al provider di servizi. Un'applicazione basata su estensioni specifiche del dispositivo in genere non funzionerà con altri provider di servizi, ma le applicazioni scritte nei servizi telefonici comuni funzionano con il provider di servizi estesi.

 

 



