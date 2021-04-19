---
description: In questo argomento vengono descritti i tipi di classi di finestra, il modo in cui vengono individuati dal sistema e gli elementi che definiscono il comportamento predefinito delle finestre che vi appartengono.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\window_89windowclasse.htm
title: Classi finestra (Windows e messaggi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da95fc54a9527bade0d925c1f993cf853b0ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317232"
---
# <a name="window-classes-windows-and-messages"></a>Classi finestra (Windows e messaggi)

In questo argomento vengono descritti i tipi di classi di finestra, il modo in cui vengono individuati dal sistema e gli elementi che definiscono il comportamento predefinito delle finestre che vi appartengono.

Una classe di finestra è un set di attributi utilizzato dal sistema come modello per creare una finestra. Ogni finestra è un membro di una classe di finestra. Tutte le classi finestra sono specifiche del processo.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                                 | Descrizione                                                                                                                                                                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sulle classi finestra](about-window-classes.md)     | Vengono illustrate le classi di finestra. Ogni classe della finestra dispone di una routine della finestra associata condivisa da tutte le finestre della stessa classe. La routine della finestra elabora i messaggi per tutte le finestre della classe e quindi ne controlla il comportamento e l'aspetto.<br/> |
| [Uso delle classi finestra](using-window-classes.md)     | Viene illustrato come registrare una finestra locale e usarla per creare una finestra principale.<br/>                                                                                                                                                                     |
| [Riferimento alla classe Window](window-class-reference.md) | Contiene il riferimento all'API.<br/>                                                                                                                                                                                                                         |



 

### <a name="window-class-functions"></a>Funzioni della classe di finestra



| Nome                                         | Descrizione                                                                                                                                                                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)     | Recupera le informazioni su una classe della finestra, incluso un handle per l'icona piccola associata alla classe della finestra. La funzione [**GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) non recupera un handle per l'icona piccola.<br/> |
| [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga)         | Recupera il valore specificato a 32 bit (**Long**) dalla struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) associata alla finestra specificata. <br/>                                                                         |
| [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)   | Recupera il valore specificato dalla struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) associata alla finestra specificata.<br/>                                                                                            |
| [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)         | Recupera il nome della classe a cui appartiene la finestra specificata. <br/>                                                                                                                                            |
| [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)       | Recupera le informazioni sulla finestra specificata. La funzione recupera inoltre il valore a 32 bit (**Long**) in corrispondenza dell'offset specificato nella memoria della finestra aggiuntiva.<br/>                                                    |
| [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) | Recupera le informazioni sulla finestra specificata. La funzione recupera inoltre il valore in corrispondenza di un offset specificato nella memoria della finestra aggiuntiva.<br/>                                                                        |
| [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa)       | Registra una classe della finestra per l'utilizzo successivo nelle chiamate alla funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .<br/>                                                             |
| [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)   | Registra una classe della finestra per l'utilizzo successivo nelle chiamate alla funzione [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) o [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) . <br/>                                                            |
| [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)   | Sostituisce il valore specificato in corrispondenza dell'offset specificato nella memoria della classe aggiuntiva o della struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) per la classe a cui appartiene la finestra specificata.<br/>                              |
| [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword)         | Sostituisce il valore a 16 bit (**Word**) in corrispondenza dell'offset specificato nella memoria della classe aggiuntiva per la classe della finestra a cui appartiene la finestra specificata.<br/>                                                               |
| [**SetWindowLong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)       | Modifica un attributo della finestra specificata. La funzione imposta anche il valore di 32 bit (Long) in corrispondenza dell'offset specificato nella memoria della finestra aggiuntiva.<br/>                                                                 |
| [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) | Modifica un attributo della finestra specificata. La funzione imposta anche un valore in corrispondenza dell'offset specificato nella memoria della finestra aggiuntiva.<br/>                                                                                   |
| [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)   | Annulla la registrazione di una classe della finestra, liberando la memoria necessaria per la classe. <br/>                                                                                                                                            |



 

Le funzioni seguenti sono obsolete.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a></td>
<td>Recupera le informazioni relative a una classe di finestra. <br/>
<blockquote>
[!Note]<br />
La funzione <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a> è stata sostituita dalla funzione <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa"><strong>GetClassInfoEx</strong></a> . È comunque possibile usare <strong>GetClassInfo</strong>, se non sono necessarie informazioni sull'icona della classe Small.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/winuser/nf-winuser-getclassword"><strong>GetClassWord</strong></a></td>
<td>Recupera il valore a 16 bit (<strong>Word</strong>) in corrispondenza dell'offset specificato nella memoria della classe aggiuntiva per la classe della finestra a cui appartiene la finestra specificata.
<blockquote>
[!Note]<br />
Questa funzione è deprecata per qualsiasi utilizzo diverso da <em>nIndex</em> impostato su GCW_ATOM. La funzione viene fornita solo per la compatibilità con le versioni di Windows a 16 bit. Le applicazioni devono utilizzare la funzione <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga"><strong>GetClassLong</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga"><strong>SetClassLong</strong></a></td>
<td>Sostituisce il valore specificato a 32 bit (<strong>Long</strong>) in corrispondenza dell'offset specificato nella memoria della classe aggiuntiva o nella struttura <a href="/windows/win32/api/winuser/ns-winuser-wndclassexa"><strong>WNDCLASSEX</strong></a> per la classe a cui appartiene la finestra specificata.
<blockquote>
[!Note]<br />
Questa funzione è stata sostituita dalla funzione <a href="/windows/desktop/api/winuser/nf-winuser-setclasslongptra"><strong>SetClassLongPtr</strong></a> . Per scrivere codice compatibile con le versioni di Windows a 32 bit e a 64 bit, usare <strong>SetClassLongPtr</strong>.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="window-class-structures"></a>Strutture della classe Window



| Nome                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)     | Contiene gli attributi della classe di finestra registrati dalla funzione [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . <br/> Questa struttura è stata sostituita dalla struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) usata con la funzione [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) . È comunque possibile usare [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) e [**registerClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) se non è necessario impostare l'icona piccola associata alla classe Window.<br/>                                                  |
| [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) | Contiene informazioni sulla classe di finestra. Viene usato con le funzioni [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) e [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)  . <br/> La struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) è simile alla struttura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) . Esistono due differenze. **WNDCLASSEX** include il membro **cbSize** , che specifica le dimensioni della struttura e il membro **hIconSm** , che contiene un handle per un'icona piccola associata alla classe Window.<br/> |



 

 

 
