---
title: Uso di ADO per il recupero di intervalli
description: Se si usa un linguaggio di automazione, ActiveX Oggetti directory (ADO) per recuperare un intervallo di valori di proprietà. Quando si usa ADO per il recupero di intervalli, esiste un problema che deve essere risolto in modo specifico.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Uso di ADO per il recupero di intervalli ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523cd65e7d26a82b9b647913c919bef374b1c76ddf1a18fd9f99384b4ae6e483
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023049"
---
# <a name="using-ado-for-range-retrieval"></a>Uso di ADO per il recupero di intervalli

Se si usa un linguaggio di automazione, è necessario usare ActiveX Directory Objects (ADO) per recuperare un intervallo di valori di proprietà.

Quando si usa ADO per il recupero di intervalli, esiste un problema che deve essere risolto in modo specifico. Quando si esegue una query per il gruppo finale di valori di proprietà, l'oggetto ADO recupererà zero oggetti, anche se ne rimangono altri. Per recuperare i valori rimanenti, usare il carattere jolly dell'intervallo ' \* '. Ad esempio, se un gruppo contiene 150 membri, i valori dei membri da 0 a 100 possono essere recuperati normalmente usando il recupero a intervalli. Se viene richiesto l'intervallo 101-200, l'oggetto ADO restituirà zero oggetti. A questo punto, è necessario modificare la query per richiedere l'intervallo 101- \* . Verranno recuperati valori da 101 a 150. Per altre informazioni e un esempio di codice, vedere Codice di esempio per l'uso [di ranging per recuperare i membri di un gruppo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).

Per altre informazioni sull'uso di ADO per il recupero di intervalli, vedere:

-   [ADO LDAP Ranging Dialect](ado-ldap-ranging-dialect.md)
-   [Dialetto ad SQL ADO](ado-sql-ranging-dialect.md)
-   [Codice di esempio per l'uso di Ranging per recuperare i membri di un gruppo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




