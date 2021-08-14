---
description: Descrizione dell'uso dell'oggetto PenInputPanel per programmare il Pannello input tablet PC a livello di sistema.
ms.assetid: f83c7709-86dc-4c64-ad17-2ad660eb57b7
title: Programmazione del pannello di input tramite la classe PenInputPanel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d430b002fb967652aea046919ec7341a984f420f756fd936e8c68dbfce8c055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449386"
---
# <a name="programming-the-input-panel-using-the-peninputpanel-class"></a>Programmazione del pannello di input tramite la classe PenInputPanel

\[[**PenInputPanel**](peninputpanel-class.md) è stato sostituito da [Microsoft.Ink.TextInput.](/previous-versions/ms581554(v=vs.100)) Fare riferimento a [Programmazione del Pannello input di testo](programming-the-text-input-panel.md).\]

Descrizione dell'uso [**dell'oggetto PenInputPanel**](peninputpanel-class.md) per programmare il Pannello input tablet PC a livello di sistema.

## <a name="input-panel-vs-the-peninputpanel-object"></a>Pannello di input e oggetto PenInputPanel

In Microsoft Windows XP Tablet PC Edition versione 1.0, il Pannello input penna tablet PC a livello di sistema fornisce un meccanismo universale per eseguire l'input di testo nella piattaforma Windows, ma non fornisce l'accesso a livello di codice. In Windows XP Tablet PC Edition Software Development Kit (SDK) versione 1.5 e successive, l'oggetto [**PenInputPanel**](peninputpanel-class.md) consente di integrare gli strumenti di input di testo direttamente nelle applicazioni e di fornire un livello di controllo non disponibile in precedenza. A partire da Windows XP Tablet PC Edition 2005, il Pannello input a livello di sistema è stato aggiornato per includere la funzionalità di input sul posto fornita dall'oggetto **PenInputPanel** e altro ancora.

La figura seguente mostra il Pannello input penna visualizzato [nell'esempio di esempio di modulo attestazioni](auto-claims-form-sample.md) automatico.

![Pannello di input visualizzato su un modulo usato per le attestazioni automobile](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

Il pannello di input sostituisce [**PenInputPanel**](peninputpanel-class.md) fornendo la stessa funzionalità di input sul posto a qualsiasi applicazione in esecuzione in Windows XP Tablet PC Edition 2005 o versione successiva senza la necessità di codice aggiuntivo. Questo articolo sull'uso **dell'oggetto PenInputPanel** viene fornito per garantire la compatibilità con le versioni precedenti. Le applicazioni che già utilizzano l'oggetto **PenInputPanel** funzioneranno allo stesso modo, ad eccezione del fatto che verrà visualizzato il Pannello di input anziché **PenInputPanel** quando l'applicazione viene eseguita Windows XP Tablet PC Edition 2005 o versione successiva.

Se si sviluppa una nuova applicazione per Tablet PC e si vuole avere una soluzione di input utente sul posto, il Pannello input penna lo fornisce automaticamente in Windows XP Tablet PC Edition 2005 o versione successiva. Non è necessario creare un'istanza [**dell'oggetto PenInputPanel.**](peninputpanel-class.md)

## <a name="disabling-the-input-panel"></a>Disabilitazione del Pannello input penna

In alcuni casi può essere necessario disabilitare il Pannello input penna. È possibile ottenere questo risultato in due modi. È possibile eseguire questa operazione a livello di codice o impostando una voce del Registro di sistema che disabilita il Pannello input penna per l'intera applicazione.

### <a name="disabling-input-panel-programmatically"></a>Disabilitazione del Pannello input a livello di codice

Per disabilitare il pannello di input a livello di codice, creare [**un'istanza di PenInputPanel**](peninputpanel-class.md) e impostarne la [**proprietà AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) su **False.**


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



Per disabilitare il pannello di input per più controlli in una singola applicazione, creare un'istanza di un oggetto [**PenInputPanel**](peninputpanel-class.md) per ogni controllo e impostare la proprietà [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)su False per **ogni** controllo oppure creare un'istanza di un singolo **Oggetto PenInputPanel** e spostarlo dal controllo al controllo quando cambia lo stato attivo per l'input. Per altre informazioni su queste due tecniche, vedere l'argomento PenInputPanel Sample (Esempio [di PenInputPanel).](peninputpanel-sample.md)

### <a name="disabling-input-panel-through-the-registry"></a>Disabilitazione del Pannello input tramite il Registro di sistema

È possibile impostare una voce del Registro di sistema per disabilitare il Pannello input penna per l'intera applicazione. Questa operazione verrà tuttavia disabilitata anche per le finestre di  dialogo comuni, ad esempio la finestra di dialogo **Apri file,** la finestra di dialogo Stampa e la finestra di dialogo **Salva** file. Ciò potrebbe rendere l'esperienza utente nell'applicazione incoerente con altre applicazioni Tablet PC.

L'impostazione della chiave del Registro di sistema su zero impedisce la visualizzazione dell'interfaccia utente del Pannello input `DisableInPlace` penna in un'applicazione. È necessario inserire la chiave `DisableInPlace` del Registro di sistema in `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\` . Aggiungere quindi un nuovo valore del Registro di sistema usando il percorso completo dell'applicazione in cui si vuole disabilitare il Pannello input penna. La voce del Registro di sistema di esempio seguente disabilita il Pannello input penna in un'applicazione denominata MyApp:

`[HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\WindowsNT\TabletTIP\DisableInPlace]``"C:\Program Files\My App\MyApp.exe"=dword:00000000`

Se si verifica ancora un problema nell'applicazione dopo aver disabilitato l'interfaccia utente del pannello di input, potrebbe essere necessario disabilitare il framework sottostante, che esegue una query sull'applicazione per il percorso del punto di inserimento. Ad esempio, il Pannello input penna può esporre un bug nel codice di rilevamento del punto di inserimento dell'applicazione. La disattivazione della query di rilevamento del punto di inserimento impedisce anche la visualizzazione dell'interfaccia utente del pannello di input. Per disabilitare il framework, impostare la chiave `EnableCaretTracking` del Registro di sistema su zero. Individuare questa chiave in `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\` .

> [!Note]  
> Anche gli strumenti di accessibilità e la tecnologia vocale Windows XP usano questo framework, quindi la disabilitazione della query disabilita anche queste funzionalità nell'applicazione.

 

## <a name="the-input-panel-and-web-pages"></a>Pannello di input e pagine Web

Per usare un'API in una pagina Web, deve funzionare in un ambiente parzialmente attendibile. Tutti [**i membri della classe PenInputPanel**](peninputpanel-class.md) richiedono l'attendibilità totale, ad eccezione dei seguenti:

-   [Costruttori PenInputPanel](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (solo codice gestito)
-   [Metodo Dispose](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (solo codice gestito)
-   [Proprietà AttachedEditControl](/previous-versions/ms582239(v=vs.100)) (solo codice gestito)
-   [**Proprietà AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)

Queste API funzionano in un ambiente parzialmente attendibile, ad esempio una pagina Web, consentendo di creare un'istanza di un [**oggetto PenInputPanel,**](peninputpanel-class.md) collegarlo a un controllo e disabilitare il pannello di input per tale controllo. Per altre informazioni, vedere Programmazione del pannello di input usando la classe PenInputPanel [e Ink sul Web.](ink-on-the-web.md)

## <a name="the-peninputpanel-object"></a>Oggetto PenInputPanel

Il resto di questo argomento descrive come usare [**l'oggetto PenInputPanel**](peninputpanel-class.md) nelle applicazioni abilitate per Tablet PC. In particolare, questo argomento fa riferimento all'oggetto **PenInputPanel** quando si parla dell'oggetto di programmazione, del pannello di input penna quando si fa riferimento all'elemento dell'interfaccia utente e del pannello di input del PC (o pannello di input) quando si fa riferimento al pannello di input globale disponibile in genere sul lato dello schermo del Tablet PC.

Le sezioni seguenti descrivono [**l'oggetto PenInputPanel**](peninputpanel-class.md) e l'interfaccia utente.

-   [Informazioni sul Pannello input penna](about-the-input-panel.md)
-   [Creazione di un'istanza della classe PenInputPanel](instantiating-the-peninputpanel-class.md)
-   [Supporto factoid](factoid-support.md)
-   [Text Services Framework](text-services-framework.md)
-   [Procedure consigliate](best-practices.md)

 

 
