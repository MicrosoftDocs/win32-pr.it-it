---
description: Questa sezione di riferimento descrive la configurazione per Windows e Messaggi. Informazioni sugli elementi di visualizzazione e sulle metriche di sistema.
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Configurazione (Windows e messaggi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa516e87aa7d338d4e2fd46a160fcbd6dadb305
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406344"
---
# <a name="configuration-windows-and-messages"></a>Configurazione (Windows e messaggi)

*Gli elementi* di visualizzazione sono le parti di una finestra e la visualizzazione visualizzata sullo schermo del sistema. *Le metriche di* sistema sono le dimensioni dei vari elementi di visualizzazione. Le metriche di sistema tipiche includono la larghezza del bordo della finestra, l'altezza dell'icona e così via. Le metriche di sistema descrivono anche altri aspetti del sistema, ad esempio se è installato un mouse, sono supportati caratteri a doppio byte o è installata una versione di debug del sistema operativo. La [**funzione GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) recupera la metrica di sistema specificata.

Le applicazioni possono anche recuperare e impostare il colore degli elementi della finestra, ad esempio menu, barre di scorrimento e pulsanti, usando rispettivamente le funzioni [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) e [**SetSysColors.**](/windows/desktop/api/winuser/nf-winuser-setsyscolors)

La [**funzione SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) recupera o imposta vari attributi di sistema, ad esempio l'ora del doppio clic, screen saver timeout, lo spessore del bordo della finestra e il modello del desktop. Quando un'applicazione **usa SystemParametersInfo per** impostare un parametro, la modifica viene apportata immediatamente. Questa funzione consente anche alle applicazioni di aggiornare il profilo utente, in modo che le modifiche apportate al sistema verranno mantenute al riavvio del sistema.

 

 
