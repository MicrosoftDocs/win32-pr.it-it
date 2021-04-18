---
description: Quando un modulo supporta più lingue, è possibile eseguirne il merge nello stesso database di Windows Installer più volte, ma assicurarsi che ogni merge usi una lingua diversa.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Unione di un modulo a più lingue nello stesso pacchetto più volte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52552a68643d52c6aad97ed666b7dc1ae4043fd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315900"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a>Unione di un modulo a più lingue nello stesso pacchetto più volte

Quando un modulo supporta più lingue, è possibile eseguirne il merge nello stesso database di Windows Installer più volte, ma assicurarsi che ogni merge usi una lingua diversa. Prima di ogni Unione, richiedere una lingua diversa dal modulo. Il database con estensione MSI risultante dispone quindi di un record nella [tabella ModuleSignature](modulesignature-table.md) per ogni unione del modulo. I componenti condivisi tra i linguaggi sono disponibili solo una volta nella [tabella dei componenti](component-table.md), ma sono associati a ogni lingua nella [tabella ModuleComponents](modulecomponents-table.md).

Quando si uniscono più lingue di un modulo nello stesso pacchetto, ogni Unione deve soddisfare le stesse restrizioni sulle tabelle codici come moduli a linguaggio singolo. I moduli non possono contenere stringhe in tabelle codici diverse.

Quando si unisce un modulo più volte in un unico file con estensione msi, potrebbe essere necessario modificare l'ordine dei file nella [tabella file](file-table.md) in modo da usare il file con estensione CAB esistente dal modulo direttamente nell'installazione. L'ordine dei file nella tabella file deve corrispondere all'ordine dei file nel file con estensione cab. Quando si unisce un modulo più volte in un database di installazione, la sequenza può essere modificata, perché i file condivisi tra le lingue potrebbero già esistere nel modulo da un'unione precedente e hanno un numero di sequenza relativo diverso.

 

 



