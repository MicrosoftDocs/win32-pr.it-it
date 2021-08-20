---
title: Modifica delle interfacce utente esistenti
description: Nel riquadro dei risultati dello snap-in MMC Utenti e computer di Active Directory vengono visualizzate diverse colonne di dati degli attributi per gli oggetti all'interno di un contenitore, ad esempio gli attributi Nome e Descrizione.
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Modifica delle interfacce utente esistenti in ACTIVE Directory
- Snap-in Utenti e computer di Active Directory, modifica della visualizzazione
- Snap-in Di Active Directory per utenti e computer, aggiunta di colonne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf6ef4743009086ae19148c42a8addc5974e4ac833cdad8eee675fdce76a5f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025869"
---
# <a name="modifying-existing-user-interfaces"></a>Modifica delle interfacce utente esistenti

Nel riquadro dei risultati dello snap-in MMC Utenti e computer di Active Directory vengono visualizzate diverse colonne di dati degli attributi per gli oggetti all'interno di un contenitore, ad esempio gli attributi **Nome** **e Descrizione.** Lo snap-in consente all'utente di aggiungere e rimuovere le colonne visualizzate nel riquadro dei risultati dello snap-in.

Per modificare la visualizzazione, l'utente usa il menu **a** discesa Visualizza e seleziona **Aggiungi/Rimuovi colonne.** Nella finestra **di dialogo Aggiungi/Rimuovi** colonne è disponibile un elenco di colonne tra cui l'utente può scegliere di visualizzare nel riquadro dei risultati.

Lo snap-in MMC Utenti e computer di Active Directory incluso in Windows Server 2003, edizione Standard, Windows Server 2003, edizione Enterprise e Windows Server 2003 Datacenter Edition consente di modificare l'elenco di colonne che possono essere visualizzate nel riquadro dei risultati dello snap-in per un contenitore. Questa funzionalità esiste solo se lo snap-in è destinato a una foresta con Windows Schema di Server 2003.

Per aggiungere una colonna all'elenco, aggiungere un valore all'attributo **extraColumns** dell'identificatore di visualizzazione per il tipo di oggetto a cui è associato l'attributo. **L'attributo extraColumns** è un attributo stringa multivalore in cui ogni stringa è nel formato seguente.


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



Nella tabella seguente sono elencati i contenuti di questi valori.



| Valore                        | Descrizione                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| " &lt; ldapdisplayname &gt; "    | Contiene una stringa che rappresenta **ldapDisplayName** dell'attributo.                                                         |
| " &lt; intestazione di colonna &gt; "      | Contiene una stringa che rappresenta il testo visualizzato nell'intestazione della colonna.                                                  |
| " &lt; visibilità predefinita &gt; " | Contiene un valore numerico che è 0 se l'attributo è nascosto per impostazione predefinita oppure 1 se l'attributo è visibile per impostazione predefinita.               |
| " &lt; width &gt; "              | Contiene la larghezza della colonna, in pixel. Se questo valore è -1, la larghezza della colonna viene impostata sulla larghezza dell'intestazione di colonna. |
| " &lt; unused &gt; "             | Non utilizzato. Deve essere zero.                                                                                                               |



 

Ad esempio, per aggiungere una colonna che visualizza il nome canonico per gli oggetti in un'unità organizzativa, viene aggiunto un valore per l'attributo **canonicalName** all'attributo **extraColumns** dell'oggetto **organizationalUnit-Display** nel contenitore degli identificatori di visualizzazione. La stringa aggiunta **all'attributo extraColumns** dell'oggetto **organizationalUnit-Display** sarà simile alla seguente.


```C++
canonicalName,Canonical Name,0,150,0
```



Nella **finestra di dialogo** Aggiungi/Rimuovi colonne vengono visualizzate solo le colonne contenute nell'attributo **extraColumns** dell'oggetto **displaySpecifier** del tipo di contenitore visualizzato. Se **l'attributo extraColumns** non contiene valori, nella finestra di dialogo **Aggiungi/Rimuovi** colonne verrà visualizzato un set fisso di colonne. Una copia del set fisso di colonne è contenuta **nell'attributo extraColumns** dell'oggetto **default-Display.**

Per aggiungere una o più colonne all'elenco di colonne per un oggetto specifico, è necessario copiare tutti i valori **extraColumns** dall'oggetto **default-Display** all'oggetto di destinazione e quindi aggiungere le colonne personalizzate. Se si specifica l'attributo **extraColumns** in una determinata classe, tale classe userà tali colonne e non le unirà alle colonne specificate nella **classe default-Display.** Pertanto, ulteriori modifiche alla **classe default-Display** non avranno alcun effetto su tale oggetto.

Per visualizzare una colonna personalizzata per tutti i tipi di contenitore in cui non sono registrate colonne personalizzate, aggiungere un valore per la colonna all'attributo **extraColumns** **dell'oggetto default-Display.**

 

 




