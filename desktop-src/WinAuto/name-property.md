---
title: Proprietà Name
description: La proprietà Name è una stringa usata dai client per identificare, trovare o annunciare un oggetto per l'utente. Tutti gli oggetti supportano la proprietà Name.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce046ef693e9e52323cdb7484bbdc291127b958d88857de6a8be4522b88e33de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133774"
---
# <a name="name-property"></a>Proprietà Name

La **proprietà Name** è una stringa usata dai client per identificare, trovare o annunciare un oggetto per l'utente. Tutti gli oggetti supportano **la proprietà** Name.

Ad esempio, il testo in un controllo pulsante è il nome, mentre il nome di una casella di riepilogo o di un controllo di modifica è il testo statico che precede immediatamente il controllo nell'ordine di tabulazione. Anche gli oggetti grafici che non visualizzano un nome forniscono testo quando viene eseguita una query per la **proprietà Name.**

La **proprietà Name** viene recuperata chiamando [**IAccessible::get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).

## <a name="selecting-names"></a>Selezione dei nomi

Il nome di un oggetto deve essere intuitivo in modo che gli utenti comprendano il significato o lo scopo dell'oggetto. Inoltre, la **proprietà Name** deve essere univoca rispetto a qualsiasi oggetto di pari livello nell'elemento padre.

La navigazione all'interno delle tabelle presenta problemi particolarmente complessi per alcuni utenti. Pertanto, gli sviluppatori di server devono rendere i nomi delle celle della tabella il più descrittivi possibile. Ad esempio, è possibile creare un nome di cella combinando i nomi della riga e della colonna che occupa, ad esempio "A1". Tuttavia, in genere è consigliabile usare nomi più descrittivi, ad esempio "Nancy, Febbraio", dove "Nancy" è la riga corrente e "Febbraio" è la colonna corrente.

## <a name="delegating-requests"></a>Delega delle richieste

Se un oggetto non ha accesso alla relativa proprietà **Name,** delega le richieste al relativo elemento padre, identificando se stesso in base al relativo ID figlio. Ad esempio, se un client chiama la proprietà **Name** di un controllo di modifica, il controllo di modifica delega la query al relativo elemento padre, che restituisce il valore del controllo di testo statico che etichetta il controllo di modifica.

 

 




