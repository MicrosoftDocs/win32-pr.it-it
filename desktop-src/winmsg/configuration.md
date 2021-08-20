---
description: Questa sezione di riferimento descrive la configurazione per Windows e Messaggi. Informazioni sugli elementi di visualizzazione e sulle metriche di sistema.
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Configurazione (Windows messaggi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a5c910fd9614d4d0e8fe9f6ba38d9dd59a0fd5649e836c3629427cde5d8617
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028469"
---
# <a name="configuration-windows-and-messages"></a>Configurazione (Windows messaggi)

*Gli elementi* di visualizzazione sono le parti di una finestra e la visualizzazione visualizzata sullo schermo del sistema. *Le metriche di* sistema sono le dimensioni dei vari elementi di visualizzazione. Le metriche di sistema tipiche includono la larghezza del bordo della finestra, l'altezza dell'icona e così via. Le metriche di sistema descrivono anche altri aspetti del sistema, ad esempio se è installato un mouse, sono supportati caratteri a doppio byte o è installata una versione di debug del sistema operativo. La [**funzione GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) recupera la metrica di sistema specificata.

Le applicazioni possono anche recuperare e impostare il colore degli elementi della finestra, ad esempio menu, barre di scorrimento e pulsanti, usando rispettivamente le funzioni [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) e [**SetSysColors.**](/windows/desktop/api/winuser/nf-winuser-setsyscolors)

La [**funzione SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) recupera o imposta vari attributi di sistema, ad esempio l'ora del doppio clic, screen saver timeout, lo spessore del bordo della finestra e il modello del desktop. Quando un'applicazione **usa SystemParametersInfo per** impostare un parametro, la modifica viene apportata immediatamente. Questa funzione consente inoltre alle applicazioni di aggiornare il profilo utente, in modo che le modifiche apportate al sistema verranno mantenute al riavvio del sistema.

 

 
