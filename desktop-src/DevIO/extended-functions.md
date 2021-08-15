---
description: Alcune funzioni di comunicazione possono essere chiamate per un dispositivo usando la funzione EscapeCommFunction.
ms.assetid: 12b92d4b-04b5-4509-9fad-af23fcfd8857
title: Funzioni estese
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 913feb46f61777bcb07fda1639519c4ef04fcb4905075b1c67955a3e911b9d0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405336"
---
# <a name="extended-functions"></a>Funzioni estese

Alcune funzioni di comunicazione possono essere chiamate per un dispositivo usando la [**funzione EscapeCommFunction.**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction) Questa funzione invia un codice per indirizzare il dispositivo all'esecuzione di una funzione estesa. Ad esempio, un'applicazione può sospendere la trasmissione di caratteri con il codice SETBREAK e riprendere la trasmissione con il codice CLRBREAK. Queste operazioni specifiche possono essere avviate anche chiamando le [**funzioni SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) [**e ClearCommBreak.**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak) **EscapeCommFunction può** essere usato anche per implementare il controllo manuale del modem. Ad esempio, i codici CLRDTR e SETDTR possono essere usati per implementare il controllo di flusso manuale DTR (data-terminal-ready). Si noti, tuttavia, che si verifica un errore se un processo usa **EscapeCommFunction** per modificare la linea DTR quando il dispositivo è stato configurato per abilitare l'handshaking DTR o la riga RTS (richiesta a invio) se l'handshaking RTS è abilitato.

La [**funzione DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) consente a un processo di inviare un codice di funzione esteso direttamente a un driver di dispositivo specificato, causando l'esecuzione di una determinata operazione da parte del dispositivo. **DeviceIoControl offre** a un dispositivo associato a una risorsa di comunicazione funzionalità non supportate dalle funzioni di comunicazione seriale standard. Consente a un'applicazione di configurare un dispositivo usando parametri univoci per tale dispositivo e di chiamare qualsiasi funzione specifica del dispositivo.

 

 
