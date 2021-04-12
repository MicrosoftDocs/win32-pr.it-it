---
description: Configurazione
ms.assetid: aba21473-07cc-4de9-a310-ad9b43c133eb
title: Configurazione (Windows e messaggi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac66d2ba25e81582734eb13148d2651b276ea01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233326"
---
# <a name="configuration-windows-and-messages"></a>Configurazione (Windows e messaggi)

*Gli elementi di visualizzazione* sono le parti di una finestra e la visualizzazione visualizzata nella schermata di visualizzazione del sistema. Le *metriche di sistema* sono le dimensioni dei vari elementi di visualizzazione. Le metriche di sistema tipiche includono lo spessore del bordo della finestra, l'altezza dell'icona e così via. Le metriche di sistema descrivono anche altri aspetti del sistema, ad esempio se è installato un mouse, sono supportati caratteri a byte doppio oppure è installata una versione di debug del sistema operativo. La funzione [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) recupera la metrica di sistema specificata.

Le applicazioni possono anche recuperare e impostare il colore degli elementi della finestra, ad esempio i menu, le barre di scorrimento e i pulsanti usando rispettivamente le funzioni [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) e [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) .

La funzione [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) Recupera o imposta diversi attributi di sistema, ad esempio l'ora di doppio clic, il timeout screen saver, lo spessore del bordo della finestra e il modello desktop. Quando un'applicazione usa **SystemParametersInfo** per impostare un parametro, la modifica viene immediatamente svolta. Questa funzione consente inoltre alle applicazioni di aggiornare il profilo utente, pertanto le modifiche apportate al sistema verranno mantenute al riavvio del sistema.

 

 
