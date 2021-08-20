---
description: Poiché il programma di installazione usa un database relazionale, esistono funzioni per l'esecuzione di query Structured Query Language (SQL) al database. La procedura seguente descrive come usare SQL per eseguire query su un database.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Uso delle query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b6ea5a2f0b962b195fde531216f4b57fd5834162e31c1e34fc9ff1dd3695df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942126"
---
# <a name="working-with-queries"></a>Uso delle query

Poiché il programma di installazione usa un database relazionale, esistono funzioni per l'esecuzione di query Structured Query Language (SQL) al database. La procedura seguente descrive come usare SQL per eseguire query su un database.

**Per eseguire query su un database con SQL**

1.  Aprire [**l'oggetto View,**](view-object.md) con l'istruzione SQL appropriata, chiamando la [**funzione MsiDatabaseOpenView.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa)

    Un [**oggetto View**](view-object.md) è la tabella logica creata applicando una query a un set di tabelle. SQL query devono rispettare la sintassi [SQL specificata](sql-syntax.md) dal programma di installazione. Questa SQL può contenere marcatori di parametro che non vengono specificati fino **all'esecuzione dell'oggetto** View.

2.  Eseguire [**l'oggetto**](view-object.md) View chiamando la [**funzione MsiViewExecute.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute)
3.  Recuperare il record successivo da un [**oggetto View**](view-object.md) chiamando la [**funzione MsiViewFetch.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch)
4.  Modificare [**l'oggetto View**](view-object.md) chiamando la [**funzione MsiViewModify.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify)

    È anche possibile convalidare i dati [**con MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) passando i flag appropriati. Se **MsiViewModify restituisce** ERROR \_ INVALID DATA da una richiesta di \_ convalida, i dati sottostanti sono danneggiati.

5.  Ottenere informazioni dettagliate sull'errore [**nell'oggetto View**](view-object.md) chiamando la [**funzione MsiViewGetError.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)
6.  Chiudere [**l'oggetto View**](view-object.md) chiamando la [**funzione MsiViewClose.**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose)

Per altre informazioni, vedere [Esempi di query di database SQL e Script](examples-of-database-queries-using-sql-and-script.md).

 

 



