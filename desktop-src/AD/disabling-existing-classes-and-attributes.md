---
title: Disabilitazione di classi e attributi esistenti
description: Le aggiunte dello schema sono permanenti.
ms.assetid: 13ffd2f5-cf1d-4cde-a3d5-74cb5a44b6fc
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74863d0d3c72f383259cfe262f4b7aa6fa27774a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707714"
---
# <a name="disabling-existing-classes-and-attributes"></a>Disabilitazione di classi e attributi esistenti

Le aggiunte dello schema sono permanenti. Non è possibile eliminare gli oggetti **attributeSchema** e **classSchema** . In un sistema distribuito è difficile garantire che non esistano istanze di una determinata classe o attributo. Se si rimuove la definizione di una classe o di un attributo, vengono danneggiate le istanze esistenti di tale classe o attributo.

È possibile disabilitare una classe o un attributo esistente contrassegnando il valore come "inattivo". Questa operazione non influisce sulle istanze esistenti della classe o dell'attributo in modo che siano contrassegnate, ma impedisce la creazione di nuove istanze.

Quando si disabilitano le classi e gli attributi dello schema, si applicano le restrizioni seguenti:

-   Non è possibile disabilitare una classe o un attributo di categoria 1.
-   Non è possibile disabilitare un attributo che è membro di una classe non anche disabilitata. Questo perché un attributo potrebbe essere necessario per la classe (non disabilitata) e la disabilitazione dell'attributo impedisce la creazione di nuove istanze della classe.

Per disabilitare **un attributo, impostare l'attributo** disattivo dell'oggetto **attributeSchema** su **true**. Quando un attributo è disabilitato, non è possibile creare nuove istanze dell'attributo. Per abilitare nuovamente **l'attributo, impostare l'attributo** IsEnabled su **false**.

Per disabilitare una classe, **impostare l'attributo disattivo dell'** oggetto **classSchema** su **true**. Quando una classe è disabilitata, non è possibile creare nuove istanze della classe. Per abilitare nuovamente la classe, impostare l' **attributo IsEnabled** su **false**.

L'impostazione di oggetti dello schema come inattivo può essere utile negli ambienti di produzione. Quando una versione di test di un'estensione dello schema non è più necessaria, contrassegnarla come inattiva. È possibile ripristinarlo rimuovendo l'attributo **Indefunto** o impostando il valore dell'attributo su **false**. In questo modo si protegge anche da una rimozione non intenzionale di un oggetto dello schema, impostando il campo come inattivo perché l'operazione può essere annullata facilmente.

Tenere presente che il server Active Directory non esegue la pulizia delle istanze esistenti di un attributo o di una classe quando si rende inattivo un oggetto dello schema. Se si **rimuove la proprietà IsValid, le istanze** diventeranno di nuovo validi oggetti normali.

L'elenco seguente include altre conseguenze del contrassegno di un oggetto **attributeSchema** o **classSchema** inattivo:

-   L'aggiunta o la modifica di un'istanza non riesce.
-   I codici di errore si comportano come se una classe inattiva non esisteva.
-   La ricerca e l'eliminazione si comportano come se non fossero stati resi inattivi gli oggetti dello schema.
-   Consente solo l'eliminazione dell'intero attributo dall'oggetto.

Nell'elenco seguente sono incluse opzioni aggiuntive in un ambiente di produzione per ridurre l'impatto delle estensioni dello schema inattive:

-   Rimuovere tutti i valori dell'attributo **Faran** da una classe inattiva.
-   Ridurre le dimensioni di tutti i valori dell'attributo **musthave** da una classe inattiva.
-   Rimuovere un attributo inattivo dal catalogo globale.
-   Rimuovere un attributo inattivo da qualsiasi indice.

Altre opzioni per la rimozione di modifiche dello schema indesiderate in un ambiente di produzione sono destinate agli sviluppatori a utilizzare un controller di dominio privato per il test. In questo caso, è possibile:

-   "Reimpostare" il server Active Directory usando Dcpromo.exe per abbassare di più il controller di dominio. Al termine dell'abbassamento di livello, utilizzare di nuovo Dcpromo.exe per innalzare di livello il server a un controller di dominio. Lo sviluppatore può quindi utilizzare gli script LDIF per ricaricare le classi, gli attributi e le istanze degli oggetti richiesti.
-   Utilizzare Ntbackup.exe per eseguire un backup dello stato del sistema in una partizione del disco disponibile. Riavviare la modalità di ripristino del servizio Safe/directory per il ripristino.

Per i sistemi operativi Windows Server 2003, quando si imposta una classe o un attributo su inattivo, è possibile riutilizzare immediatamente i valori **ldapDisplayName**, **schemaIDGUID**, **OID** e **mapiID** dell'elemento dello schema inattivo quando si crea una nuova classe o attributo per sostituirlo. La versione inattiva della classe o dell'attributo viene mantenuta nel contenitore dello schema, ma è nascosta nello snap-in MMC. Per riattivare l'elemento dello schema precedente, impostare il valore di **Unfunct** su **false**.

Nell'esempio di codice LDIF riportato di seguito viene illustrato come modificare l'attributo **Indefunto** e modificare il RDN in modo che non venga confuso con la nuova classe creata per sostituirla.

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

Usare il comando seguente per eseguire l'esempio di codice LDIF su una foresta per un computer in esecuzione in sistemi operativi Windows Server 2003.

**ldifde/i/f RDN. ldf/c "DC = X" "DC = Domain, DC = com"**

(Dove "DC = X" è una costante)

 

 




