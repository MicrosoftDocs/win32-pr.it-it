---
title: Glossario (funzionalità di accessibilità di Windows)
description: Pagina del glossario
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: c45583f2-a6e8-4a01-9577-9b604b5bbc62
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16679c63f0716058e53c7c9d164a24593c481dff
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300822"
---
# <a name="glossary-windows-accessibility-features"></a>Glossario (funzionalità di accessibilità di Windows)

## <a name="a"></a>A

<dl> <dt>

**chiave di accesso**
</dt> <dd>

Carattere sottolineato nel testo dell'etichetta di un controllo.

</dd> <dt>

**supporto per l'accessibilità**
</dt> <dd>

Definito anche Assistive Technology; programmi specializzati che interagiscono con il sistema operativo di un computer per soddisfare specifici problemi, ad esempio un intervallo limitato di movimento o cecità. I prodotti includono tastiere più grandi, tastiere con controllo degli sguardi, utilità di input vocale, tastiere sullo schermo e prodotti in grado di convertire testo in sintesi vocale o in una visualizzazione dinamica Braille. Per ulteriori informazioni, vedere [prodotti Assistive Technology](https://www.microsoft.com/enable/at/default.aspx).

</dd> <dt>

**oggetto accessibile**
</dt> <dd>

Qualsiasi elemento dell'interfaccia utente che implementa l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) e dispone di proprietà che descrivono il nome dell'oggetto, le posizioni dello schermo e altre informazioni necessarie per gli strumenti di accessibilità. Per ulteriori informazioni, vedere [oggetti accessibili](accessible-objects.md).

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**elemento figlio**
</dt> <dd>

Vedere [*elemento semplice*](uiauto-glossary.md).

</dd> <dt>

**client**
</dt> <dd>

Qualsiasi programma che usa automazione interfaccia utente o Microsoft Active Accessibility per accedere, identificare o modificare gli elementi dell'interfaccia utente di un'applicazione; i client includono i supporti per l'accessibilità, gli strumenti di test automatizzati e alcune applicazioni di training basate su computer. Per ulteriori informazioni, vedere funzionamento di [Active Accessibility](how-active-accessibility-works.md).

</dd> <dt>

**provider lato client**
</dt> <dd>

Componente software implementato da un client di automazione interfaccia utente per recuperare informazioni sull'interfaccia utente di un'applicazione che non supporta o non supporta completamente l'automazione dell'interfaccia utente. In genere, i provider lato client (proxy) comunicano con l'applicazione attraverso il limite di processo inviando e ricevendo messaggi di Windows.

</dd> <dt>

**container**
</dt> <dd>

Detto anche padre; oggetto accessibile che corrisponde a uno o più elementi semplici; ad esempio, un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per una casella di riepilogo è l'elemento padre degli elementi dell'elenco.

</dd> <dt>

**pattern di controllo**
</dt> <dd>

In automazione interfaccia utente, implementazione di progettazione che descrive una parte di funzionalità discreta per un controllo. Questa funzionalità può includere l'aspetto visivo di un controllo e le azioni che può eseguire.

</dd> <dt>

**oggetto pattern di controllo**
</dt> <dd>

Istanza della fase di esecuzione di un oggetto COM che espone una o più interfacce del pattern di controllo.

</dd> <dt>

**provider pattern di controllo**
</dt> <dd>

Componente software che implementa una o più interfacce del pattern di controllo.

</dd> <dt>

**controllo personalizzato**
</dt> <dd>

Controllo creato da un utente o da un fornitore di software di terze parti oppure un controllo definito dal sistema modificato da un utente o da un fornitore di software di terze parti.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**degenerare l'intervallo di testo (intervallo vuoto)**
</dt> <dd>

Oggetto che rappresenta un intervallo di testo vuoto (carattere zero). Un intervallo di testo degenere presenta endpoint adiacenti e specifica un punto tra due caratteri.

</dd> <dt>

**intervallo di testo non contiguo**
</dt> <dd>

Oggetto che rappresenta più intervalli di testo che non sono fisicamente adiacenti tra loro.

</dd> <dt>

**ancoraggio del contenitore**
</dt> <dd>

Controllo che consente la disposizione di elementi figlio, sia orizzontalmente che verticalmente, rispetto ai limiti del contenitore di ancoraggio e ad altri elementi all'interno del contenitore.

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**listener di eventi**
</dt> <dd>

Un'applicazione client che ha eseguito la registrazione per ricevere notifiche da automazione interfaccia utente o Microsoft Active Accessibility ogni volta che vengono apportate modifiche specifiche dell'interfaccia utente.

</dd> <dt>

**notifica degli eventi**
</dt> <dd>

Una chiamata da un provider di automazione interfaccia utente a un client, in cui il provider invia una notifica al client di un evento che potrebbe influire sullo stato o sull'aspetto di un elemento dell'interfaccia utente.

</dd> </dl>

## <a name="f"></a>F

<dl> <dt>

**Filtra \[ zione\]**
</dt> <dd>

Per definire i tipi di elementi di automazione interfaccia utente da includere in una visualizzazione dell'albero di automazione interfaccia utente. Vedere anche: visualizzazione non elaborata, visualizzazione controlli e visualizzazione contenuto.

</dd> <dt>

**radice del frammento**
</dt> <dd>

Elemento di automazione interfaccia utente nel nodo radice di un sottoalbero dell'albero di automazione interfaccia utente. Una radice del frammento non ha un elemento padre ma è ospitata in un altro Framework, in genere un handle di finestra Win32 (**HWND**).

</dd> </dl>

## <a name="h"></a>H

<dl> <dt>

**host**
</dt> <dd>

Elemento dell'interfaccia utente, ad esempio una finestra o un controllo, che contiene altri elementi dell'interfaccia utente. Un host esegue i servizi di automazione interfaccia utente per conto degli elementi ospitati.

</dd> </dl>

## <a name="i"></a>I

<dl> <dt>

**IAccessible**
</dt> <dd>

Interfaccia COM che contiene tutti i metodi e le proprietà per Microsoft Active Accessibility.

</dd> <dt>

**Proxy IAccessible**
</dt> <dd>

Tipo di supporto di [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) che fornisce le informazioni di accessibilità predefinite per gli elementi dell'interfaccia utente standard: controlli utente, menu utente e controlli comuni da COMCTL e Comctl32. Per ulteriori informazioni, vedere la pagina relativa ai [proxy IAccessible](iaccessible-proxies.md).

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**navigazione logica**
</dt> <dd>

Una delle due modalità di navigazione [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) in cui un client Esplora la gerarchia di oggetti di Microsoft Active Accessibility (avanti, precedente, padre, primo figlio, ultimo figlio).

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**marshalling**
</dt> <dd>

Creazione di pacchetti e invio di parametri di interfaccia tra i limiti dei processi.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**implementazione nativa**
</dt> <dd>

Tipo di supporto fornito dagli elementi dell'interfaccia utente che implementano l'interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .

</dd> </dl>

## <a name="o"></a>O

<dl> <dt>

**modello fuori schermo**
</dt> <dd>

Questo modello è un database di oggetti sullo schermo e include le relative proprietà e le relative relazioni spaziali.

</dd> <dt>

**OLEACC**
</dt> <dd>

La libreria a collegamento dinamico che fornisce Microsoft Active Accessibility Runtime e gestisce le richieste dei client Microsoft Active Accessibility.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**parent**
</dt> <dd>

Detto anche contenitore; oggetto accessibile che corrisponde a uno o più elementi semplici; ad esempio, un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per una casella di riepilogo è l'elemento padre degli elementi dell'elenco.

</dd> <dt>

**elemento di automazione segnaposto**
</dt> <dd>

Elemento di automazione interfaccia utente che rappresenta un elemento virtualizzato nell'albero di automazione interfaccia utente. In genere, un segnaposto non dispone di dati caricati per tutte le proprietà di automazione interfaccia utente ed è necessario implementare solo il pattern di controllo [VirtualizedItem](uiauto-implementingvirtualizeditem.md) .

</dd> <dt>

**evento di modifica proprietà**
</dt> <dd>

Evento che viene attivato quando viene modificato il valore di una proprietà. I client si registrano per ricevere eventi di modifica di proprietà specifici e l'automazione interfaccia utente invia una notifica ai client registrati quando si verificano tali eventi.

</dd> <dt>

**interfaccia del provider**
</dt> <dd>

Raccolta di metodi pubblici implementati da un provider di automazione interfaccia utente.

</dd> <dt>

**proxy**
</dt> <dd>

Vedere il [*proxy IAccessible*](uiauto-glossary.md).

</dd> </dl>

## <a name="r"></a>R

<dl> <dt>

**visualizzazione non elaborata**
</dt> <dd>

Albero completo degli oggetti [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) nell'albero di automazione interfaccia utente per il quale il desktop è la radice. La visualizzazione non elaborata segue strettamente la struttura nativa a livello di codice di un'applicazione e pertanto è la visualizzazione più accurata della struttura dell'interfaccia utente. Costituisce inoltre la base sulla quale vengono compilate le altre visualizzazioni dell'albero.

</dd> <dt>

**elemento realizzato**
</dt> <dd>

Elemento dell'interfaccia utente per il quale le informazioni complete sono state caricate in memoria, consentendo all'automazione dell'interfaccia utente di creare un elemento di automazione per l'elemento.

</dd> <dt>

**Identificatore della fase di esecuzione**
</dt> <dd>

Matrice di numeri interi che identifica l'istanza in esecuzione di un elemento di automazione interfaccia utente. L'identificatore è univoco all'interno dell'interfaccia utente del desktop in cui è stato generato.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**matrice sicura**
</dt> <dd>

Tipo di dati autodescrittivo per la dichiarazione di matrici utilizzate nella creazione di componenti COM. Insieme ai dati, una matrice sicura contiene informazioni sul numero e sui limiti delle relative dimensioni.

</dd> <dt>

**ambito**
</dt> <dd>

Definizione dell'extent della vista, a partire da un elemento di base.

</dd> <dt>

**server**
</dt> <dd>

Qualsiasi controllo, modulo o applicazione che utilizza Microsoft Active Accessibility per esporre informazioni sull'interfaccia utente

</dd> <dt>

**provider lato server**
</dt> <dd>

Componente software che espone informazioni su un elemento dell'interfaccia utente basato su un Framework dell'interfaccia utente che non supporta l'automazione dell'interfaccia utente in modo nativo. I provider lato server (provider nativi) comunicano con le applicazioni client attraverso il limite di processo esponendo le interfacce COM al sistema principale di automazione interfaccia utente, che consente di soddisfare le richieste dei client.

</dd> <dt>

**elemento Simple**
</dt> <dd>

Noto anche come elemento figlio; qualsiasi elemento dell'interfaccia utente che condivide un oggetto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) con altri elementi e si basa su tale oggetto **IAccessible** per esporre le relative proprietà. Per altre informazioni, vedere [elementi semplici](simple-elements.md).

</dd> <dt>

**navigazione spaziale**
</dt> <dd>

Una delle due modalità di navigazione [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) in cui un client passa da un elemento dell'interfaccia utente a un altro in base alle rispettive posizioni sullo schermo (verso l'alto, verso il basso, a sinistra, a destra).

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**Text Services Framework**
</dt> <dd>

Framework di sistema scalabile che consente servizi di linguaggio naturale e input di testo avanzato sul desktop e all'interno delle applicazioni.

</dd> <dt>

**unità di testo**
</dt> <dd>

Unità di testo predefinita (carattere, parola, riga o paragrafo) utilizzata per spostarsi tra i segmenti logici di un intervallo di testo.

</dd> </dl>

## <a name="u"></a>U

<dl> <dt>

**Client di automazione interfaccia utente**
</dt> <dd>

Un'applicazione di Assistive Technology, ad esempio un'applicazione per la lettura dello schermo, che usa l'automazione dell'interfaccia utente per ottenere l'accesso a livello di codice agli elementi dell'interfaccia utente in un'interfaccia utente dell'applicazione. Il client presenta all'utente finale informazioni sugli elementi dell'interfaccia utente. Gli script di test automatizzati sono considerati anche client di automazione interfaccia utente.

</dd> <dt>

**Core di automazione interfaccia utente**
</dt> <dd>

Componente della fase di esecuzione che implementa il Framework di automazione interfaccia utente.

</dd> <dt>

**Elemento di automazione interfaccia utente**
</dt> <dd>

Elemento dell'interfaccia utente rappresentato da un oggetto COM che implementa un'interfaccia del provider di automazione interfaccia utente e che espone l'interfaccia [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) ai client di automazione interfaccia utente.

</dd> <dt>

**Framework di automazione interfaccia utente**
</dt> <dd>

Componente integrale di Windows che supporta l'accesso programmatico alla maggior parte degli elementi dell'interfaccia utente sul desktop. Consente ai prodotti di Assistive Technology, quali utilità per la lettura dello schermo, di fornire informazioni sull'interfaccia utente agli utenti finali e di modificare l'interfaccia utente per mezzo di input standard. Automazione interfaccia utente consente inoltre l'interazione degli script di test automatizzati con l'interfaccia utente.

</dd> <dt>

**Nodo di automazione interfaccia utente**
</dt> <dd>

Deprecato. Vedere elemento di automazione interfaccia utente.

</dd> <dt>

**Provider di automazione interfaccia utente**
</dt> <dd>

Implementazione di interfacce di automazione interfaccia utente che espone informazioni programmatiche su un elemento dell'interfaccia utente. Il provider fornisce queste informazioni al Framework di automazione interfaccia utente in risposta alle richieste del client di automazione interfaccia utente.

</dd> <dt>

**Albero di automazione interfaccia utente**
</dt> <dd>

Rappresentazione gerarchica di tutti gli elementi di automazione interfaccia utente sul desktop di Windows. L'albero è costituito da un elemento radice che rappresenta il desktop corrente e i cui elementi figlio rappresentano le finestre dell'applicazione. Ognuno di questi elementi figlio può contenere elementi che rappresentano parti dell'interfaccia utente, ad esempio menu, pulsanti, barre degli strumenti e caselle di riepilogo. Questi elementi possono contenere elementi come gli elementi elenco.

</dd> <dt>

**Framework dell'interfaccia utente**
</dt> <dd>

Componente che gestisce controlli figlio, hit testing e rendering in un'area dello schermo.

</dd> </dl>

## <a name="v"></a>V

<dl> <dt>

**identificatore visualizzazione**
</dt> <dd>

Valore che identifica una visualizzazione disponibile per un elemento di automazione interfaccia utente che implementa un pattern di controllo. Questo tipo di elemento fornisce ed è in grado di passare tra più rappresentazioni dello stesso set di informazioni o controlli figlio.

</dd> <dt>

**elemento virtualizzato**
</dt> <dd>

Elemento dell'interfaccia utente che viene caricato in memoria solo quando è necessario, in genere quando l'elemento diventa visibile sullo schermo. Un elemento virtualizzato è rappresentato da un elemento di automazione segnaposto nell'albero di automazione interfaccia utente.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Eventi finestra (WinEvents)**
</dt> <dd>

Tipo di evento utilizzato per notificare ai client che un oggetto accessibile è stato modificato in qualche modo.

</dd> <dt>

**elemento basato su finestra**
</dt> <dd>

Elemento di automazione interfaccia utente che rappresenta un elemento dell'interfaccia utente con il proprio handle di finestra Win32 (**HWND**).

</dd> </dl>

 

 




