---
description: TAPI consente di accedere alla visualizzazione di un telefono.
ms.assetid: f6017ecc-b2a0-4a92-8c28-ce7411f8dd84
title: Visualizza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5dd813297c1d4624bb37cea8d833f63bcebeeb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129307"
---
# <a name="display"></a>Visualizza

TAPI consente di accedere alla visualizzazione di un telefono. La visualizzazione viene modellata come area alfanumerica con righe e colonne. Le funzionalità del dispositivo del telefono indicano le dimensioni dello schermo di un telefono come il numero di righe e il numero di colonne. Entrambi questi numeri sono pari a zero se il dispositivo telefonico non dispone di una visualizzazione. Usare [**phoneSetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonesetdisplay) per scrivere informazioni nella visualizzazione di un dispositivo telefonico aperto e [**phoneGetDisplay**](/windows/desktop/api/Tapi/nf-tapi-phonegetdisplay) per recuperare il contenuto corrente della visualizzazione di un telefono.

Quando viene modificata la visualizzazione di un dispositivo telefonico, viene inviato un messaggio di [**\_ stato telefonico**](phone-state.md) alla funzione dell'applicazione per notificare all'applicazione la modifica dello stato. I parametri di questo messaggio forniscono un'indicazione della modifica.

 

 



