---
description: Le proprietà utilizzate nel sistema di proprietà di Windows Vista e versioni successive sono dichiarate negli schemi proprietà.
ms.assetid: 4e301210-df3a-41db-a58e-015ee8d41714
title: Creazione di proprietà personalizzate.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90849383e25889edf7f3abd4704c36354eff153c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346646"
---
# <a name="creating-custom-properties"></a>Creazione di proprietà personalizzate.

Le proprietà utilizzate nel sistema di proprietà di Windows Vista e versioni successive sono dichiarate negli schemi proprietà. Questi schemi di proprietà sono definiti in file XML e descrivono i vari aspetti di una proprietà, incluso il relativo tipo (incluse le informazioni sul tipo primitivo e se è multivalore), come possono essere visualizzati nell'interfaccia utente di Windows, il tipo di etichette (stringhe di modifica descrittiva) da usare con esso e come viene memorizzato nella cache nell'archivio di ricerca per un accesso più rapido Le proprietà sono identificate dal nome canonico o dalla relativa chiave di proprietà (PKEY).

Un nome canonico è il nome descrittivo della proprietà e usa una convenzione dello spazio dei nomi simile a quella usata in Microsoft .NET. Per le proprietà definite dal sistema, ovvero quelle incluse in Windows, la convenzione è `System.GroupName.PropertyName` . Si noti che in questi nomi viene usato lo schema di maiuscole e minuscole Pascal, che converte in maiuscolo le lettere all'inizio di ogni parola. I nomi canonici vengono usati in vari punti, inclusi gli elenchi di proprietà e i nomi di colonna nella cache delle proprietà. Vengono pertanto utilizzati nelle query Structured Query Language (SQL) per recuperare il valore di una proprietà.

Un PKEY è una coppia di valori costituita da un GUID e un **valore DWORD**, definiti rispettivamente come *FormatID* e *propid* . È rappresentato da una struttura [**PropertyKey**](/windows/win32/api/wtypes/ns-wtypes-propertykey) . La maggior parte delle API del sistema di proprietà accetta queste chiavi di proprietà. Windows Software Development Kit (SDK) include il file di intestazione Propkey. h che include una definizione macro di ogni chiave di `System` proprietà con la convenzione `PKEY_GroupName_PropertyName` . Ad esempio, `PKEY_Photo_DateTaken` è la chiave della proprietà per la proprietà con nome canonico `System.Photo.DateTaken` . I valori delle proprietà vengono archiviati nel formato di una struttura [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) , che è un'estensione dei tipi Variant OLE.

In questa sezione è contenuto il seguente argomento, che è parte integrante della creazione di proprietà personalizzate:

-   [Informazioni sullo schema della descrizione della proprietà](./propdesc-schema-entry.md)

> [!Note]  
> A causa di potenziali problemi che l'indicizzatore potrebbe avere quando si utilizza lo schema del sistema di proprietà, è fondamentale definire gli attributi in modo accurato e strategico per il primo rilascio dello schema. Eventuali modifiche apportate agli attributi (tipo, larghezza delle colonne, se indicizzabili) non verranno riflesse nel database dopo che uno schema è stato registrato. L'unico modo per riconoscere queste modifiche dopo che lo schema è stato registrato una volta in un sistema sarebbe ricompilare l'indice e quindi registrare il nuovo schema oppure per registrare lo schema e quindi creare una nuova proprietà per ogni versione successiva; ad esempio `PKEY_GroupName_PropertyNameV2` , `PKEY_GroupName_PropertyNameV3` e così via). Non è consigliabile creare nuove proprietà in questo modo, perché più colonne estranee potrebbero avere conseguenze sulle prestazioni del sistema.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Implementazione di gestori di proprietà](./building-property-handlers.md)
</dt> <dt>

[Schema Descrizione proprietà](./propdesc-schema-entry.md)
</dt> </dl>

 

 
