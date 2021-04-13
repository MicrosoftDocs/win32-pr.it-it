---
description: Di seguito sono riportate le domande frequenti sullo sviluppo per i componenti della piattaforma Tablet PC installati da Windows Vista SDK.
ms.assetid: eb349493-a2b2-4b58-bcbc-ee09953c8dc8
title: Domande frequenti (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722c00fa5aaf2b43494484fc015fa8b3e4c7826
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104400018"
---
# <a name="frequently-asked-questions-about-developing-for-the-tablet-pc-platform"></a>Domande frequenti sullo sviluppo per la piattaforma Tablet PC

Di seguito sono riportate le domande frequenti sullo sviluppo per i componenti della piattaforma Tablet PC installati da Windows Vista SDK.

## <a name="q-can-i-use-the-ink-apis-or-controls-in-a-web-page"></a>Q. È possibile utilizzare le API o i controlli input penna in una pagina Web?

R. Sì. La libreria gestita da Tablet PC supporta ambienti parzialmente attendibili, ovvero l'esecuzione di assembly gestiti da pagine Web.

È inoltre disponibile il supporto per la distribuzione del browser di applicazioni che utilizzano Windows Presentation Foundation.

## <a name="q-do-i-need-a-tablet-pc-to-develop-tablet-pc-applications"></a>Q. È necessario un Tablet PC per sviluppare applicazioni Tablet PC?

R. No, i componenti della piattaforma Tablet PC installati dal Windows SDK includono le estensioni e le utilità necessarie per lo sviluppo di software per il Tablet PC in un computer desktop o portatile. È possibile utilizzare un mouse o un tablet esterno per input penna e grafia.

I componenti della piattaforma Tablet PC installati dal Windows SDK possono essere installati in Windows XP Professional o Windows Server 2003, ma per le applicazioni è disponibile un minor numero di funzionalità. Su queste piattaforme, l'applicazione può raccogliere input penna con gli oggetti [**InkCollector**](inkcollector-class.md) e [**InkOverlay**](inkoverlay-class.md) e può essere testata e sottoposta a debug.

Inoltre, i controlli [InkEdit](inkedit-control-reference.md) e [InkPicture](inkpicture-control-reference.md) possono raccogliere input penna su questi sistemi operativi solo se i componenti della piattaforma Tablet PC sono stati installati dalla Windows SDK (o da una versione precedente di Tablet PC Development Kit); non raccolgono input penna nelle applicazioni ridistribuite a computer non tablet senza installare i componenti della piattaforma.

## <a name="q-do-i-need-to-run-a-special-version-of-windows-to-do-handwriting-recognition"></a>Q. È necessario eseguire una versione speciale di Windows per eseguire il riconoscimento della grafia?

R. No. Mentre solo Windows XP Tablet PC Edition e alcune versioni di Windows Vista includono i riconoscitori della grafia, è possibile scaricare il [pacchetto di riconoscimento Windows XP Tablet PC Edition 2005]( https://www.microsoft.com/downloads/details.aspx?FamilyId=080184DD-5E92-4464-B907-10762E9F918B&amp;displaylang=en) e installarlo in Windows XP Professional o windows Server 2003 solo a scopo di sviluppo. Non è possibile ridistribuire i riconoscitori con l'applicazione.

## <a name="q-what-is-the-difference-between-windows-vista-and-tablet-pc-technology"></a>Q. Qual è la differenza tra la tecnologia Windows Vista e Tablet PC?

R. I Tablet PC eseguono il sistema operativo Windows Vista, con tutte le funzionalità di Windows Vista, oltre a funzionalità aggiuntive specifiche per il Tablet PC. Queste funzionalità della tecnologia Tablet PC consentono agli utenti di eseguire applicazioni Windows e Windows utilizzando una penna, annotando i documenti e creando documenti scritti a mano usando l'input penna digitale. La tecnologia Tablet PC è disponibile nella maggior parte delle versioni di Windows Vista e se l'hardware di Tablet PC è disponibile in un computer, le funzionalità funzionano.

Per le versioni precedenti dei sistemi operativi Windows che non supportano in modo nativo l'input penna, è possibile ridistribuire e utilizzare i controlli dell'input penna del Tablet PC per visualizzare l'input penna disegnato su un Tablet PC.

## <a name="q-what-is-the-difference-between-windows-xp-tablet-pc-edition-and-windows-xp-tablet-pc-edition-2005"></a>Q. Qual è la differenza tra Windows XP Tablet PC Edition e Windows XP Tablet PC Edition 2005?

R. Windows XP Tablet PC Edition 2005 è una versione aggiornata di Windows XP Tablet PC Edition.

## <a name="q-how-do-i-modify-my-application-to-run-on-a-tablet-pc"></a>Q. Ricerca per categorie modificare l'applicazione per l'esecuzione in un Tablet PC?

R. Le applicazioni Microsoft Windows in esecuzione in un computer desktop o portatile Windows XP con hardware analogo possono essere eseguite su un Tablet PC senza modifiche.

## <a name="q-i-understand-that-i-dont-need-to-make-any-changes-to-my-application-but-it-is-difficult-to-use-it-with-a-pen-and-speech-what-can-i-do-to-optimize-my-application-for-a-tablet-pc"></a>Q. Ho compreso che non è necessario apportare alcuna modifica all'applicazione, ma è difficile usarla con una penna e un discorso. Cosa è possibile fare per ottimizzare l'applicazione per un Tablet PC?

R. I controlli API e input penna dei componenti della piattaforma Tablet PC possono essere utilizzati per creare interfacce utente più adatte all'input penna e grafia. Per ulteriori informazioni su come migliorare l'applicazione, vedere la pagina relativa [alle linee guida sull'esperienza utente per PC portatili per gli sviluppatori](/previous-versions//dd356056(v=vs.85)).

## <a name="q-what-programming-languages-does-the-tablet-support"></a>Q. Quali linguaggi di programmazione supportano il Tablet?

R. La tecnologia Tablet PC in Windows Vista supporta COM (C++) e librerie gestite (la suite di linguaggi Visual Studio .NET).

La tecnologia Tablet PC supporta inoltre Windows Presentation Foundation (WPF).

## <a name="q-do-i-have-sample-code-that-demonstrates-tablet-platform-capabilities"></a>Q. Sono disponibili esempi di codice che illustrano le funzionalità della piattaforma Tablet?

R. Sì, il codice di esempio per COM e i linguaggi gestiti selezionati è incluso nei componenti della piattaforma Tablet PC installati da Windows Platform SDK.

Per le applicazioni di esempio disponibili, vedere:

- [Esempi di PC portatili e Tablet PC](mobile-pc-and-tablet-pc-samples.md)
- [Esempi di input penna digitali, Windows Presentation Foundation (WPF)](/previous-versions/dotnet/netframework-3.0/aa972145(v=vs.85))
- <systemdrive>: \\ Programmi \\ Microsoft SDK \\ Windows \\ v 6.0 \\ esempi \\ TabletPC

## <a name="q-whats-the-base-level-of-tablet-hardware-that-i-should-develop-for"></a>Q. Qual è il livello di base dell'hardware del tablet da sviluppare per?

R. In generale, è consigliabile progettare per un sistema compatibile con Windows Vista, senza precedenti.

## <a name="q-what-user-interface-guidelines-can-you-provide-for-tablet-applications"></a>Q. Quali linee guida dell'interfaccia utente è possibile fornire per le applicazioni Tablet?

R. I problemi dell'orientamento del menu a discesa per lo schermo/digitalizzatore parallasse sono descritti nelle [linee guida sull'esperienza utente del computer mobile per gli sviluppatori](/previous-versions//dd356056(v=vs.85)) nella sezione relativa al computer mobile del Windows SDK.

## <a name="q-do-you-include-system-level-handwriting-gestures-for-commonly-used-keystrokes-can-i-create-my-own-gestures-for-use-when-an-application-is-running-or-has-focus"></a>Q. Si includono i movimenti di grafia a livello di sistema per le sequenze di tasti utilizzate comunemente? È possibile creare movimenti personalizzati da usare quando un'applicazione è in esecuzione o ha lo stato attivo?

R. Sì, è incluso un set di movimenti per gli eventi del mouse. Inoltre, è possibile creare movimenti da usare nell'applicazione. Per ulteriori informazioni sui movimenti, vedere [utilizzo dei movimenti](using-gestures.md).

## <a name="q-how-can-i-determine-whether-my-application-is-running-on-a-tablet"></a>Q. Come è possibile determinare se l'applicazione è in esecuzione in un Tablet?

R. Usare Windows GetSystemMetricsAPI e passare \_ TABLETPC SM come valore dell'indice. Il \_ TABLETPC SM è definito in winuser. h. Il valore di \_ TABLETPC SM è 86.

Per lo sviluppo Web, è necessario leggere la \_ \_ variabile di ambiente stringa agente utente. È possibile accedere alla raccolta Request. ServerVariables.

Per informazioni dettagliate sull'utilizzo di GetSystemMetrics su Tablet PC che eseguono Windows Vista o Windows XP Tablet PC Edition, vedere [determinare se un PC è un Tablet PC](determining-whether-a-pc-is-a-tablet-pc.md).

## <a name="q-how-can-i-determine-whether-tablet-platform-components-are-available"></a>Q. Come è possibile determinare se i componenti della piattaforma Tablet sono disponibili?

R. Alcune parti della piattaforma Tablet PC possono essere installate in versioni non Tablet dei sistemi operativi Windows XP Professional, Windows Server 2003 e Windows 2000.

Il modo corretto per determinare se un componente dell'API è installato consiste nel tentare di creare un'istanza di un oggetto o di un controllo e verificarne l'esistenza prima di provare a utilizzarla.

Per determinare, ad esempio, se l'oggetto [**InkCollector**](inkcollector-class.md) è disponibile, provare a crearlo utilizzando [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

```C++
IInkCollector* pIInkCollector = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkCollector,
 NULL, CLSCTX_INPROC_SERVER, 
 IID_IInkCollector,
 (void **)&pIInkCollector);
if (SUCCEEDED(hr)) 
{ 
  /* InkCollector is usable. */ 
} else 
{
  /* InkCollector unavailable. */
}
```

## <a name="q-how-do-i-run-the-tablet-input-service-on-server-skus"></a>Q. Ricerca per categorie eseguire il servizio di input del tablet in SKU del server?

R. TabletInputService è progettato per non essere eseguito automaticamente negli SKU del server quando viene installato il pacchetto client. Il pacchetto client installa tutti i componenti della piattaforma, in modo che sia possibile eseguire le applicazioni client tablet anche in un server. Il servizio di input del tablet è in ascolto della notifica PnP in cui è collegato un digitalizzatore esterno. Per abilitare il servizio di input di Tablet in un server, utilizzare l'utilità configurazione di sistema.

Dal menu **Start** selezionare **Esegui**. Digitare "msconfig" e premere INVIO. Selezionare la scheda **Servizi** , trovare i servizi denominati "HID Input Service", selezionare la casella di controllo accanto, quindi fare clic su **applica**. Chiudere l'utilità.

## <a name="q-more-faqs-and-other-resources"></a>Q. Altre domande frequenti e altre risorse

- [Centro per sviluppatori Microsoft](https://developer.microsoft.com)
- [Guida di riferimento a Tablet PC Core](./core-reference---tablet-pc-com-library.md)