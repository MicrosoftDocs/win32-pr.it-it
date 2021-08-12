---
description: Limitazioni di sicurezza in modalità gruppo di lavoro
ms.assetid: 05c0aba7-b94b-49d4-a0fc-1ff0a23550b3
title: Limitazioni di sicurezza in modalità gruppo di lavoro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af613b8de16b99090bcdb02bde0015d01312df3d642c895d61ef59ff80873eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546275"
---
# <a name="security-limitations-in-workgroup-mode"></a>Limitazioni di sicurezza in modalità gruppo di lavoro

La [configurazione del gruppo di lavoro](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) accodamento messaggi non consente al servizio componenti in coda COM+ di supportare la sicurezza delle applicazioni. Se Accodamento messaggi è stato installato con la [](specifying-the-authentication-protocol.md) configurazione del gruppo di lavoro, è  necessario disabilitare la sicurezza in ogni applicazione in  coda a cui si accede in questa configurazione selezionando Non autenticare i messaggi nella scheda Accodamento per la finestra di dialogo Proprietà dell'applicazione COM+, usando lo strumento di amministrazione Servizi componenti.  Questa operazione deve essere eseguita solo in una rete attendibile e deve essere eseguita sia nel client che nel server se l'applicazione è già stata esportata.

 

 



