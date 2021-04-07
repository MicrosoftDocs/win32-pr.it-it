---
description: Alcune funzioni di comunicazione possono essere chiamate per un dispositivo tramite la funzione EscapeCommFunction.
ms.assetid: 12b92d4b-04b5-4509-9fad-af23fcfd8857
title: Funzioni estese
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0e57c316b521cbc246e5f31dcfb683238e216e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049240"
---
# <a name="extended-functions"></a>Funzioni estese

Alcune funzioni di comunicazione possono essere chiamate per un dispositivo tramite la funzione [**EscapeCommFunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction) . Questa funzione Invia un codice per indicare al dispositivo di eseguire una funzione estesa. Un'applicazione, ad esempio, può sospendere la trasmissione di caratteri con il codice di interruzione e riprendere la trasmissione con il codice CLRBREAK. Queste operazioni particolari possono essere avviate anche chiamando le funzioni [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) e [**ClearCommBreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak) . **EscapeCommFunction** può essere usato anche per implementare il controllo modem manuale. I codici CLRDTR e SETDTR, ad esempio, possono essere usati per implementare il controllo di flusso DTR manuale (data-ready). Si noti, tuttavia, che si verifica un errore se un processo USA **EscapeCommFunction** per modificare la linea DTR quando il dispositivo è stato configurato per abilitare l'handshake DTR o la riga RTS (request-to-Send) se l'handshake RTS è abilitato.

La funzione [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) consente a un processo di inviare un codice di funzione esteso direttamente a un driver di dispositivo specificato, facendo in modo che il dispositivo esegua una determinata operazione. **DeviceIoControl** fornisce a un dispositivo associato a una risorsa di comunicazione le funzionalità non supportate dalle funzioni standard di comunicazione seriale. Consente a un'applicazione di configurare un dispositivo usando parametri univoci per tale dispositivo e di chiamare qualsiasi funzione specifica del dispositivo.

 

 
