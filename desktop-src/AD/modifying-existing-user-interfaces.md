---
title: Modifica di interfacce utente esistenti
description: Il riquadro dei risultati dello snap-in MMC utenti e computer Active Directory Visualizza varie colonne di dati di attributo per gli oggetti all'interno di un contenitore, ad esempio gli attributi nome e descrizione.
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Modifica delle interfacce utente esistenti AD
- Snap-in utenti e computer di Active Directory, modifica della visualizzazione
- Snap-in utenti e computer AD, aggiunta di colonne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0765988a9ceed3e98966091ad94b868b96fd88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855406"
---
# <a name="modifying-existing-user-interfaces"></a>Modifica di interfacce utente esistenti

Il riquadro dei risultati dello snap-in MMC utenti e computer Active Directory Visualizza varie colonne di dati di attributo per gli oggetti all'interno di un contenitore, ad esempio gli attributi **nome** e **Descrizione** . Lo snap-in consente all'utente di aggiungere e rimuovere le colonne visualizzate nel riquadro dei risultati dello snap-in.

Per modificare la visualizzazione, l'utente utilizza il menu a discesa **Visualizza** e seleziona **Aggiungi/Rimuovi colonne**. Nella finestra di dialogo **Aggiungi/Rimuovi colonne** è disponibile un elenco di colonne che l'utente può scegliere di visualizzare nel riquadro risultati.

Lo snap-in MMC utenti e computer Active Directory incluso in Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition e Windows Server 2003, Datacenter Edition, consente di modificare l'elenco delle colonne che possono essere visualizzate nel riquadro dei risultati dello snap-in per un contenitore. Questa funzionalità è disponibile solo se lo snap-in è destinato a una foresta con schema di Windows Server 2003.

Per aggiungere una colonna all'elenco, aggiungere un valore all'attributo **outcolumns** dell'identificatore di visualizzazione per il tipo di oggetto a cui è associato l'attributo. L'attributo **outcolumns** è un attributo di stringa multivalore in cui ogni stringa è nel formato seguente.


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



La tabella seguente elenca il contenuto di questi valori.



| Valore                        | Descrizione                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| " &lt; ldapDisplayName &gt; "    | Contiene una stringa che rappresenta **ldapDisplayName** dell'attributo.                                                         |
| " &lt; intestazione di colonna &gt; "      | Contiene una stringa che rappresenta il testo visualizzato nell'intestazione della colonna.                                                  |
| " &lt; visibilità predefinita &gt; " | Contiene un valore numerico che è 0 se l'attributo è nascosto per impostazione predefinita o 1 se l'attributo è visibile per impostazione predefinita.               |
| " &lt; larghezza &gt; "              | Contiene la larghezza, in pixel, della colonna. Se questo valore è-1, la larghezza della colonna viene impostata sulla larghezza dell'intestazione di colonna. |
| "non &lt; usato &gt; "             | Non utilizzato. Deve essere zero.                                                                                                               |



 

Ad esempio, per aggiungere una colonna in cui verrà visualizzato il nome canonico per gli oggetti in un'unità organizzativa, viene aggiunto un valore per l'attributo **CanonicalName** all'attributo **outcolumns** dell'oggetto **organizationalUnit-Display** nel contenitore Display Specifiers. La stringa aggiunta all'attributo **outcolumns** dell'oggetto **organizationalUnit-Display** sarà simile alla seguente.


```C++
canonicalName,Canonical Name,0,150,0
```



Nella finestra di dialogo **Aggiungi/Rimuovi colonne** vengono visualizzate solo le colonne contenute nell'attributo **outcolumns** dell'oggetto **displaySpecifier** del tipo di contenitore visualizzato. Se l' **attributo delle colonne non** contiene valori, nella finestra di dialogo **Aggiungi/Rimuovi colonne** viene visualizzato un set fisso di colonne. Una copia del set di colonne fisso è contenuta nell'attributo **outcolumns** dell'oggetto di **visualizzazione predefinito** .

Per aggiungere una o più colonne all'elenco di colonne per un oggetto specifico, è necessario copiare tutti **i valori delle colonne a** partire dall'oggetto **predefinito-display** nell'oggetto di destinazione e quindi aggiungere le colonne personalizzate. Se si specifica l'attributo **outcolumns** su una determinata classe, tale classe utilizzerà tali colonne e non le unirà alle colonne specificate nella classe **default-Display** . Pertanto, ulteriori modifiche apportate alla classe **default-Display** non avranno alcun effetto su tale oggetto.

Per visualizzare una colonna personalizzata per tutti i tipi di contenitore per i quali non sono state registrate colonne personalizzate, aggiungere un valore per la colonna all'attributo **outcolumns** dell'oggetto **visualizzato per impostazione predefinita** .

 

 




