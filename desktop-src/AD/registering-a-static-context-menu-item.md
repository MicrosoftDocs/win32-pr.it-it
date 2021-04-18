---
title: Registrazione di una voce di menu di scelta rapida statica
description: In questo argomento viene descritta la registrazione di una voce di menu di scelta rapida statica visualizzata per oggetti Active Directory.
ms.assetid: ed945812-3adb-4058-bdb6-8d9d34468265
ms.tgt_platform: multiple
keywords:
- Registrazione di una voce di menu di scelta rapida statica AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89e3ee5336061ca296e2c94f8907ebd385610494
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "106299560"
---
# <a name="registering-a-static-context-menu-item"></a>Registrazione di una voce di menu di scelta rapida statica

Gli snap-in di MMC amministrativi di Active Directory Domain Services e la shell di Windows forniscono un meccanismo per aggiungere un elemento al menu di scelta rapida visualizzato per gli oggetti in Active Directory Domain Services. Il menu di scelta rapida può richiamare qualsiasi file che può essere avviato con l'API [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) , ad esempio l'URL di un'applicazione o di una pagina Web.

## <a name="registering-with-active-directory-domain-services"></a>Registrazione con Active Directory Domain Services

La registrazione dell'estensione del menu di scelta rapida è specifica di un'impostazione locale. Se l'estensione del menu di scelta rapida si applica a tutte le impostazioni locali, deve essere registrata nell'oggetto [**displaySpecifier**](/windows/desktop/ADSchema/c-displayspecifier) della classe di oggetti in tutti i sottocontenitori delle impostazioni locali nel contenitore degli identificatori di visualizzazione. Se l'estensione del menu di scelta rapida è localizzata per determinate impostazioni locali, deve essere registrata nell'oggetto **displaySpecifier** nel sottocontenitore delle impostazioni locali. Per ulteriori informazioni sul contenitore e le impostazioni locali per gli identificatori di visualizzazione, vedere la pagina relativa agli [identificatori di visualizzazione](display-specifiers.md) e al [contenitore DisplaySpecifiers](displayspecifiers-container.md).

Sono disponibili due attributi per gli identificatori di visualizzazione in cui è possibile registrare una voce di menu di scelta rapida statica, [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) e [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu).

L'attributo [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) identifica i menu di scelta rapida amministrativi da visualizzare negli snap-in amministrativi del Active Directory Domain Services. Il menu di scelta rapida viene visualizzato quando l'utente Visualizza il menu di scelta rapida per gli oggetti della classe appropriata in uno degli snap-in MMC amministrativi.

L'attributo [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) identifica i menu di scelta rapida dell'utente finale da visualizzare nella shell di Windows. Il menu di scelta rapida viene visualizzato quando l'utente Visualizza il menu di scelta rapida per gli oggetti della classe appropriata in Esplora risorse. A partire da Windows Server 2003, la shell di Windows non Visualizza più gli oggetti provenienti da Active Directory Domain Services.

Tutti questi attributi sono multivalore.

Quando si registra una voce di menu di scelta rapida statica, i valori per gli attributi [**adminContextMenu**](/windows/desktop/ADSchema/a-admincontextmenu) e [**shellContextMenu**](/windows/desktop/ADSchema/a-shellcontextmenu) richiedono il formato seguente.


```C++
<order number>,<menu text>,<command>
```



Il " &lt; numero &gt; di ordine" è un numero senza segno che rappresenta la posizione dell'elemento nel menu di scelta rapida. Quando viene visualizzato un menu di scelta rapida, i valori vengono ordinati usando un confronto tra il " &lt; numero di ordine" di ogni valore &gt; . Se più di un valore ha lo stesso " &lt; numero &gt; di ordine", le estensioni del menu di scelta rapida vengono caricate nell'ordine in cui vengono lette dal server Active Directory. Se possibile, usare un " &lt; numero di ordine" non esistente &gt; , ovvero uno che non è stato usato da altri valori nella proprietà. Non esiste una posizione di inizio prescritta e sono consentiti gap nella &lt; sequenza "Order Number &gt; ".

Il " &lt; testo &gt; di menu" è la stringa visualizzata nel menu di scelta rapida. Il " &lt; testo &gt; di menu" può includere un carattere "&" che precede il tasto di scelta rapida per la voce di menu. In questo modo il carattere preceduto sarà sottolineato. Se ad esempio il " &lt; testo del menu &gt; " è "&file", il testo del menu verrà visualizzato come "file", la "f" sarà sottolineata e "f" sarà il tasto di scelta rapida per la voce di menu.

Il " &lt; comando &gt; " è il programma o il file eseguito dallo snap-in. È necessario specificare il percorso completo oppure il file deve essere presente nella variabile di ambiente percorso computer. Il file viene richiamato usando la funzione [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) . Il " &lt; comando &gt; " non può contenere parametri aggiuntivi, ad esempio Notepad.exe Myfile.txt. Poiché viene usato **ShellExecute** , è possibile usare qualsiasi file o indirizzo che può essere passato a **ShellExecute** per " &lt; Command &gt; ". Se, ad esempio, " &lt; Command &gt; " contiene "d: \\file.txt", d: \\file.txt verrà aperto con l'applicazione associata all'estensione txt. Analogamente, se " &lt; Command &gt; " contiene " https://www.fabrikam.com ", viene aperto il Web browser predefinito e verrà visualizzata la pagina Web specificata. Sono consentiti percorsi e nomi di applicazioni con spazi. Se " &lt; Command &gt; " è un'applicazione, le ADsPath e la classe dell'oggetto selezionato vengono passate come argomenti della riga di comando, separate da uno spazio.

Nella shell di Windows sono supportate le voci del menu di scelta rapida a selezione multipla. In questo caso, &lt; &gt; viene richiamato "Command" per ogni oggetto selezionato. In Active Directory Domain Services gli snap-in di amministrazione, le voci del menu di scelta rapida statico a selezione multipla non sono supportate.

> [!IMPORTANT]
> Per la shell di Windows, i dati dell'identificatore di visualizzazione vengono recuperati all'accesso dell'utente e memorizzati nella cache per la sessione dell'utente. Per gli snap-in amministrativi, i dati dell'identificatore di visualizzazione vengono recuperati quando lo snap-in viene caricato e viene memorizzato nella cache per la durata del processo. Per la shell di Windows, ciò significa che le modifiche apportate agli identificatori di visualizzazione diventano effettive dopo che un utente si disconnette e si riaccende. Per gli snap-in amministrativi, le modifiche diventano effettive quando lo snap-in o il file della console viene ricaricato; ovvero, se si avvia una nuova istanza del file di console o di una nuova istanza di Mmc.exe e si aggiunge lo snap-in, vengono recuperati i dati degli identificatori di visualizzazione più recenti.

 

Per ulteriori informazioni e un esempio di codice, vedere [codice di esempio per l'installazione di una voce di menu di scelta rapida statica](example-code-for-installing-a-static-context-menu-item.md).

 

 