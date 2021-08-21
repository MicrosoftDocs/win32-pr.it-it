---
title: Stringa di binding
description: A causa del numero di oggetti accessibili da un servizio directory, possono verificarsi conflitti di denominazione.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- Stringa di associazione ADSI
- ADsPath ADSI , descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad8e1bc59011c1279b340348572fa0681a0d301319f75603b73714df4c9cb96f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023689"
---
# <a name="binding-string"></a>Stringa di binding

A causa del numero di oggetti accessibili da un servizio directory, possono verificarsi conflitti di denominazione. La stringa di associazione, comunemente definita ADsPath, consente di specificare un oggetto specifico senza causare un conflitto di denominazione. Questo può essere applicato per un singolo provider di servizi directory o tra più provider di servizi directory.

ADsPath è una stringa che identifica in modo univoco un oggetto ADSI in un servizio directory. Poiché gli oggetti ADSI esistono all'interno del contesto dello spazio dei nomi del servizio directory sottostante, parte della sintassi di un nome ADsPath è specifica del provider.

Nella tabella seguente sono elencati i provider ADSI forniti per impostazione predefinita.



| Provider         | Descrizione                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Winnt<br/> | Usato per comunicare con i Windows di dominio. Per altre informazioni su WinNT ADsPath, vedere [WinNT ADsPath.](winnt-adspath.md)<br/>           |
| LDAP<br/>  | Usato per comunicare con i server LDAP, ad esempio Active Directory. Per altre informazioni su LDAP ADsPath, vedere [LDAP ADsPath.](ldap-adspath.md)<br/>  |
| Annunci<br/>   | Fornisce [**un'implementazione di IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) che può essere utilizzata per enumerare tutti i provider ADSI installati nel client.<br/> |



 

Usare questi nomi di provider per accedere allo spazio dei nomi del provider predefinito. Ad esempio, se si esegue l'associazione a LDAP, ADSI esegue l'associazione a un contenitore che contiene l'oggetto di dominio attualmente connesso. Se si esegue l'associazione a WinNT, ADSI esegue l'associazione a un contenitore che contiene oggetti correlati a tutti i domini nella rete.

Gli elementi iniziali della stringa ADsPath sono l'identificatore programmatico (progID) del provider ADSI, seguito da "://", seguito dalla sintassi determinata dallo spazio dei nomi del provider. La stringa progID può o meno fare distinzione tra maiuscole e minuscole, a seconda del provider. Le stringhe progID per i provider elencati in precedenza fa distinzione tra maiuscole e minuscole.

La stringa di percorso può o meno fare distinzione tra maiuscole e minuscole, a seconda del provider. Le stringhe di percorso per i provider elencati in precedenza non supportano la distinzione tra maiuscole e minuscole.

Di seguito sono riportati esempi di ADsPaths.

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

Per trovare tutti i provider installati nel computer, eseguire il binding al provider ADs come illustrato nell'esempio di codice seguente.


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



Usando il provider LDAP, è possibile specificare ADsPath in un formato di nome distinto (DN) X.500, a partire dal tag CN, oppure è possibile specificarne l'inverso gerarchico, a partire dal tag O. Il modulo utilizzato nell'ADsPath iniziale determina l'ordine dei tag.

Nella tabella seguente sono elencati i caratteri speciali ADsPath.



| Nome                      | Carattere           | Descrizione                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Virgoletta doppia<br/>   | "<br/>        | Usato per virgolette qualsiasi parte di ADsPath che può contenere un carattere speciale in modo che la stringa venga interpretata letteralmente. Ad esempio, "CN=Nome/Prefisso".<br/>                                     |
| Barra rovesciata<br/>      | \\<br/>       | Usato per far precedere i caratteri speciali per indicare che devono essere usati come valori letterali. Per altre informazioni e un elenco di caratteri speciali, vedere [Nomi distinti.](/previous-versions/windows/desktop/ldap/distinguished-names)<br/> |
| Barra<br/>          | /<br/>        | Separatore componenti.<br/>                                                                                                                                                                       |
| Parentesi acute<br/> | <><br/> | Delimitare un ADsPath all'interno di un'altra convenzione di denominazione.<br/>                                                                                                                                       |



 

Per delimitare un ADsPath in una specifica di ricerca o come parte di un URL, usare la parentesi uncinata aperta e chiusa (< >). Ad esempio, " &lt; WinNT://MyDomain/UserAccount &gt; ".

Alcuni provider ADSI potrebbero avere aggiunto restrizioni di sintassi a causa dei requisiti dello spazio dei nomi.

## <a name="active-directory-binding-options"></a>Opzioni di binding di Active Directory

Active Directory consente di eseguire l'associazione a un oggetto usando diversi altri tipi di stringhe di associazione, ad esempio un identificatore univoco globale (GUID) COM o un ID di sicurezza (SID). Per altre informazioni, vedere [Binding ad Active Directory.](/windows/desktop/AD/binding-to-active-directory-domain-services)

 

