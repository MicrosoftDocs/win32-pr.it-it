---
title: Utilizzo di ADO per il recupero di intervalli
description: Se viene usato un linguaggio di automazione, è necessario usare ADO (ActiveX Directory Objects) per recuperare un intervallo di valori di proprietà. Quando si usa ADO per il recupero di intervalli, è necessario risolvere un problema specifico.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Utilizzo di ADO per il recupero di intervalli ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707366"
---
# <a name="using-ado-for-range-retrieval"></a>Utilizzo di ADO per il recupero di intervalli

Se viene usato un linguaggio di automazione, è necessario usare ADO (ActiveX Directory Objects) per recuperare un intervallo di valori di proprietà.

Quando si usa ADO per il recupero di intervalli, è necessario risolvere un problema specifico. Quando si esegue una query per il gruppo di valori di proprietà finale, l'oggetto ADO recupererà zero oggetti, anche se rimane. Per recuperare i valori rimanenti, usare il carattere jolly di intervallo ' \* '. Se, ad esempio, un gruppo contiene 150 membri, è possibile recuperare i valori dei membri 0-100 normalmente utilizzando il recupero con intervallo. Se viene quindi richiesto l'intervallo 101-200, l'oggetto ADO restituirà zero oggetti. A questo punto è necessario modificare la query in un intervallo di richiesta 101- \* . Questa operazione consente di recuperare i valori da 101 a 150. Per ulteriori informazioni e un esempio di codice, vedere [codice di esempio per l'utilizzo di ranging per recuperare i membri di un gruppo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).

Per ulteriori informazioni sull'utilizzo di ADO per il recupero di intervalli, vedere:

-   [Dialetto ADO LDAP](ado-ldap-ranging-dialect.md)
-   [Sottolinguaggio ADO SQL](ado-sql-ranging-dialect.md)
-   [Codice di esempio per l'uso della funzione Rang per recuperare i membri di un gruppo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




