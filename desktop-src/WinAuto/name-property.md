---
title: Proprietà Name
description: La proprietà Name è una stringa utilizzata dai client per identificare, trovare o annunciare un oggetto per l'utente. Tutti gli oggetti supportano la proprietà Name.
ms.assetid: 7533955a-9538-4ead-a6ca-f61dd1b4d5c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e93d8b90190f81179d681600f4b1bfacf4665e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298314"
---
# <a name="name-property"></a>Proprietà Name

La proprietà **Name** è una stringa utilizzata dai client per identificare, trovare o annunciare un oggetto per l'utente. Tutti gli oggetti supportano la proprietà **Name** .

Il testo di un controllo Button, ad esempio, è il nome, mentre il nome di una casella di riepilogo o di un controllo di modifica è il testo statico che precede immediatamente il controllo nell'ordine di tabulazione. Anche gli oggetti grafici che non visualizzano un nome forniscono testo quando vengono sottoposti a query per la proprietà **Name** .

La proprietà **Name** viene recuperata chiamando [**IAccessible:: Get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname).

## <a name="selecting-names"></a>Selezione dei nomi

Il nome di un oggetto dovrebbe essere intuitivo per consentire agli utenti di comprendere il significato o lo scopo dell'oggetto. Inoltre, la proprietà **Name** deve essere univoca rispetto agli oggetti di pari livello nell'elemento padre.

La navigazione all'interno delle tabelle presenta problemi particolarmente complessi per alcuni utenti. Gli sviluppatori di server devono pertanto rendere i nomi delle celle di tabella più descrittivi possibili. Ad esempio, è possibile creare un nome di cella combinando i nomi della riga e della colonna occupata, ad esempio "a1". Tuttavia, in genere è preferibile usare nomi più descrittivi, ad esempio "Nancy, February", dove "Nancy" è la riga corrente e "February" è la colonna corrente.

## <a name="delegating-requests"></a>Delega di richieste

Se un oggetto non ha accesso alla proprietà **Name** , delega le richieste al relativo elemento padre, identificandosi in base al relativo ID figlio. Se, ad esempio, un client chiama la proprietà **Name** di un controllo di modifica, il controllo di modifica delega la query al relativo elemento padre, che restituisce il valore del controllo testo statico che etichetta il controllo di modifica.

 

 




