---
description: Esistono alcune considerazioni specifiche per i sistemi amministrati in remoto.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Considerazioni sull'amministrazione remota di PAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b3106a02aa4098d2814a955e6582d6e8f1c79f7f161a6875891e13a0db71a7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098591"
---
# <a name="wfp-remote-administration-considerations"></a>Considerazioni sull'amministrazione remota di PAM

Esistono alcune considerazioni specifiche per i sistemi amministrati in remoto. In primo luogo, quando l'installazione del software viene distribuita in remoto (tramite SMS o MSI), sullo schermo di un amministratore connesso localmente (se presente), non al servizio di installazione, vengono visualizzate le finestre di dialogo di errore WFP. In secondo momento, se un amministratore accede in remoto a un server terminal e installa un'applicazione che sostituisce i file di sistema protetti, le finestre di dialogo di errore PAM vengono visualizzate solo nella console principale, non nella finestra remota dell'amministratore.

Per questi motivi, PAM elimina le finestre di dialogo di errore finché un amministratore non esegue l'accesso in locale. Gli amministratori remoti possono trovare gli errori di sostituzione dei file nel registro eventi di sistema.

**Windows Vista e Windows Server 2008:** L'amministrazione remota di PAM non è supportata.

 

 



