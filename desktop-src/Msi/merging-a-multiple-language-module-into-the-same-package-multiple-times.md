---
description: Quando un modulo supporta più lingue, è possibile unirlo nello stesso database del programma di installazione di Windows più volte, ma assicurarsi che ogni unione usi una lingua diversa.
ms.assetid: 816b1f52-1ca2-4332-9a9b-462ea372c3bb
title: Unione di un modulo in più lingue nello stesso pacchetto più volte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a96f3830b2caa4069eddc69b0b68de1deff35d00c5b4fdb81d4d21d4355bd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129261"
---
# <a name="merging-a-multiple-language-module-into-the-same-package-multiple-times"></a>Unione di un modulo in più lingue nello stesso pacchetto più volte

Quando un modulo supporta più lingue, è possibile unirlo nello stesso database del programma di installazione di Windows più volte, ma assicurarsi che ogni unione usi una lingua diversa. Prima di ogni unione, richiedere una lingua diversa dal modulo. Il database .msi ha quindi un record nella [tabella ModuleSignature](modulesignature-table.md) per ogni unione del modulo. I componenti condivisi tra le lingue esistono una sola volta nella tabella [dei](component-table.md)componenti , ma sono associati a ogni lingua nella [tabella ModuleComponents](modulecomponents-table.md).

Quando si uniscono più linguaggi di un modulo nello stesso pacchetto, ogni unione deve soddisfare le stesse restrizioni nelle code pages dei moduli a linguaggio singolo. I moduli non possono contenere stringhe in diverse code pages.

Quando si unirà un modulo più volte in un singolo file .msi, potrebbe essere necessario modificare l'ordine dei file nella tabella [file](file-table.md) per usare il .cab esistente dal modulo direttamente nell'installazione. L'ordine dei file nella tabella file deve corrispondere all'ordine dei file nel .cab. Quando un modulo viene unito più volte in un database di installazione, la sequenza può essere modificata, perché i file condivisi tra le lingue potrebbero essere già presenti nel modulo da un'unione precedente e hanno un numero di sequenza relativo diverso.

 

 



