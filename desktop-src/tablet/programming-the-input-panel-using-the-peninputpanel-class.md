---
description: Descrizione dell'utilizzo dell'oggetto PenInputPanel per programmare il pannello di input di Tablet PC a livello di sistema.
ms.assetid: f83c7709-86dc-4c64-ad17-2ad660eb57b7
title: Programmazione del pannello di input usando la classe PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e00d1cb10983255ab2e532aa08de6e9e6a0fb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349391"
---
# <a name="programming-the-input-panel-using-the-peninputpanel-class"></a>Programmazione del pannello di input usando la classe PenInputPanel

\[[**PenInputPanel**](peninputpanel-class.md) è stato sostituito da [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100)). Per [la programmazione del pannello input di testo](programming-the-text-input-panel.md), vedere.\]

Descrizione dell'utilizzo dell'oggetto [**PenInputPanel**](peninputpanel-class.md) per programmare il pannello di input di Tablet PC a livello di sistema.

## <a name="input-panel-vs-the-peninputpanel-object"></a>Pannello di input rispetto all'oggetto PenInputPanel

In Microsoft Windows XP Tablet PC Edition versione 1,0, il pannello di input di Tablet PC a livello di sistema fornisce un meccanismo universale per eseguire l'input di testo nella piattaforma Windows, ma non fornisce l'accesso a livello di codice. In Windows XP Tablet PC Edition Software Development Kit (SDK) versione 1,5 e successive, l'oggetto [**PenInputPanel**](peninputpanel-class.md) consente di integrare gli strumenti di input di testo direttamente nelle applicazioni e di fornire un livello di controllo non disponibile in precedenza. A partire da Windows XP Tablet PC Edition 2005, il pannello di input a livello di sistema è stato aggiornato in modo da includere la funzionalità di input sul posto fornita dall'oggetto **PenInputPanel** e altro ancora.

Il grafico seguente mostra il pannello di input visualizzato nell'esempio di [esempio di modulo delle attestazioni automatiche](auto-claims-form-sample.md) .

![Pannello di input visualizzato su un modulo usato per le attestazioni dell'automobile](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

Il pannello input sostituisce l'oggetto [**PenInputPanel**](peninputpanel-class.md) fornendo le stesse funzionalità di input sul posto a qualsiasi applicazione in esecuzione in Windows XP Tablet PC Edition 2005 o versione successiva senza la necessità di codice aggiuntivo. Questo articolo sull'uso dell'oggetto **PenInputPanel** viene fornito per compatibilità con le versioni precedenti. Le applicazioni che già utilizzano l'oggetto **PenInputPanel** funzioneranno allo stesso tempo, ad eccezione del fatto che il pannello di input verrà visualizzato al posto di **PenInputPanel** quando l'applicazione viene eseguita in Windows XP Tablet PC Edition 2005 o versioni successive.

Se si sviluppa una nuova applicazione per il Tablet PC e si desidera disporre di una soluzione di input utente sul posto, il pannello di input lo fornisce automaticamente in Windows XP Tablet PC Edition 2005 o versioni successive. Non è necessario creare un'istanza dell'oggetto [**PenInputPanel**](peninputpanel-class.md) .

## <a name="disabling-the-input-panel"></a>Disabilitazione del pannello input

In alcuni casi potrebbe essere necessario disabilitare il pannello di input. È possibile ottenere questo risultato in due modi. È possibile eseguire questa operazione a livello di codice o impostando una voce del registro di sistema che disabilita il pannello di input per l'intera applicazione.

### <a name="disabling-input-panel-programmatically"></a>Disabilitazione del pannello input a livello di codice

Per disabilitare il pannello di input a livello di codice, creare un'istanza di [**PenInputPanel**](peninputpanel-class.md) e impostare la relativa proprietà [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) su **false**.


```C++
using Microsoft.Ink;

// ...

private PenInputPanel theInputPanel;

// ...

private void Form1_Load(object sender, System.EventArgs e)
{
// Attach the Input Panel to a specific TextBox control.
theInputPanel = new PenInputPanel(textBox1);

// Disable the Input Panel for the TextBox.
theInputPanel.AutoShow = false;
}
```



Per disabilitare il pannello di input per più controlli in un'unica applicazione, creare un'istanza di un oggetto [**PenInputPanel**](peninputpanel-class.md) per ogni controllo e impostare la proprietà [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)su **false** per ogni o creare un'istanza di un singolo oggetto **PenInputPanel** e spostarlo dal controllo al controllo come modifiche dello stato attivo per l'input. Per ulteriori informazioni su queste due tecniche, vedere l'argomento di [esempio PenInputPanel](peninputpanel-sample.md) .

### <a name="disabling-input-panel-through-the-registry"></a>Disabilitazione del pannello di input tramite il registro di sistema

È possibile impostare una voce del registro di sistema per disabilitare il pannello di input per l'intera applicazione. Tuttavia, verrà disabilitato anche per le finestre di dialogo comuni, ad esempio la finestra di dialogo **Apri file** , la finestra di dialogo **stampa** e la finestra di dialogo **Salva file** . In questo modo l'esperienza utente nell'applicazione potrebbe non essere coerente con altre applicazioni Tablet PC.

L'impostazione della `DisableInPlace` chiave del registro di sistema su zero impedisce la visualizzazione dell'interfaccia utente del pannello di input in un'applicazione. È necessario inserire la `DisableInPlace` chiave del registro di sistema in `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\` . Aggiungere quindi un nuovo valore del registro di sistema usando il percorso completo dell'applicazione in cui si vuole disabilitare il pannello di input. La voce del registro di sistema di esempio seguente disabilita il pannello di input in un'applicazione denominata MyApp:

`[HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\WindowsNT\TabletTIP\DisableInPlace]``"C:\Program Files\My App\MyApp.exe"=dword:00000000`

Se nell'applicazione viene ancora visualizzato un problema dopo aver disattivato l'interfaccia utente del pannello di input, potrebbe essere necessario disabilitare il Framework sottostante, che esegue una query sull'applicazione per individuare la posizione del punto di inserimento. Ad esempio, il pannello di input può esporre un bug nel codice di traccia del punto di inserimento dell'applicazione. La disattivazione della query di rilevamento del cursore impedisce inoltre di visualizzare l'interfaccia utente del pannello di input. Per disabilitare il Framework, impostare la `EnableCaretTracking` chiave del registro di sistema su zero. Individuare la chiave in `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\` .

> [!Note]  
> Anche gli strumenti di accessibilità e la tecnologia vocale di Windows XP utilizzano questo Framework, quindi la disabilitazione della query Disabilita anche queste funzionalità nell'applicazione.

 

## <a name="the-input-panel-and-web-pages"></a>Il pannello di input e le pagine Web

Per usare un'API in una pagina Web, deve funzionare in un ambiente parzialmente attendibile. Tutti i membri della classe [**PenInputPanel**](peninputpanel-class.md) richiedono l'attendibilità totale, ad eccezione di quanto segue:

-   [Costruttori PenInputPanel](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (solo codice gestito)
-   [Metodo Dispose](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (solo codice gestito)
-   [Proprietà AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (solo codice gestito)
-   [**Proprietà AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)

Queste API funzionano in un ambiente parzialmente attendibile, ad esempio una pagina Web, che consente di creare un'istanza di un oggetto [**PenInputPanel**](peninputpanel-class.md) , collegarlo a un controllo e disabilitare il pannello di input per il controllo. Per ulteriori informazioni, vedere programmazione del pannello input utilizzando la classe PenInputPanel e l' [input penna sul Web](ink-on-the-web.md).

## <a name="the-peninputpanel-object"></a>Oggetto PenInputPanel

Nella parte restante di questo argomento viene descritto come utilizzare l'oggetto [**PenInputPanel**](peninputpanel-class.md) nelle applicazioni abilitate per Tablet PC. In particolare, questo argomento si riferisce all'oggetto **PenInputPanel** quando si discute l'oggetto di programmazione, il pannello input penna quando si fa riferimento all'elemento dell'interfaccia utente e il pannello di input del PC (o pannello di input) quando si fa riferimento al pannello di input globale in genere presente sul lato dello schermo del Tablet PC.

Le sezioni seguenti descrivono l'oggetto [**PenInputPanel**](peninputpanel-class.md) e l'interfaccia utente.

-   [Informazioni sul pannello input](about-the-input-panel.md)
-   [Creazione di un'istanza della classe PenInputPanel](instantiating-the-peninputpanel-class.md)
-   [Supporto del controllo controllo](factoid-support.md)
-   [Text Services Framework](text-services-framework.md)
-   [Procedure consigliate](best-practices.md)

 

 
