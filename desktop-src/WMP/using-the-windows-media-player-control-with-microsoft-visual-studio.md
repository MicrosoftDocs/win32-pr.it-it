---
title: Uso del controllo Windows Media Player con Microsoft Visual Studio
description: Uso del controllo Windows Media Player con Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Windows Media Player,incorporamento ActiveX controllo
- Windows Media Player a oggetti, incorporamento ActiveX controllo
- modello a oggetti, incorporamento ActiveX controllo
- Windows Media Player Mobile, incorporamento ActiveX controllo
- Windows Media Player ActiveX, incorporamento
- Windows Media Player Controllo ActiveX per dispositivi mobili, incorporamento
- ActiveX, incorporamento
- Windows Media Player,.NET Framework
- Windows Media Player a oggetti, .NET Framework
- modello a oggetti, .NET Framework
- Windows Media Player Mobile,.NET Framework
- Windows Media Player ActiveX controllo, .NET Framework
- Windows Media Player Controllo ActiveX per dispositivi mobili, .NET Framework
- ActiveX controllo, .NET Framework
- Windows Media Player ActiveX controllo, Visual Studio
- Windows Media Player Controllo ActiveX per dispositivi mobili, Visual Studio
- ActiveX controllo, Visual Studio
- .NET Framework,Visual Studio programma incorporato
- incorporamento, Visual Studio programmi
- Visual Studio,incorporamento del programma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73bb9597b8ad5baadbd51625c68a1d7fb7ebc1791c2d6e8015fb79ba2cab3be6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830450"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a>Uso del controllo Windows Media Player con Microsoft Visual Studio

È possibile aggiungere il controllo Windows Media Player Serie 9 o successiva ActiveX a un'applicazione .NET Framework tramite la casella degli strumenti in Visual Studio.

## <a name="adding-the-windows-media-player-control"></a>Aggiunta del controllo Windows Media Player controllo

Prima di creare un nuovo progetto, assicurarsi che nel computer sia installata la versione più recente di Windows Media Player e Windows Media Player SDK.

Avviare Visual Studio, quindi creare un nuovo progetto.

In Visual Studio aprire la casella degli strumenti.

Se Windows Media Player non viene visualizzato nella parte **Componenti** della casella degli strumenti, eseguire le operazioni seguenti:

1.  Fare clic con il pulsante destro del mouse nella casella degli strumenti e **quindi scegliere Scegli elementi**. Verrà visualizzata la **finestra di dialogo Personalizza casella** degli strumenti .
2.  Nella scheda **Componenti COM** selezionare Windows Media Player.

    Se Windows Media Player non viene visualizzato nell'elenco, fare clic su Sfoglia e quindi aprire Wmp.dll, che dovrebbe essere nella cartella Windows  \\ System32.

3.  Fare clic su **OK**. Il Windows Media Player controllo verrà inserito nella scheda casella degli strumenti corrente.

È ora possibile selezionare Windows Media Player nella casella degli strumenti e aggiungerlo a un form.

Visual Studio assegna al Windows Media Player un nome predefinito, ad esempio "axWindowsMediaPlayer1". È possibile modificare il nome in un nome più facilmente ricordabile, ad esempio "Player".

L'aggiunta Windows Media Player controllo dalla casella degli strumenti aggiunge anche riferimenti a due librerie create da Visual Studio, AxWMPLib e WMPLib. È possibile trovarli nel Esplora soluzioni in **Riferimenti**.

Per semplificare l'uso degli oggetti nello spazio dei nomi Player, è necessario includere lo spazio dei nomi nelle direttive using o imports dei file, come indicato di seguito:


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



La direttiva garantisce che sia possibile fare riferimento agli **oggetti Player** senza qualificarne completamente i nomi.

> [!Note]  
> Il Windows Media Player è un **oggetto AxWindowsMediaPlayer** dello spazio **dei nomi AxWMPLib.** Tuttavia, la **classe AxWindowsMediaPlayer** usa tipi di dati, interfacce e altri elementi dello spazio **dei nomi WMPLib.**

 

## <a name="configuring-visibility-of-the-control"></a>Configurazione della visibilità del controllo

La prima volta che si aggiunge Windows Media Player controllo a un form, questo sarà visibile. Se non si vuole usare l'immagine visibile del lettore nell'applicazione, nascondere il lettore predefinito impostando una delle proprietà seguenti:



| Proprietà        | Valore                                                 |
|-----------------|-------------------------------------------------------|
| **uiMode**      | "invisible" (vedere [Player.uiMode](player-uimode.md)).) |
| **Visible**     | "false"                                               |
| **Size.Width**  | 0                                                     |
| **Size.Height** | 0                                                     |



 

È possibile impostare queste proprietà nel codice o **nella** finestra Proprietà quando il controllo Windows Media Player selezionato nella finestra di progettazione form.

## <a name="object-model-compatibility-of-the-control"></a>Compatibilità del modello a oggetti del controllo

Il modello a oggetti per Windows Media Player controllo è fondamentalmente lo stesso nella .NET Framework come nel codice e nello script non gestiti. Esistono tuttavia differenze nella modalità di esposizione degli elementi:

-   La maggior parte degli oggetti viene esposta sotto il nome dell'interfaccia COM sottostante. Ad esempio, **l'oggetto Playlist** viene esposto come **IWMPPlaylist.**
-   Alcune interfacce hanno versioni successive. Ad esempio, **A IWMPMedia** ha fornito funzionalità aggiuntive in **IWMPMedia2** e **IWMPMedia3.** Se si dichiara un oggetto **come IWMPMedia,** in genere si ha accesso alle funzionalità di tutte le versioni dell'interfaccia. IntelliSense® tuttavia, non riconoscerà i metodi o le proprietà delle interfacce di versioni successive e l'editor .NET Visual Basic non correggerà automaticamente l'uso di maiuscole e minuscole. Per ottenere il vantaggio completo di IntelliSense e di altre funzionalità di Visual Studio, dichiarare l'oggetto usando la versione più recente dell'interfaccia, ad esempio **IWMPMedia3.**
-   Non sono disponibili proprietà indicizzate (C#) o proprietà predefinite (Visual Basic .NET). Ad esempio, per recuperare **un oggetto Playlist.item,** è necessario chiamare il metodo della funzione di accesso **IWMPlaylist.get \_ Item** in C# o recuperare la proprietà **IWMPlayist.Item** in Visual Basic .NET.
-   A causa di un conflitto di denominazione tra la proprietà Windows Media Player **Controls** e la proprietà **Controls** esposta da ogni controllo, la versione Player di questa proprietà è denominata **CtlControls** nel contesto del controllo ActiveX controllo. Questo non è tuttavia il caso in cui si crea Player a livello di codice anziché come ActiveX controllo.

Usare visualizzatore oggetti in Visual Studio per individuare i nomi API corretti per metodi e oggetti negli spazi dei nomi **AxWMPLib** e **WMPLib.**

## <a name="distributing-your-application"></a>Distribuzione dell'applicazione

Quando si distribuisce l'applicazione, assicurarsi di installare AxInterop.WMPLib.dll e Interop.WMPLib.dll nella cartella dell'applicazione. È anche necessario assicurarsi che la versione Windows Media Player installata nel computer dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del controllo Windows Media Player a livello di codice**](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[**Incorporamento del controllo Windows Media Player in una soluzione C#**](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[**Incorporamento del controllo Windows Media Player in una Visual Basic .NET**](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




