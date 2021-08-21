---
title: Disabilitazione di classi e attributi esistenti
description: Le aggiunte dello schema sono permanenti.
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a783bc0898cf3ecc883865abde037d1e70c60ec83913f2fb9148e230ae392f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118018801"
---
# <a name="disabling-existing-classes-and-attributes"></a>Disabilitazione di classi e attributi esistenti

Le aggiunte dello schema sono permanenti. Non è possibile eliminare **gli oggetti attributeSchema** **e classSchema.** In un sistema distribuito è difficile garantire che non siano presenti istanze di una determinata classe o attributo. La rimozione della definizione di una classe o di un attributo danneggia le istanze esistenti di tale classe o attributo.

È possibile disabilitare una classe o un attributo esistente contrassegnarlo come "inattivo". Ciò non influisce sulle istanze esistenti della classe o dell'attributo così contrassegnate, ma impedisce la creazione di nuove istanze.

Quando si disabilitano le classi e gli attributi dello schema, si applicano le restrizioni seguenti:

-   Non è possibile disabilitare una classe o un attributo di categoria 1.
-   Non è possibile disabilitare un attributo membro di una classe che non è anche disabilitato. Ciò è dovuto al fatto che potrebbe essere necessario un attributo per la classe (non disabilitata) e la disabilitazione dell'attributo impedisce la creazione di nuove istanze della classe.

Per disabilitare un attributo, impostare **l'attributo isDefunct** del relativo **oggetto attributeSchema** su **TRUE.** Quando un attributo è disabilitato, non è possibile creare nuove istanze dell'attributo. Per abilitare nuovamente l'attributo , impostare **l'attributo isDefunct** su **FALSE.**

Per disabilitare una classe, impostare **l'attributo isDefunct** del relativo **oggetto classSchema** su **TRUE.** Quando una classe è disabilitata, non è possibile creare nuove istanze della classe. Per abilitare nuovamente la classe, impostare **l'attributo isDefunct** su **FALSE.**

L'impostazione di oggetti dello schema come inevasi può essere utile negli ambienti di produzione. Quando una versione di test di un'estensione dello schema non è più necessaria, contrassegnarla come inevasa. È possibile ripristinarlo rimuovendo **l'attributo isDefunct** o impostando il valore dell'attributo su **FALSE.** Ciò consente anche di proteggersi da una rimozione imprevista di un oggetto dello schema impostandolo su inevaso perché l'operazione può essere facilmente invertito.

Tenere presente che il server Active Directory non esegue la pulizia delle istanze esistenti di un attributo o di una classe quando si rende in defezione un oggetto dello schema. Se si rimuove la **proprietà isDefunct,** tutte le istanze diventano di nuovo oggetti normali validi.

L'elenco seguente include altre conseguenze del contrassegno di **un oggetto attributeSchema** o **classSchema** in defezione:

-   L'aggiunta o la modifica di un'istanza ha esito negativo.
-   I codici di errore si comportano come se non esistesse mai una classe inesistente.
-   La ricerca e l'eliminazione si comportano come se nessun oggetto dello schema fosse stato reso infetto.
-   Consente solo l'eliminazione dell'intero attributo dall'oggetto.

L'elenco seguente include opzioni aggiuntive in un ambiente di produzione per ridurre l'impatto delle estensioni dello schema inevase:

-   Rimuovere tutti **i valori di attributo mayHave** da una classe inevasa.
-   Ridurre le dimensioni di tutti i valori di attributo **mustHave** da una classe in defezione.
-   Rimuovere un attributo inevaso dal catalogo globale.
-   Rimuovere un attributo inevaso da qualsiasi indice.

Altre opzioni per rimuovere le modifiche indesiderate dello schema in un ambiente di produzione sono per gli sviluppatori che usano un controller di dominio privato per i test. In questo caso, è possibile:

-   "Reimpostare" il server Active Directory usando Dcpromo.exe per abbassare di livello il controller di dominio. Al termine dell'abbassamento di livello, usare Dcpromo.exe per alzare di nuovo di livello il server a controller di dominio. Lo sviluppatore può quindi usare gli script LDIF per ricaricare le classi, gli attributi e le istanze di oggetti necessari.
-   Usare Ntbackup.exe per eseguire un backup dello stato del sistema in una partizione del disco disponibile. Riavviare il Cassaforte/ripristino del servizio directory per eseguire il ripristino.

Per i sistemi operativi Windows Server 2003, quando si imposta una classe o un attributo su inesatto, è possibile riutilizzare immediatamente i valori **ldapDisplayName**, **schemaIdGuid**, **OID** e **mapiID** dell'elemento dello schema in stato in corso quando si crea una nuova classe o attributo per sostituirlo. La versione inevasa della classe o dell'attributo viene mantenuta nel contenitore Schema, ma è nascosta nello snap-in MMC. Per riattivare l'elemento dello schema precedente, impostare **isDefunct** su **FALSE.**

L'esempio di codice LDIF seguente illustra come modificare l'attributo **isDefunct** e modificare rdn in modo che non sia confuso con la nuova classe creata per sostituirlo.

``` syntax
 dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modify
   replace: isDefunct
   isDefunct: TRUE
   -

   dn: CN=MyClass,CN=Schema,CN=Configuration,DC=X
   changetype: modrdn
   newrdn: cn=MyClassOld
   deleteoldrdn: 1

   dn:
   changetype: modify
   add: schemaUpdateNow
   schemaUpdateNow: 1
   -
```

Usare il comando seguente per eseguire l'esempio di codice LDIF su una foresta per un computer in esecuzione Windows Server 2003.

**ldifde /i /f rdn.ldf /c "DC=X" "dc=mydomain,dc=com"**

(Dove "DC=X" è una costante)

 

 




