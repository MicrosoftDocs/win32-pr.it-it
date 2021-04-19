---
description: Il livello dati contiene spesso principalmente informazioni statiche&\# 8212; le informazioni sono persistenti su supporti durevoli.
ms.assetid: d2bce8b6-1f88-4e4a-bb08-fc7ee4c039da
title: Ottimizzare le chiamate tra la logica di business e i dati COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3346f628344e7505fde03c3a64b7420d199312ee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304818"
---
# <a name="optimizing-interactions-between-the-com-business-logic-tier-and-the-data-tier"></a>Ottimizzazione delle interazioni tra il livello di logica di business COM+ e il livello dati

Il livello dati contiene spesso principalmente informazioni statiche, ovvero informazioni persistenti su supporti durevoli. Poiché questo livello comprende informazioni principalmente statiche, richiede un'analisi approfondita dei potenziali colli di bottiglia. Oltre alla possibilità ovvia di colli di bottiglia della connessione, le aree sensibili possono essere causate dai record a cui si accede di frequente, dai metodi di accesso ai dati non efficienti e dalla necessità di coordinare l'accesso ai sistemi legacy.

## <a name="connecting-to-the-data-tier"></a>Connessione al livello dati

Due considerazioni rivestono un ruolo importante nella progettazione di un livello dati per un'applicazione COM+: il pool di connessioni e l' [attivazione JIT (just-in-Time) com+](com--just-in-time-activation.md)e l'utilizzo di DSN. I componenti che effettuano connessioni al livello dati devono utilizzare il [pool di oggetti com+](com--object-pooling.md) impostato sul componente.

Quando si creano i DSN, utilizzare le stringhe del costruttore di oggetti specificate sul componente anziché creare un DSN di file. I DSN di file sono più lenti rispetto a una connessione utilizzando una stringa del costruttore di oggetti. È possibile specificare stringhe del costruttore di oggetti nella finestra delle proprietà del componente. Per altre informazioni, vedere [stringhe del costruttore di oggetti com+](com--object-constructor-strings.md).

Se si utilizzano componenti per accedere a un database di SQL Server, utilizzare il pool di oggetti COM+ anziché il pool di connessioni SQL.

Se il componente usa ADO per recuperare più recordset, stabilire più connessioni per il componente. Quando ADO recupera più recordset, crea più connessioni in background se non vengono create. Se vengono create, è possibile raggrupparle e avere maggiore controllo sul numero di connessioni usate.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Ottimizzazione delle interazioni tra il livello di logica di business COM+ e il livello di presentazione](optimizing-interactions-between-the-com--business-logic-tier-and-the-presentation-tier.md)
</dt> </dl>

 

 



