---
description: Lo stato di installazione di un file complementare dipende non dalle informazioni relative al controllo delle versioni dei file, bensì al controllo delle versioni del padre complementare.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: File complementari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968021"
---
# <a name="companion-files"></a>File complementari

Lo stato di installazione di un file complementare dipende non dalle informazioni relative al controllo delle versioni dei file, bensì al controllo delle versioni del padre complementare. Vedere le [regole di controllo delle versioni dei file](file-versioning-rules.md). Per specificare un file complementare, la chiave primaria dell'elemento padre complementare nella [tabella file](file-table.md) deve essere creata nella colonna Version del record per il complemento.

Nell'esempio seguente, Filea è l'elemento padre complementare e FileB è il file complementare.

[Tabella file](file-table.md) (parziale)



| File  | Versione |
|-------|---------|
| FileA | 1.0.0.0 |
| FileB | FileA   |



 

In questo esempio, lo stato di installazione di FileB dipende dalle [regole di controllo delle versioni dei file](file-versioning-rules.md) e dalle informazioni sul controllo delle versioni per file a. Se il programma di installazione stabilisce che la versione di Filea nel pacchetto deve essere installata su una versione precedente di Filea già esistente nel computer dell'utente, installerà anche FileB dal pacchetto indipendentemente dalla versione di qualsiasi FileB installato.

Si noti che un file che rappresenta il percorso della chiave per il componente non deve essere un file complementare. Questo comporterebbe la logica di controllo delle versioni del file del percorso della chiave determinata dal file padre complementare.

 

 



