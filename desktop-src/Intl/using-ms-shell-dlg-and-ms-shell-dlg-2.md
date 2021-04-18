---
description: Utilizzo di MS Shell Dlg e MS Shell Dlg 2
ms.assetid: ac3b57a6-5b92-4366-ad71-c501cec60997
title: Utilizzo di MS Shell Dlg e MS Shell Dlg 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad43f972e776151551fa312ce2bd8ed6d19be58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319480"
---
# <a name="using-ms-shell-dlg-and-ms-shell-dlg-2"></a>Utilizzo di MS Shell Dlg e MS Shell Dlg 2

Windows è disponibile nelle edizioni localizzate per molte lingue. Tuttavia, l'edizione in lingua inglese può essere usata anche per eseguire applicazioni scritte in lingue diverse dall'inglese. Questo vale anche quando lo script usato per questi linguaggi è diverso, ad esempio quando le applicazioni sono scritte in greco o giapponese. Queste applicazioni richiedono un'interfaccia utente con finestre di dialogo, icone e utilità che forniscono informazioni nella lingua dell'applicazione, che potrebbero essere diverse dalla lingua utilizzata nell'interfaccia utente di Windows corrente.

Il problema nella selezione del tipo di carattere per un'interfaccia utente è ovvio. Ad esempio, il tipo di carattere della shell, noto anche come il sistema o il tipo di carattere predefinito, per la lingua inglese (Stati Uniti) Windows 98 è MS Sans Serif, mentre il tipo di carattere della Shell per greco (Grecia) Windows 98 è MS Sans Serif greco. Per il giapponese (Giappone) Windows 98, il tipo di carattere della shell è MS UI Gothic. Non è possibile eseguire il mapping diretto di questi set di caratteri. Sostituendo MS Sans Serif con MS Sans Serif Greek quando le impostazioni locali sono impostate su Greco (Grecia) non è possibile eseguire adeguatamente le applicazioni esistenti o visualizzare caratteri greci nei menu di sistema, nelle finestre di dialogo e nei controlli di modifica.

Windows risolve questo problema utilizzando i tipi di carattere logici MS Shell Dlg e MS Shell Dlg 2 per consentire la selezione del tipo di carattere appropriato per la visualizzazione dello script. In questa sezione vengono illustrate diverse considerazioni di programmazione per l'utilizzo dei tipi di carattere logici per implementare finestre di dialogo, menu e simili per interfacce utente flessibili che vengono visualizzate correttamente in tutti i sistemi operativi Windows supportati e in tutte le lingue. Per ulteriori informazioni, vedere [creazione e selezione di tipi di carattere](../gdi/font-creation-and-selection.md). Per una descrizione dell'uso della tecnologia MUI (Multilingual User Interface) per la creazione di interfacce utente per le applicazioni multilingue, vedere anche [interfaccia utente multilingue](multilingual-user-interface.md) .

## <a name="about-the-logical-fonts"></a>Informazioni sui tipi di carattere logici

I tipi di carattere logici MS Shell Dlg e MS Shell Dlg 2 sono essenzialmente nomi di facet usati per il mapping per consentire il supporto di impostazioni locali/impostazioni cultura contenenti caratteri non contenuti nella tabella codici 1252, il set di caratteri di Windows per il Stati Uniti e l'Europa occidentale. MS Shell Dlg esegue il mapping al tipo di carattere predefinito della shell associato alle impostazioni cultura e alle impostazioni locali correnti e supporta l'aspetto classico del desktop Windows. MS Shell Dlg 2 nome del volto è stato introdotto in Windows 2000 per supportare l'aspetto introdotto con Windows 2000.

Se, ad esempio, l'applicazione utilizza MS Shell Dlg o MS Shell Dlg 2 per le finestre di dialogo, un team di localizzazione che crea risorse in lingua greca per l'applicazione può concentrarsi sulla conversione del testo. Non è necessario preoccuparsi di problemi quali la distinzione tra MS Sans Serif e MS Sans Serif greco.

> [!Note]  
> I tipi di carattere generati da MS Shell Dlg e MS Shell Dlg 2 sono diversi nelle diverse versioni di Windows. Pertanto, è necessario assicurarsi che gli elementi dell'interfaccia utente siano visualizzati correttamente in tutte le piattaforme.

 

## <a name="handle-hard-coded-font-names"></a>Gestire i nomi dei tipi di carattere Hard-Coded

L'utilizzo di Unicode consente alle applicazioni di gestire migliaia di caratteri diversi, ma la maggior parte dei tipi di carattere non copre tutto il set di caratteri Unicode. Le applicazioni non devono avere nomi di carattere hardcoded. Un motivo è che la codifica a livello di codice di un tipo di carattere che Visualizza i caratteri per una lingua e non per un altro linguaggio causa la visualizzazione non corretta di tutto il testo localizzato nel secondo linguaggio. Un altro motivo per evitare i nomi dei tipi di carattere hardcoded è che il tipo di carattere desiderato potrebbe non essere caricato nel sistema operativo che Visualizza il testo dell'applicazione.

Il modo migliore per gestire i nomi dei tipi di carattere è considerarli come risorse localizzabili. L'utilizzo di un tipo di carattere logico consente di risolvere il problema dell'esecuzione dell'interfaccia utilizzando qualsiasi linguaggio in Windows NT o Windows 2000, per qualsiasi lingua. Impostando un nome di tipo di carattere come risorsa localizzabile, il localizzatore può modificare il tipo di carattere per l'interfaccia utente localizzata.

## <a name="handle-hard-coded-font-sizes"></a>Gestire Hard-Coded dimensioni dei tipi di carattere

Alcuni script sono complessi e richiedono un numero elevato di pixel per la visualizzazione corretta. Ad esempio, la maggior parte dei caratteri inglesi viene visualizzata in una griglia 5x7, ma i caratteri giapponesi necessitano almeno di una griglia 16x16 per essere chiaramente visibili. Mentre il cinese necessita di una griglia 24x24, Thai richiede solo 8 pixel per la larghezza ma almeno 22 pixel per l'altezza. È facile capire che alcuni caratteri potrebbero non essere leggibili con una dimensione del carattere ridotta.

L'interfaccia utente dell'applicazione deve considerare le dimensioni del carattere come risorse localizzabili. L'utilizzo di un tipo di carattere logico consente di risolvere il problema dell'esecuzione dell'interfaccia utilizzando qualsiasi linguaggio in Windows NT o Windows 2000, per qualsiasi lingua. Impostando una dimensione del carattere come risorsa localizzabile, il localizzatore può modificare il tipo di carattere per l'interfaccia utente localizzata.

## <a name="map-the-logical-fonts"></a>Mappare i tipi di carattere logici

Ogni carattere logico viene mappato da una voce nel registro di sistema al tipo di carattere della shell appropriato per le impostazioni locali attualmente attive. Quando viene utilizzato uno dei tipi di carattere logici, Windows passa al tipo di carattere per le impostazioni locali attualmente selezionate in fase di esecuzione. Questa operazione consente la visualizzazione corretta dell'interfaccia utente di Windows in lingua inglese (Stati Uniti), nonché dei caratteri non presenti nella tabella codici 1252. In questo modo, attualmente le applicazioni localizzate possono essere eseguite nella versione inglese (Stati Uniti) di Windows senza alcuna modifica.

Ogni computer Windows esegue il mapping di MS Shell Dlg e MS Shell Dlg 2 a un tipo di carattere fisico appropriato, in base alla lingua definita per i programmi non Unicode, descritti nella [terminologia NLS](nls-terminology.md). I mapping effettivi vengono archiviati nella chiave del registro di sistema HKEY \_ Local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ Current Version \\ FontSubstitutes.

### <a name="font-mapping-on-windows-me9895"></a>Mapping dei tipi di carattere in Windows Me/98/95

MS Shell Dlg generalmente esegue il mapping a una versione specifica della tabella codici di MS Sans Serif.

### <a name="font-mapping-on-windows-nt-40"></a>Mapping dei tipi di carattere in Windows NT 4,0

MS Shell Dlg viene mappato a MS Sans Serif per Europa occidentale e centrale, greco, turco, Baltico e lingue con lo script cirillico; MS UI Gothic per giapponese; Gulim per coreano; SimSun per cinese semplificato; PMinglu per il cinese tradizionale; Via.

### <a name="font-mapping-on-windows-2000-windows-xp-windows-server-2003-windows-vista-and-windows-7"></a>Mapping dei tipi di carattere in Windows 2000, Windows XP, Windows Server 2003, Windows Vista e Windows 7

Entrambi i tipi di carattere logici sono associati a tipi di carattere TrueType basati su Unicode. MS Shell Dlg USA Microsoft Sans Serif (distinto da MS Sans Serif) se la lingua di installazione non è giapponese. MS Shell Dlg viene mappato a MS UI Gothic se la lingua di installazione è giapponese.

Nei sistemi MUI Windows XP, MS Shell Dlg viene mappato a MS UI Gothic solo quando le impostazioni locali del sistema e la lingua dell'interfaccia utente sono impostate su giapponese. In caso contrario, MS Shell Dlg esegue il mapping a Microsoft Sans Serif.

In Windows Vista e Windows 7, MS Shell Dlg esegue il mapping a Microsoft UI Gothic se la lingua dell'interfaccia utente predefinita del computer è impostata su giapponese (indipendentemente dalla lingua di installazione). MS Shell Dlg esegue il mapping a Microsoft Sans Serif se la lingua dell'interfaccia utente predefinita del computer è impostata su una lingua diversa dal giapponese.

MS Shell Dlg 2 usa semplicemente il tipo di carattere Tahoma indipendentemente dalla lingua. Il vantaggio principale di Tahoma su Microsoft Sans Serif è che Tahoma ha un tipo di carattere in grassetto nativo. Lo svantaggio principale è che i sistemi operativi precedenti potrebbero non essere installati e potrebbe sostituire un tipo di carattere meno interessante.

I caratteri che non sono implementati in Tahoma o Microsoft Sans Serif possono essere implementati in altri tipi di carattere di Windows utilizzati per la visualizzazione del testo nelle interfacce utente. A seconda di quali controlli o API vengono utilizzati per visualizzare il testo, è possibile che nel sistema vengano utilizzati diversi meccanismi, ad esempio il collegamento dei tipi di [carattere](https://msdn.microsoft.com/globalization/mt662331) , per selezionare automaticamente tali tipi di carattere per la visualizzazione di tali caratteri.

Le applicazioni possono usare Microsoft Sans Serif o Tahoma in modo esplicito e salvare il livello di riferimento indiretto utilizzato in MS Shell Dlg o MS Shell Dlg 2. A causa del collegamento dei tipi di carattere, la specifica di Microsoft Sans Serif o Tahoma fornisce glifi appropriati per tutte le lingue.

## <a name="use-ms-shell-dlg-for-a-non-english-application-on-windows-me9895"></a>Usare MS Shell Dlg per un'applicazione non in lingua inglese in Windows Me/98/95

In Windows Me/98/95, MS Shell Dlg non è destinato all'utilizzo con un'applicazione statica, non in lingua inglese, che viene eseguita quando l'utente ha scelto un'impostazione locale con un set di caratteri di base di Windows diverso. In questo caso, è possibile che la lingua dell'interfaccia utente dell'applicazione non sia supportata con il tipo di carattere che sostituisce MS Shell Dlg.

Se, ad esempio, l'utente utilizza una versione in lingua tedesca di Windows e desidera installare un'applicazione in lingua greca non Unicode, l'utente tenta di modificare le impostazioni locali in greco (Grecia). Questa azione Reimposta MS Shell Dlg su un tipo di carattere greco, ma questo tipo di carattere non contiene tutti i glifi necessari per la visualizzazione in tedesco. Pertanto, tutti i caratteri non ASCII nell'interfaccia utente in lingua tedesca non vengono visualizzati correttamente. Per supportare questo scenario, un'applicazione deve impostare MS Shell Dlg su un tipo di carattere che contiene sia il glifo dell'Europa occidentale che il greco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Selezione e enumerazione dei tipi di carattere internazionali](using-international-fonts-and-text.md)
</dt> <dt>

[Interfaccia utente multilingue](multilingual-user-interface.md)
</dt> </dl>

 

 
