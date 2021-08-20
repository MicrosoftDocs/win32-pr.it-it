---
description: Lo stato di installazione di un file complementare non dipende dalle proprie informazioni sul controllo delle versioni dei file, ma dal controllo delle versioni del relativo elemento padre complementare.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: File complementari
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7d35aa89e216df4e17c84fb15c9c1f19908a74e9c1d14113da4df2128cdfb87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145100"
---
# <a name="companion-files"></a>File complementari

Lo stato di installazione di un file complementare non dipende dalle proprie informazioni sul controllo delle versioni dei file, ma dal controllo delle versioni del relativo elemento padre complementare. Vedere Regole [di controllo delle versioni dei file](file-versioning-rules.md). Per specificare un file complementare, è necessario creare la chiave primaria del padre complementare nella tabella [File](file-table.md) nella colonna Versione del record per il file complementare.

Nell'esempio seguente FileA è l'elemento padre complementare e FileB è il file complementare.

[Tabella file](file-table.md) (parziale)



| File  | Versione |
|-------|---------|
| FileA | 1.0.0.0 |
| FileB | FileA   |



 

In questo esempio lo stato di installazione di FileB dipende dalle regole di controllo delle versioni dei [file](file-versioning-rules.md) e dalle informazioni sul controllo delle versioni per FileA. Se il programma di installazione determina che la versione di FileA nel pacchetto deve essere installata su una versione precedente di FileA già esistente nel computer dell'utente, installerà anche FileB dal pacchetto indipendentemente dalla versione di qualsiasi FileB installato.

Si noti che un file che rappresenta il percorso della chiave per il componente non deve essere un file complementare. In questo modo la logica di controllo delle versioni del file del percorso della chiave viene determinata dal file padre complementare.

 

 



