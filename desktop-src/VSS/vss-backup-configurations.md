---
description: Esistono diversi tipi di backup supportati in modo convenzionale&\# 8212; incrementale, differenziale e completo&8212; di cui vss è a conoscenza, nonché una configurazione di backup particolare per \# vss.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Configurazioni di backup vss
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8552bc379be4fc2bf7301043355a1a4417a59154ea15c36061b9cfd13c5d209f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056339"
---
# <a name="vss-backup-configurations"></a>Configurazioni di backup vss

Sono disponibili diversi tipi di backup supportati convenzionalmente, ovvero incrementale, differenziale e completo, di cui VSS è a conoscenza, nonché una configurazione di backup particolare di VSS.

Nella definizione di una configurazione di backup, un richiedente e i writer in un sistema indicano come verranno scritti i dati in un dispositivo di archiviazione, come verrà distribuito il meccanismo di copia shadow e quali informazioni devono essere salvate. L'interazione tra writer e richiedenti è determinata dal tipo di backup che un richiedente vuole eseguire e dai tipi (o schemi) che ogni writer può supportare:

-   [Stato del backup VSS](vss-backup-state.md)
-   [Supporto dello schema di backup del writer](writer-backup-schema-support.md)
-   [Supporto dello schema a livello di file](file-level-schema-support.md)

 

 



