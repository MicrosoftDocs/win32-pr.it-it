---
title: Creazione di una finestra di dialogo per la selezione di un formato per la registrazione
description: Creazione di una finestra di dialogo per la selezione di un formato per la registrazione
ms.assetid: e94ca8da-4ee6-4362-a144-27b86f2cadac
keywords:
- Gestione compressione audio,creazione di finestre di dialogo
- ACM (Audio Compression Manager), creazione di finestre di dialogo
- Esempi di ACM, creazione di finestre di dialogo
- creazione di finestre di dialogo
- Funzione acmFormatChoose
- gestione compressione audio,selezione del formato per la ricodezione
- ACM (Audio Compression Manager), selezione del formato per la ricodezione
- Esempi di ACM, selezione del formato per la ricodezione
- selezione del formato per la ricodezione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4650732e290b626eb26cd2eea321124f16b5572a7660aabf09bbe3740934e52d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037681"
---
# <a name="producing-a-dialog-box-for-selecting-a-format-for-recording"></a>Creazione di una finestra di dialogo per la selezione di un formato per la registrazione

Un'applicazione può consentire all'utente di selezionare un formato per il quale un dispositivo audio waveform installato fornisce supporto nativo. Ad esempio, è possibile che un editor audio-forma d'onda registri nuovi dati audio-forma d'onda senza usare un acm o un decompressore per fornire un livello di traslazione. A tale scopo, usare la funzione [**acmFormatChoose,**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) specificando i flag ACM \_ FORMATENUMF HARDWARE e \_ ACM FORMATENUMF INPUT nel membro \_ \_ **fdwEnum** della [**struttura ACMFORMATCHOOSE.**](/windows/win32/api/msacm/ns-msacm-acmformatchoose)

 

 




