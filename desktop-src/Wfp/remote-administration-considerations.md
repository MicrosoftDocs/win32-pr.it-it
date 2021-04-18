---
description: Esistono alcune considerazioni specifiche per i sistemi amministrati in remoto.
ms.assetid: bfdf121e-9b4e-4323-82ec-9bd32531caad
title: Considerazioni sull'amministrazione remota di WFP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bb40776f6b727abb49d7e0685bb12b087ed2bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316018"
---
# <a name="wfp-remote-administration-considerations"></a>Considerazioni sull'amministrazione remota di WFP

Esistono alcune considerazioni specifiche per i sistemi amministrati in remoto. In primo luogo, quando l'installazione del software viene distribuita in modalità remota (tramite SMS o MSI), le finestre di dialogo di errore di WFP vengono visualizzate sullo schermo di un amministratore connesso localmente (se presente) e non del servizio di installazione. In secondo luogo, se un amministratore accede a un server terminal in remoto e installa un'applicazione che sostituisce i file di sistema protetti, le finestre di dialogo di errore WFP vengono visualizzate solo nella console principale, non nella finestra remota dell'amministratore.

Per questi motivi, Pam disattiva le finestre di dialogo di errore fino a quando un amministratore non esegue l'accesso in locale. Gli amministratori remoti possono trovare errori di sostituzione del file nel registro eventi di sistema.

**Windows Vista e Windows Server 2008:** Amministrazione remota WFP non supportata.

 

 



