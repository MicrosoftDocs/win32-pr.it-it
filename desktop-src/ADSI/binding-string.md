---
title: Stringa di binding
description: A causa del numero di oggetti accessibili da un servizio directory, possono verificarsi conflitti di denominazione.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- ADSI stringa di binding
- ADsPath ADSI, descrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13d2d8b58dd01713fa6382f27714b72651ad6f8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963448"
---
# <a name="binding-string"></a>Stringa di binding

A causa del numero di oggetti accessibili da un servizio directory, possono verificarsi conflitti di denominazione. La stringa di associazione, nota in genere come ADsPath, consente di specificare un oggetto particolare senza causare un conflitto di denominazione. Questo può essere applicato per un singolo provider di servizi directory o per più provider di servizi di directory.

Un ADsPath è una stringa che identifica in modo univoco un oggetto ADSI in un servizio directory. Poiché gli oggetti ADSI sono presenti nel contesto dello spazio dei nomi del servizio directory sottostante, una parte della sintassi di un nome ADsPath è specifica del provider.

Nella tabella seguente sono elencati i provider ADSI forniti per impostazione predefinita.



| Provider         | Descrizione                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WinNT<br/> | Utilizzato per comunicare con i controller di dominio Windows. Per ulteriori informazioni sul ADsPath WinNT, vedere [WinNT ADsPath](winnt-adspath.md).<br/>           |
| LDAP<br/>  | Utilizzato per comunicare con i server LDAP, ad esempio Active Directory. Per ulteriori informazioni su LDAP ADsPath, vedere [LDAP ADsPath](ldap-adspath.md).<br/>  |
| Annunci<br/>   | Fornisce un'implementazione di [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) che può essere utilizzata per enumerare tutti i provider ADSI installati nel client.<br/> |



 

Usare questi nomi di provider per accedere allo spazio dei nomi del provider predefinito. Se ad esempio si esegue l'associazione a LDAP, ADSI viene associato a un contenitore che contiene l'oggetto di dominio attualmente connesso. Se si esegue l'associazione a WinNT, ADSI viene associato a un contenitore che include oggetti correlati a tutti i domini nella rete.

Gli elementi iniziali della stringa ADsPath sono l'identificatore a livello di codice (progID) del provider ADSI, seguito da "://", seguito dalla sintassi dettata dallo spazio dei nomi del provider. La stringa progID può o meno fare distinzione tra maiuscole e minuscole, a seconda del provider. Le stringhe progID per i provider elencate in precedenza fanno distinzione tra maiuscole e minuscole.

La stringa di percorso può o meno fare distinzione tra maiuscole e minuscole, a seconda del provider. Le stringhe di percorso per i provider elencate sopra non fanno distinzione tra maiuscole e minuscole.

Di seguito sono riportati alcuni esempi di ADsPaths.

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

Per trovare tutti i provider installati nel computer, eseguire l'associazione al provider ADs come illustrato nell'esempio di codice seguente.


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



Utilizzando il provider LDAP, è possibile specificare il ADsPath in un formato di nome distinto X. 500, a partire dal tag CN, oppure è possibile specificare l'inverso gerarchico, a partire dal tag O. Il form usato nella ADsPath iniziale determina l'ordine dei tag.

Nella tabella seguente sono elencati i caratteri speciali ADsPath.



| Nome                      | Carattere           | Descrizione                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Virgoletta doppia<br/>   | "<br/>        | Usato per citare qualsiasi parte di ADsPath che può contenere un carattere speciale in modo che la stringa venga interpretata letteralmente. Ad esempio, "CN = nome/prefisso".<br/>                                     |
| Barra rovesciata<br/>      | \\<br/>       | Usato per precedere i caratteri speciali per indicare che devono essere usati come valori letterali. Per ulteriori informazioni e per un elenco di caratteri speciali, vedere [nomi distinti](/previous-versions/windows/desktop/ldap/distinguished-names).<br/> |
| Barra<br/>          | /<br/>        | Separatore componenti.<br/>                                                                                                                                                                       |
| Parentesi acute<br/> | <><br/> | Delimitare un ADsPath all'interno di un'altra convenzione di denominazione.<br/>                                                                                                                                       |



 

Per delimitare un ADsPath in una specifica di ricerca o come parte di un URL, utilizzare la parentesi uncinata aperta (< >). Ad esempio, " &lt; WinNT://mydomain/UserAccount &gt; ".

Alcuni provider ADSI potrebbero avere aggiunto restrizioni di sintassi a causa dei requisiti dello spazio dei nomi.

## <a name="active-directory-binding-options"></a>Opzioni di associazione Active Directory

Active Directory fornisce la possibilità di eseguire l'associazione a un oggetto utilizzando diversi altri tipi di stringhe di associazione, ad esempio un identificatore univoco globale (GUID) COM o un ID di sicurezza (SID). Per ulteriori informazioni, vedere [associazione a Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).

 

