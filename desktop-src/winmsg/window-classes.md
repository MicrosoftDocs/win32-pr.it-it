---
description: Questo argomento descrive i tipi di classi finestra, il modo in cui il sistema le individua e gli elementi che definiscono il comportamento predefinito delle finestre che le appartengono.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\window_89windowclasse.htm
title: Classi di finestra (Windows e messaggi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a77e96a06433bf6bbcb72fb76a41a29fccee27ad
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482647"
---
# <a name="window-classes-windows-and-messages"></a>Classi di finestra (Windows e messaggi)

Questo argomento descrive i tipi di classi finestra, il modo in cui il sistema le individua e gli elementi che definiscono il comportamento predefinito delle finestre che le appartengono.

Una classe finestra è un set di attributi che il sistema usa come modello per creare una finestra. Ogni finestra è un membro di una classe di finestra. Tutte le classi di finestra sono specifiche del processo.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                                 | Descrizione                                                                                                                                                                                                                                                    |
|------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sulle classi di finestre](about-window-classes.md)     | Vengono illustrate le classi di finestra. A ogni classe di finestra è associata una routine della finestra condivisa da tutte le finestre della stessa classe. La routine della finestra elabora i messaggi per tutte le finestre della classe e ne controlla pertanto il comportamento e l'aspetto.<br/> |
| [Uso delle classi di finestra](using-window-classes.md)     | Illustra come registrare una finestra locale e usarla per creare una finestra principale.<br/>                                                                                                                                                                     |
| [Informazioni di riferimento sulla classe Window](window-class-reference.md) | Contiene il riferimento all'API.<br/>                                                                                                                                                                                                                         |



 

### <a name="window-class-functions"></a>Funzioni della classe Window



| Nome                                         | Descrizione                                                                                                                                                                                                                   |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetClassInfoEx**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa)     | Recupera informazioni su una classe della finestra, incluso un handle per l'icona piccola associata alla classe della finestra. La [**funzione GetClassInfo**](/windows/win32/api/winuser/nf-winuser-getclassinfoa) non recupera un handle per l'icona piccola.<br/> |
| [**GetClassLong**](/windows/win32/api/winuser/nf-winuser-getclasslonga)         | Recupera il valore a 32 bit (**long**) specificato dalla [**struttura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) associata alla finestra specificata. <br/>                                                                         |
| [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)   | Recupera il valore specificato dalla struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) associata alla finestra specificata.<br/>                                                                                            |
| [**GetClassName**](/windows/win32/api/winuser/nf-winuser-getclassname)         | Recupera il nome della classe a cui appartiene la finestra specificata. <br/>                                                                                                                                            |
| [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)       | Recupera informazioni sulla finestra specificata. La funzione recupera anche il valore a 32 bit (**long**) in corrispondenza dell'offset specificato nella memoria della finestra aggiuntiva.<br/>                                                    |
| [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) | Recupera informazioni sulla finestra specificata. La funzione recupera anche il valore in corrispondenza di un offset specificato nella memoria aggiuntiva della finestra.<br/>                                                                        |
| [**Registerclass**](/windows/win32/api/winuser/nf-winuser-registerclassa)       | Registra una classe di finestra per un uso successivo nelle chiamate alla [**funzione CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**o CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)<br/>                                                             |
| [**RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa)   | Registra una classe di finestra per un uso successivo nelle chiamate alla [**funzione CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) [**o CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa) <br/>                                                            |
| [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)   | Sostituisce il valore specificato in corrispondenza dell'offset specificato nella memoria della classe aggiuntiva o nella struttura [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) per la classe a cui appartiene la finestra specificata.<br/>                              |
| [**SetClassWord**](/windows/win32/api/winuser/nf-winuser-setclassword)         | Sostituisce il valore a 16 bit (**WORD**) in corrispondenza dell'offset specificato nella memoria della classe aggiuntiva per la classe della finestra a cui appartiene la finestra specificata.<br/>                                                               |
| [**Setwindowlong**](/windows/win32/api/winuser/nf-winuser-setwindowlonga)       | Modifica un attributo della finestra specificata. La funzione imposta anche il valore a 32 bit (long) in corrispondenza dell'offset specificato nella memoria aggiuntiva della finestra.<br/>                                                                 |
| [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra) | Modifica un attributo della finestra specificata. La funzione imposta anche un valore in corrispondenza dell'offset specificato nella memoria aggiuntiva della finestra.<br/>                                                                                   |
| [**UnregisterClass**](/windows/win32/api/winuser/nf-winuser-unregisterclassa)   | Annulla la registrazione di una classe di finestra, liberando la memoria necessaria per la classe. <br/>                                                                                                                                            |



 

Le funzioni seguenti sono obsolete.




| Nome | Descrizione | 
|------|-------------|
| <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>GetClassInfo</strong></a> | Recupera informazioni su una classe finestra. <br /><blockquote>[!Note]<br />La <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoa"><strong>funzione GetClassInfo</strong></a> è stata sostituita dalla <a href="/windows/desktop/api/winuser/nf-winuser-getclassinfoexa"><strong>funzione GetClassInfoEx.</strong></a> È comunque possibile usare <strong>GetClassInfo,</strong>tuttavia, se non sono necessarie informazioni sull'icona piccola della classe.</blockquote><br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-getclassword"><strong>GetClassWord</strong></a> | Recupera il valore a 16 bit (<strong>WORD</strong>) in corrispondenza dell'offset specificato nella memoria della classe aggiuntiva per la classe finestra a cui appartiene la finestra specificata.<blockquote>[!Note]<br />Questa funzione è deprecata per qualsiasi uso diverso da <em>nIndex</em> impostato su GCW_ATOM. La funzione viene fornita solo per la compatibilità con le versioni a 16 bit di Windows. Le applicazioni devono usare <a href="/windows/desktop/api/winuser/nf-winuser-getclasslonga"><strong>la funzione GetClassLong.</strong></a></blockquote><br /><br /> | 
| <a href="/windows/desktop/api/winuser/nf-winuser-setclasslonga"><strong>SetClassLong</strong></a> | Sostituisce il valore a 32 bit<strong>(long)</strong>specificato in corrispondenza dell'offset specificato nella memoria della classe aggiuntiva o nella struttura <a href="/windows/win32/api/winuser/ns-winuser-wndclassexa"><strong>WNDCLASSEX</strong></a> per la classe a cui appartiene la finestra specificata.<blockquote>[!Note]<br />Questa funzione è stata sostituita dalla <a href="/windows/desktop/api/winuser/nf-winuser-setclasslongptra"><strong>funzione SetClassLongPtr.</strong></a> Per scrivere codice compatibile con le versioni a 32 bit e a 64 bit di Windows, usare <strong>SetClassLongPtr.</strong></blockquote><br /><br /> | 




 

### <a name="window-class-structures"></a>Strutture della classe Window



| Nome                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)     | Contiene gli attributi della classe della finestra registrati dalla [**funzione RegisterClass.**](/windows/win32/api/winuser/nf-winuser-registerclassa) <br/> Questa struttura è stata sostituita dalla [**struttura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) usata con la [**funzione RegisterClassEx.**](/windows/win32/api/winuser/nf-winuser-registerclassexa) È comunque possibile usare [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) e [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) se non è necessario impostare la piccola icona associata alla classe della finestra.<br/>                                                  |
| [**WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) | Contiene informazioni sulla classe della finestra. Viene usato con le [**funzioni RegisterClassEx**](/windows/win32/api/winuser/nf-winuser-registerclassexa) [**e GetClassInfoEx.**](/windows/win32/api/winuser/nf-winuser-getclassinfoexa) <br/> La [**struttura WNDCLASSEX**](/windows/win32/api/winuser/ns-winuser-wndclassexa) è simile alla [**struttura WNDCLASS.**](/windows/win32/api/winuser/ns-winuser-wndclassa) Esistono due differenze. **WNDCLASSEX** include il membro **cbSize,** che specifica le dimensioni della struttura, e il membro **hIconSm,** che contiene un handle per una piccola icona associata alla classe della finestra.<br/> |



 

 

 
