---
title: Uso del controllo Media Player di Windows con Microsoft Visual Studio
description: Uso del controllo Media Player di Windows con Microsoft Visual Studio
ms.assetid: e007876e-f215-4976-8a70-018fedc0e67d
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, .NET Framework
- Modello a oggetti Media Player Windows, .NET Framework
- modello a oggetti, .NET Framework
- Windows Media Player Mobile, .NET Framework
- Windows Media Player ActiveX Control, .NET Framework
- Controllo ActiveX Windows Media Player Mobile, .NET Framework
- Controllo ActiveX, .NET Framework
- Controllo ActiveX di Windows Media Player, Visual Studio
- Controllo ActiveX Windows Media Player Mobile, Visual Studio
- Controllo ActiveX, Visual Studio
- .NET Framework, incorporamento del programma Visual Studio
- incorporamento, programmi di Visual Studio
- Visual Studio, incorporamento del programma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b01fecd6acdfd5ccc9a7d823740ef3915bf9c6
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/21/2019
ms.locfileid: "104045417"
---
# <a name="using-the-windows-media-player-control-with-microsoft-visual-studio"></a>Uso del controllo Media Player di Windows con Microsoft Visual Studio

È possibile aggiungere il controllo ActiveX Windows Media Player 9 o versioni successive a un'applicazione .NET Framework tramite la casella degli strumenti in Visual Studio.

## <a name="adding-the-windows-media-player-control"></a>Aggiunta del controllo Media Player di Windows

Prima di creare un nuovo progetto, assicurarsi che nel computer sia installata la versione più recente di Windows Media Player e Windows Media Player SDK.

Avviare Visual Studio e quindi creare un nuovo progetto.

In Visual Studio aprire la casella degli strumenti.

Se Windows Media Player non viene visualizzato nella parte relativa ai **componenti** della casella degli strumenti, procedere come segue:

1.  Fare clic con il pulsante destro del mouse all'interno della casella degli strumenti e **scegliere Scegli elementi**. Verrà visualizzata la finestra di dialogo **Personalizza casella degli strumenti** .
2.  Nella scheda **componenti com** selezionare Windows Media Player.

    Se Windows Media Player non viene visualizzato nell'elenco, fare clic su **Sfoglia**, quindi aprire Wmp.dll, che dovrebbe trovarsi nella \\ cartella system32 di Windows.

3.  Fare clic su **OK**. Il controllo Media Player Windows verrà inserito nella scheda della casella degli strumenti corrente.

È ora possibile selezionare Windows Media Player nella casella degli strumenti e aggiungerlo a un modulo.

Visual Studio fornisce al controllo Windows Media Player un nome predefinito, ad esempio "axWindowsMediaPlayer1". È possibile modificare il nome in un elemento più facilmente memorizzabile, ad esempio "Player".

L'aggiunta del controllo Windows Media Player dalla casella degli strumenti aggiunge anche riferimenti a due librerie create da Visual Studio, AxWMPLib e WMPLib. È possibile trovarli nel Esplora soluzioni in **riferimenti**.

Per semplificare l'uso degli oggetti nello spazio dei nomi del lettore, è necessario includere lo spazio dei nomi nelle direttive using o Imports dei file, come indicato di seguito:


```Csharp
using WMPLib;
```




```VB
imports WMPLib

```



La direttiva garantisce che sia possibile fare riferimento a oggetti **Player** senza qualificare il nome completo.

> [!Note]  
> Il controllo Media Player Windows è un oggetto **AxWindowsMediaPlayer** dello spazio dei nomi **AxWMPLib** . Tuttavia, la classe **AxWindowsMediaPlayer** usa tipi di dati, interfacce e altri elementi dallo spazio dei nomi **WMPLib** .

 

## <a name="configuring-visibility-of-the-control"></a>Configurazione della visibilità del controllo

Quando si aggiunge per la prima volta il controllo Windows Media Player a un modulo, questo sarà visibile. Se non si vuole usare l'immagine visibile del lettore nell'applicazione, nascondere il lettore predefinito impostando una delle proprietà seguenti:



| Proprietà        | Valore                                                 |
|-----------------|-------------------------------------------------------|
| **uiMode**      | "invisibile" (vedere [Player. uiMode](player-uimode.md).) |
| **Visible**     | "false"                                               |
| **Size. Width**  | 0                                                     |
| **Size. Height** | 0                                                     |



 

È possibile impostare queste proprietà nel codice o nella finestra **Proprietà** quando si seleziona il controllo Media Player Windows nella finestra di progettazione del form.

## <a name="object-model-compatibility-of-the-control"></a>Compatibilità del modello a oggetti del controllo

Il modello a oggetti per il controllo Media Player di Windows è fondamentalmente lo stesso nel .NET Framework come nel codice non gestito e nello script. Tuttavia, esistono differenze nel modo in cui vengono esposti gli elementi:

-   La maggior parte degli oggetti è esposta sotto il nome dell'interfaccia COM sottostante. Ad esempio, l'oggetto **playlist** viene esposto come **IWMPPlaylist**.
-   Alcune interfacce hanno versioni successive. Ad esempio, a **IWMPMedia** sono state assegnate funzionalità aggiuntive in **IWMPMedia2** e **IWMPMedia3**. Se si dichiara un oggetto come **IWMPMedia**, è in genere possibile accedere alla funzionalità di tutte le versioni dell'interfaccia. Tuttavia,® IntelliSense non riconoscerà i metodi o le proprietà delle interfacce di versione successiva e l'editor .NET Visual Basic non correggerà automaticamente le maiuscole. Per sfruttare tutti i vantaggi di IntelliSense e altre funzionalità di Visual Studio, dichiarare l'oggetto usando la versione più recente dell'interfaccia, ad esempio **IWMPMedia3**.
-   Non sono presenti proprietà indicizzate (C#) o proprietà predefinite (Visual Basic .NET). Ad esempio, per recuperare una **playlist. Item**, è necessario chiamare il metodo della funzione di accesso **IWMPlaylist. Get \_ Item** in C# o recuperare la proprietà **IWMPlayist. Item** in Visual Basic .NET.
-   A causa di un conflitto di denominazione tra la proprietà **controlli** Media Player di Windows e la proprietà **controlli** esposti da ogni controllo, la versione del lettore di questa proprietà è denominata **CtlControls** nel contesto del controllo ActiveX. (Tuttavia, questo non avviene quando si crea il lettore a livello di codice anziché come controllo ActiveX).

Usare il Visualizzatore oggetti in Visual Studio per individuare i nomi API corretti per i metodi e gli oggetti negli spazi dei nomi **AxWMPLib** e **WMPLib** .

## <a name="distributing-your-application"></a>Distribuzione dell'applicazione

Quando si distribuisce l'applicazione, assicurarsi di installare AxInterop.WMPLib.dll e Interop.WMPLib.dll nella cartella dell'applicazione. Sarà inoltre necessario assicurarsi che la versione di Windows Media Player richiesta sia installata nel computer dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del controllo Media Player Windows a livello di codice**](creating-the-windows-media-player-control-programmatically.md)
</dt> <dt>

[**Incorporamento del controllo Media Player Windows in una soluzione C#**](embedding-the-windows-media-player-control-in-a-c--solution.md)
</dt> <dt>

[**Incorporamento del controllo Media Player Windows in una soluzione Visual Basic .NET**](embedding-the-windows-media-player-control-in-a-visual-basic--net-solution.md)
</dt> </dl>

 

 




