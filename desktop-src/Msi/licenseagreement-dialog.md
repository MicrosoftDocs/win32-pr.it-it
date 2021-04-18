---
description: Questa finestra di dialogo modale Visualizza il contratto di licenza con l'utente.
ms.assetid: 367fe264-6e08-4b40-b61b-617bb92986b7
title: Finestra di dialogo LicenseAgreement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8876f315787671ee36de42e5b86167659611a77a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307250"
---
# <a name="licenseagreement-dialog"></a>Finestra di dialogo LicenseAgreement

Questa finestra di dialogo modale Visualizza il contratto di licenza con l'utente. In genere, nella finestra di dialogo viene visualizzato il testo dell'accordo utilizzando un [controllo ScrollableText](scrollabletext-control.md) e una coppia di pulsanti di opzione che consentono all'utente di accettare o rifiutare l'accordo. Per motivi legali è consigliabile che nessuno dei pulsanti venga presentato all'utente come già selezionato per impostazione predefinita. In questo modo l'utente deve effettuare una scelta attiva. Gli autori usano in genere un [controllo RadioButtonGroup](radiobuttongroup-control.md) a questo scopo. Si noti tuttavia che lo stato attivo su una finestra di dialogo non viene spostato in un controllo RadioButtonGroup fino a quando non viene selezionato uno dei pulsanti del gruppo.

 

 



