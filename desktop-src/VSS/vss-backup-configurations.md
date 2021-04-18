---
description: Esistono diversi tipi di backup supportati convenzionalmente&\# 8212, incrementali, differenziali e completi&\# 8212, che VSS è in grado di riconoscere, oltre a una configurazione di backup peculiare di VSS.
ms.assetid: eddf29bc-221b-4b10-9842-a893b62fa846
title: Configurazioni del backup VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4e4c4f383a208781722053b47ba9ae5bcbf1db7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307167"
---
# <a name="vss-backup-configurations"></a>Configurazioni del backup VSS

Sono disponibili diversi tipi di backup supportati convenzionalmente, ovvero incrementali, differenziali e completi, che VSS è in grado di riconoscere, nonché una configurazione di backup peculiare per VSS.

Quando si definisce una configurazione di backup, un richiedente e i writer in un sistema indicano la modalità di scrittura dei dati in un dispositivo di archiviazione, il modo in cui verrà distribuito il meccanismo di copia shadow e le informazioni da salvare. L'interazione tra writer e richiedenti è determinata dal tipo di backup che un richiedente vuole eseguire e dai tipi (o schemi) che ciascun writer può supportare:

-   [Stato backup VSS](vss-backup-state.md)
-   [Supporto dello schema di backup del writer](writer-backup-schema-support.md)
-   [Supporto dello schema a livello di file](file-level-schema-support.md)

 

 



