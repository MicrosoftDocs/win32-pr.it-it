---
description: Uso di MS Shell Dlg e MS Shell Dlg 2
ms.assetid: ac3b57a6-5b92-4366-ad71-c501cec60997
title: Uso di MS Shell Dlg e MS Shell Dlg 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c29b6f45267ee9f123e5a6dddcd044d667fbe4553af8b3f580edd633b2293ef2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389508"
---
# <a name="using-ms-shell-dlg-and-ms-shell-dlg-2"></a>Uso di MS Shell Dlg e MS Shell Dlg 2

Windows è disponibile nelle edizioni localizzate per molte lingue. Tuttavia, l'edizione in lingua inglese può essere usata anche per eseguire applicazioni scritte in lingue diverse dall'inglese. Questo vale anche quando lo script usato per queste lingue è diverso, come quando le applicazioni vengono scritte in greco o giapponese. Queste applicazioni richiedono un'interfaccia utente con finestre di dialogo, icone e utilità che forniscono informazioni nella lingua dell'applicazione, che potrebbe essere diversa da quella usata nell'interfaccia utente Windows corrente.

Il problema nella selezione del tipo di carattere per un'interfaccia utente è ovvio. Ad esempio, il tipo di carattere della shell, noto anche come tipo di carattere predefinito o di sistema, per l'inglese (Stati Uniti) Windows 98 è MS Sans Serif, mentre il tipo di carattere della shell per greco (Greco) Windows 98 è MS Sans Serif greco. Per il giapponese (Giappone) Windows 98, il tipo di carattere della shell è MS UI Japanese. Questi set di caratteri non possono essere mappati direttamente tra loro. La sostituzione di MS Sans Serif con MS Sans Serif Greco quando le impostazioni locali sono impostate su Greco (Greco) non consente alle applicazioni esistenti di essere eseguite in modo adeguato o di visualizzare i caratteri greci nei menu di sistema, nelle finestre di dialogo e nei controlli di modifica.

Windows risolvere questo problema usando i tipi di carattere logici MS Shell Dlg e MS Shell Dlg 2 per consentire la selezione del tipo di carattere appropriato per la visualizzazione dello script. Questa sezione tratta diverse considerazioni di programmazione per l'uso dei tipi di carattere logici per implementare finestre di dialogo, menu e simili per interfacce utente flessibili che vengono visualizzate correttamente in tutti i sistemi operativi Windows supportati e in tutti i linguaggi. Per altre informazioni, vedere Creazione e selezione [dei tipi di carattere](../gdi/font-creation-and-selection.md). Vedere anche [interfaccia utente multilingue](multilingual-user-interface.md) per una descrizione dell'uso della tecnologia interfaccia utente multilingue (MUI) nella creazione di interfacce utente per le applicazioni multilingue.

## <a name="about-the-logical-fonts"></a>Informazioni sui tipi di carattere logici

I tipi di carattere logici MS Shell Dlg e MS Shell Dlg 2 sono essenzialmente nomi di visi usati per il mapping per abilitare il supporto per impostazioni locali/impostazioni cultura con caratteri non contenuti nella tabella codici 1252, il set di caratteri Windows per il Stati Uniti e l'Europa occidentale. MS Shell Dlg esegue il mapping al tipo di carattere predefinito della shell associato alle impostazioni cultura/impostazioni locali correnti e supporta l'aspetto Windows desktop classico. Il nome del viso MS Shell Dlg 2 è stato introdotto nel Windows 2000 per supportare l'aspetto introdotto con Windows 2000.

Ad esempio, se l'applicazione usa MS Shell Dlg o MS Shell Dlg 2 per le finestre di dialogo, un team di localizzazione che crea risorse in lingua greco per l'applicazione può concentrarsi sulla traduzione del testo. Non devono preoccuparsi di problemi come la distinzione tra MS Sans Serif e MS Sans Serif Greek.

> [!Note]  
> I tipi di carattere generati da MS Shell Dlg e MS Shell Dlg 2 sono diversi in Windows versioni. È quindi necessario assicurarsi che gli elementi dell'interfaccia utente siano visualizzati in tutte le piattaforme.

 

## <a name="handle-hard-coded-font-names"></a>Gestire i Hard-Coded dei tipi di carattere

L'uso di Unicode consente alle applicazioni di gestire migliaia di caratteri diversi, ma la maggior parte dei tipi di carattere non copre tutto il set di caratteri Unicode. Le applicazioni non devono codificare a livello di codice i nomi dei tipi di carattere. Un motivo è che la codifica hard-coding di un nome di carattere che visualizza i caratteri per una lingua e non i caratteri per un'altra lingua causa la visualizzazione non corretta di tutto il testo localizzato nella seconda lingua. Un altro motivo per non impostare come hard-code i nomi dei tipi di carattere è che il tipo di carattere desiderato potrebbe non essere caricato nel sistema operativo che visualizza il testo dell'applicazione.

Il modo migliore per considerare i nomi dei tipi di carattere è considerarli come risorse localizzabili. L'uso di un tipo di carattere logico risolve il problema dell'esecuzione dell'interfaccia usando qualsiasi lingua Windows NT o Windows 2000, per qualsiasi lingua. L'impostazione di un nome di carattere come risorsa localizzabile consente al localizzatore di modificare il tipo di carattere per l'interfaccia utente localizzata.

## <a name="handle-hard-coded-font-sizes"></a>Gestire le dimensioni Hard-Coded carattere

Alcuni script sono complessi e richiedono un numero elevato di pixel per la corretta visualizzazione. Ad esempio, la maggior parte dei caratteri inglesi viene visualizzata su una griglia 5x7, ma i caratteri giapponesi devono avere almeno una griglia 16x16 per essere chiaramente visualizzati. Mentre il cinese necessita di una griglia 24x24, il tailandese richiede solo 8 pixel per la larghezza, ma almeno 22 pixel per l'altezza. È facile comprendere che alcuni caratteri potrebbero non essere leggibili con dimensioni del carattere ridotte.

L'interfaccia utente dell'applicazione deve considerare le dimensioni dei caratteri come risorse localizzabili. L'uso di un tipo di carattere logico risolve il problema dell'esecuzione dell'interfaccia usando qualsiasi lingua Windows NT o Windows 2000, per qualsiasi lingua. L'impostazione di una dimensione del carattere come risorsa localizzabile consente al localizzatore di modificare il tipo di carattere per l'interfaccia utente localizzata.

## <a name="map-the-logical-fonts"></a>Eseguire il mapping dei tipi di carattere logici

Ognuno dei tipi di carattere logici viene mappato da una voce nel Registro di sistema al tipo di carattere della shell appropriato per le impostazioni locali attualmente attive. Quando si usa uno dei tipi di carattere logici, Windows il tipo di carattere per le impostazioni locali attualmente selezionate in fase di esecuzione. Questa operazione consente la visualizzazione corretta dell'interfaccia utente inglese (Stati Uniti) Windows, nonché dei caratteri non presenti nella tabella codici 1252. Le applicazioni localizzate attualmente disponibili possono quindi essere eseguite nella versione inglese (Stati Uniti) di Windows senza modifiche.

Ogni Windows esegue il mapping di MS Shell Dlg e MS Shell Dlg 2 a un tipo di carattere fisico appropriato, in base alla lingua definita per i programmi non Unicode, descritta in Terminologia [NLS.](nls-terminology.md) I mapping effettivi vengono archiviati nella chiave del Registro di sistema HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ \\ FontSubstitutes versione corrente.

### <a name="font-mapping-on-windows-me9895"></a>Mapping dei caratteri Windows me/98/95

MS Shell Dlg viene in genere mappato a una versione specifica della tabella codici di MS Sans Serif.

### <a name="font-mapping-on-windows-nt-40"></a>Mapping dei tipi di carattere Windows NT 4.0

MS Shell Dlg esegue il mapping a MS Sans Serif per l'Europa occidentale e centrale, il greco, il turco, il paesino e le lingue usando lo script cirillico; MS UI Gothic for Japanese; Gulim per il coreano; Simsun per il cinese semplificato; PMinglu per il cinese tradizionale; and so on.

### <a name="font-mapping-on-windows-2000-windows-xp-windows-server-2003-windows-vista-and-windows-7"></a>Mapping dei caratteri Windows 2000, Windows XP, Windows Server 2003, Windows Vista e Windows 7

Entrambi i tipi di carattere logici vengono mappati ai tipi di carattere TrueType basati su Unicode. MS Shell Dlg usa Microsoft Sans Serif (distinto da MS Sans Serif) se la lingua di installazione non è il giapponese. MS Shell Dlg esegue il mapping a MS UI Japanese se la lingua di installazione è giapponese.

Nei Windows MUI XP, MS Shell Dlg esegue il mapping a MS UI Japanese solo quando le impostazioni locali del sistema e la lingua dell'interfaccia utente sono impostate sul giapponese. In caso contrario, MS Shell Dlg esegue il mapping a Microsoft Sans Serif.

In Windows Vista e Windows 7, MS Shell Dlg esegue il mapping a MS UI Japanese se la lingua predefinita dell'interfaccia utente del computer è impostata sul giapponese (indipendentemente dalla lingua di installazione). MS Shell Dlg esegue il mapping a Microsoft Sans Serif se la lingua predefinita dell'interfaccia utente del computer è impostata su una lingua diversa dal giapponese.

MS Shell Dlg 2 usa semplicemente il tipo di carattere Tahoma indipendentemente dalla lingua. Il vantaggio principale di Tahoma rispetto a Microsoft Sans Serif è che Tahoma ha un carattere in grassetto nativo. Lo svantaggio principale è che nei sistemi operativi meno recenti potrebbe non essere installato e potrebbe sostituire un tipo di carattere meno interessante.

I caratteri non implementati in Tahoma o Microsoft Sans Serif possono essere implementati in altri tipi di carattere Windows usati per la visualizzazione del testo nelle interfacce utente. A seconda dei controlli o delle API usati per visualizzare [](https://msdn.microsoft.com/globalization/mt662331) il testo, il sistema può usare vari meccanismi, ad esempio il collegamento dei tipi di carattere, per selezionare automaticamente tali tipi di carattere per la visualizzazione di tali caratteri.

Le applicazioni possono usare In modo esplicito Microsoft Sans Serif o Tahoma e salvare il livello di riferimento indiretto interessato dall'uso di MS Shell Dlg o MS Shell Dlg 2. A causa del collegamento del tipo di carattere, specificando Microsoft Sans Serif o Tahoma vengono forniti glifi appropriati per tutte le lingue.

## <a name="use-ms-shell-dlg-for-a-non-english-application-on-windows-me9895"></a>Usare MS Shell Dlg per un'applicazione non in lingua inglese in Windows Me/98/95

In Windows Me/98/95, MS Shell Dlg non è destinato all'uso con un'applicazione dell'interfaccia utente statica non inglese che viene eseguita quando l'utente ha scelto impostazioni locali con un set di caratteri di base Windows diverso. In questo caso, la lingua dell'interfaccia utente dell'applicazione potrebbe non essere supportata con il tipo di carattere sostituito da MS Shell Dlg.

Ad esempio, se l'utente usa una versione in lingua tedesca di Windows e vuole installare un'applicazione non Unicode in lingua greco, l'utente tenta di modificare le impostazioni locali in greco (Greco). Questa azione reimposta MS Shell Dlg su un tipo di carattere greco, ma questo tipo di carattere non contiene tutti i glifi necessari per la visualizzazione in tedesco. Pertanto, tutti i caratteri non ASCII nell'interfaccia utente in lingua tedesca non verranno visualizzati correttamente. Per supportare questo scenario, un'applicazione deve impostare MS Shell Dlg su un tipo di carattere che contiene sia l'Europa occidentale che i glifi greci.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Enumerazione e selezione dei caratteri internazionali](using-international-fonts-and-text.md)
</dt> <dt>

[Interfaccia utente multilingue](multilingual-user-interface.md)
</dt> </dl>

 

 
