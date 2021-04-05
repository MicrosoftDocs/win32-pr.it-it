---
description: Poiché il programma di installazione utilizza un database relazionale, sono disponibili funzioni che consentono di eseguire query Structured Query Language (SQL) nel database. Nella procedura riportata di seguito viene descritto come utilizzare SQL per eseguire query su un database.
ms.assetid: 1b8fd935-4964-4875-801b-cc6765b16924
title: Utilizzo delle query
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0be4839c1e97f05d09769d69d62345b0602b789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967728"
---
# <a name="working-with-queries"></a>Utilizzo delle query

Poiché il programma di installazione utilizza un database relazionale, sono disponibili funzioni che consentono di eseguire query Structured Query Language (SQL) nel database. Nella procedura riportata di seguito viene descritto come utilizzare SQL per eseguire query su un database.

**Per eseguire una query su un database con SQL**

1.  Aprire l'oggetto [**View**](view-object.md) , con l'istruzione SQL appropriata, chiamando la funzione [**MsiDatabaseOpenView**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseopenviewa) .

    Un oggetto [**visualizzazione**](view-object.md) è la tabella logica creata applicando una query a un set di tabelle. Le query SQL devono rispettare la [sintassi SQL](sql-syntax.md) fornita dal programma di installazione. Questa istruzione SQL può contenere marcatori di parametro che non vengono specificati fino a quando non viene eseguito l'oggetto **visualizzazione** .

2.  Eseguire l'oggetto [**View**](view-object.md) chiamando la funzione [**MsiViewExecute**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewexecute) .
3.  Recuperare il record successivo da un oggetto [**visualizzazione**](view-object.md) chiamando la funzione [**MsiViewFetch**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewfetch) .
4.  Modificare l'oggetto [**visualizzazione**](view-object.md) chiamando la funzione [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) .

    È anche possibile convalidare i dati con [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) passando i flag appropriati. Se **MsiViewModify** restituisce \_ un errore \_ di dati non validi da una richiesta di convalida, i dati sottostanti sono danneggiati.

5.  Ottenere informazioni dettagliate sull'errore nell'oggetto [**vista**](view-object.md) chiamando la funzione [**MsiViewGetError**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora) .
6.  Chiudere l'oggetto [**View**](view-object.md) chiamando la funzione [**MsiViewClose**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewclose) .

Per ulteriori informazioni, vedere [esempi di query sul database con SQL e script](examples-of-database-queries-using-sql-and-script.md).

 

 



