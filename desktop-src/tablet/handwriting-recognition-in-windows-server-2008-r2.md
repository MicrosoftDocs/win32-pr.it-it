---
description: Windows Server 2008 R2 aggiunge il supporto per il riconoscimento della grafia lato server in Windows. Questo argomento descrive come riconoscere la grafia in Windows Server 2008 R2.
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Riconoscimento della grafia in Windows Server 2008 R2
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047559"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a>Riconoscimento della grafia in Windows Server 2008 R2

Windows Server 2008 R2 supporta il riconoscimento della grafia lato server. Il riconoscimento lato server consente a un server di riconoscere il contenuto dall'input penna nelle pagine Web. Questa operazione è particolarmente utile quando gli utenti in una rete specificano i termini che vengono interpretati utilizzando un dizionario personalizzato. Se, ad esempio, si dispone di un'applicazione medica che esegue una query su un database del server per i nomi dei pazienti, questi nomi possono essere aggiunti a un altro database a cui si fa riferimento incrociato quando si eseguono ricerche da un modulo Silverlight scritto a mano.

## <a name="set-up-your-server-for-server-side-recognition"></a>Configurare il server per il riconoscimento Server-Side

Attenersi alla procedura seguente per configurare il riconoscimento lato server.

- Installa Servizi di riconoscimento della grafia
- Installare il supporto per server Web (IIS) e server applicazioni
- Abilitare il ruolo esperienza desktop
- Avviare il servizio di input di Tablet PC

### <a name="install-ink-and-handwriting-services"></a>Installa Servizi di riconoscimento della grafia

Per installare i servizi di input penna e grafia, aprire Server Manager facendo clic sull'icona Server Manager nella barra di avvio veloce. Scegliere **Aggiungi funzionalità** dal menu **funzionalità** . Assicurarsi di selezionare la casella di controllo **servizi di riconoscimento della grafia** . Nella figura seguente è illustrata la finestra di dialogo **Seleziona funzionalità** con **servizi di riconoscimento della grafia** selezionata.

![Finestra di dialogo Seleziona funzionalità con servizi di input penna e grafia selezionati casella di controllo](images/setup-server-1-ink-and-handwriting.png)<br/>
*Finestra di dialogo Seleziona funzionalità con servizi di input penna e grafia selezionati casella di controllo*

### <a name="installation-support-for-web-server-iis-and-application-server"></a>Supporto dell'installazione per server Web (IIS) e server applicazioni

Aprire Server Manager come per il primo passaggio. Successivamente, sarà necessario aggiungere i ruoli server Web (IIS) e server applicazioni. Dal menu **ruoli** fare clic su **Aggiungi ruoli**. Verrà visualizzata l'aggiunta guidata ruoli. Fare clic su **Avanti**. Verificare che il **server applicazioni** e il **server Web (IIS)** siano selezionati. Nella figura seguente è illustrata la finestra di dialogo **Selezione ruoli server** con i ruoli server **Web (IIS)** e **server applicazioni** selezionati.

![Finestra di dialogo Selezione ruoli server con i ruoli server Web (IIS) e server applicazioni selezionati](images/setup-server-2-select-server-roles.png)<br/>
*Finestra di dialogo Selezione ruoli server con i ruoli server Web (IIS) e server applicazioni selezionati*

Quando si seleziona **server applicazioni**, verrà richiesto di installare ASP.NET Framework. Fare clic sul pulsante **Aggiungi funzionalità necessarie** . Dopo aver fatto clic su **Avanti**, verrà visualizzata una finestra di dialogo panoramica. fare clic su **Avanti**. A questo punto la finestra di dialogo **Selezione servizi ruolo** dovrebbe essere disponibile. Verificare che il **server Web (IIS)** sia selezionato. Nella figura seguente viene illustrata la finestra di dialogo **Selezione servizi ruolo** con server Web (IIS) abilitato.

![Finestra di dialogo Selezione servizi ruolo con server Web (IIS) abilitato](images/setup-server-3-select-role-services.png)<br/>
*Finestra di dialogo Selezione servizi ruolo con server Web (IIS) abilitato*

Fare clic su **Avanti**. Verrà visualizzata una finestra di dialogo Panoramica; fare di nuovo clic su **Avanti** . A questo punto verrà visualizzata una pagina che offre le opzioni per i ruoli per il server Web (IIS). Fare clic su **Avanti**. Nella pagina successiva il pulsante **Installa** diventerà attivo. Fare clic su **Installa** per installare il supporto per server Web (IIS) e server applicazioni.

### <a name="enable-the-desktop-experience-role"></a>Abilitare il ruolo esperienza desktop

Per abilitare l'esperienza desktop, fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione** e quindi fare clic su **Server Manager**. Selezionare **Aggiungi servizi** e quindi selezionare il servizio **esperienza desktop** . Nella figura seguente viene illustrata la finestra di dialogo **Seleziona funzionalità** con l'elemento esperienza desktop installato.

![Finestra di dialogo Seleziona funzionalità con servizio esperienza desktop selezionato](images/setup-server-4-desktop-experience.png)<br/>
*Finestra di dialogo Seleziona funzionalità con servizio esperienza desktop selezionato*

Fare clic su **Avanti** per installare l'esperienza desktop.

### <a name="start-the-tablet-service"></a>Avviare il servizio Tablet

Dopo aver installato il servizio esperienza desktop, il servizio di input di Tablet PC verrà visualizzato nel menu **Servizi** . Per accedere al menu **Servizi** , fare clic sul pulsante **Start**, scegliere **strumenti di amministrazione**, quindi fare clic su **Servizi**. Per avviare il servizio, fare clic con il pulsante destro del mouse su **servizio di input di Tablet PC** e quindi scegliere **Avvia**. La figura seguente mostra il menu **Servizi** con il servizio di input di Tablet PC avviato.

![Menu dei servizi con il servizio di input di Tablet PC avviato](images/setup-server-5-tablet-pc-input-service.png)<br/>
*Menu dei servizi con il servizio di input di Tablet PC avviato*

## <a name="performing-server-side-recognition-using-silverlight"></a>Esecuzione del riconoscimento Server-Side tramite Silverlight

In questa sezione viene illustrato come creare un'applicazione Web che utilizza Silverlight per acquisire l'input della grafia. Usare la procedura seguente per programmare il riconoscimento in Visual Studio 2008.

- Installare e aggiornare Visual Studio 2008 per aggiungere il supporto per Silverlight.
- Creare un nuovo progetto Silverlight in Visual Studio 2008.
- Aggiungere i riferimenti al servizio necessari per il progetto.
- Creare un servizio WCF Silverlight per il riconoscimento dell'input penna.
- Aggiungere il riferimento al servizio al progetto client.
- Aggiungere la classe InkCollector al progetto InkRecognition.
- Rimuovere le direttive del trasporto protetto dalla configurazione client

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a>Installare e aggiornare Visual Studio 2008 per aggiungere il supporto per Silverlight

Prima di iniziare, è necessario eseguire i passaggi seguenti nel server Windows Server 2008 R2.

- Installare Visual Studio 2008.
- Installare [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).
- Installare [Microsoft Silverlight 5 SDK](https://www.microsoft.com/silverlight/).

Al termine dell'installazione di queste applicazioni e degli aggiornamenti, è possibile creare un'applicazione Web di riconoscimento lato server.

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a>Creare un nuovo progetto Web Silverlight in Visual Studio 2008

Scegliere **Nuovo progetto** dal menu **File**. Selezionare il modello applicazione Silverlight dall'elenco di progetti Visual C \# . Assegnare al progetto il nome InkRecognition e fare clic su **OK**. La figura seguente mostra il \# progetto Silverlight C selezionato e denominato InkRecognition.

![\#progetto Silverlight c selezionato con il nome InkRecognition](images/project-1-new-project.png)<br/>
*\#progetto Silverlight c selezionato con il nome InkRecognition*

Dopo aver fatto clic su **OK**, viene visualizzata una finestra di dialogo in cui viene richiesto di aggiungere un'applicazione Silverlight al progetto. Selezionare **Aggiungi un nuovo progetto Web ASP.NET alla soluzione per ospitare Silverlight** e fare clic su **OK**. Nell'immagine seguente viene illustrato come configurare il progetto di esempio prima di fare clic su **OK**.

![Finestra di dialogo con la richiesta per l'aggiunta di un'applicazione Silverlight a un progetto](images/project-2-add-a-new-aspnetproject.png)<br/>
*Finestra di dialogo con la richiesta per l'aggiunta di un'applicazione Silverlight a un progetto*

### <a name="add-the-necessary-service-references-to-your-project"></a>Aggiungere i riferimenti al servizio necessari al progetto

A questo punto è disponibile un progetto client Silverlight generico (InkRecognition) con un progetto Web (InkRecognition. Web) configurato nella soluzione. Il progetto viene aperto con Page. XAML e default. aspx aperti. Chiudere le finestre e aggiungere i riferimenti System. Runtime. Serialization e System. ServiceModel al progetto InkRecognition facendo clic con il pulsante destro del mouse sulla cartella riferimenti nel progetto InkRecognition e scegliendo **Aggiungi riferimento**. Nella figura seguente viene illustrata la finestra di dialogo con i riferimenti necessari selezionati.

![Finestra di dialogo Aggiungi riferimenti con System. Runtime. Serialization e System. ServiceModel selezionati](images/project-3a-add-references-to-inkreco.png)<br/>
*Finestra di dialogo Aggiungi riferimenti con System. Runtime. Serialization e System. ServiceModel selezionati*

Successivamente, è necessario aggiungere i riferimenti System. ServiceModel e Microsoft. Ink al progetto InkRecognition. Web. Per impostazione predefinita, il riferimento a Microsoft. Ink non verrà visualizzato nei riferimenti .NET, quindi cercare Microsoft.Ink.dll nella cartella Windows. Dopo aver individuato la DLL, aggiungere l'assembly ai riferimenti del progetto: selezionare la scheda **Sfoglia** , passare alla cartella contenente Microsoft.Ink.dll, selezionare Microsoft.Ink.dll, quindi fare clic su **OK**. Nell'immagine seguente viene illustrata la soluzione del progetto in Esplora risorse con tutti gli assembly di riferimento aggiunti.

![progetto InkRecognition in Esplora risorse con tutti gli assembly di riferimento aggiunti](images/project-3b-with-reference-assemblies.png)<br/>
*progetto InkRecognition in Esplora risorse con tutti gli assembly di riferimento aggiunti*

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a>Creare un servizio WCF Silverlight per il riconoscimento dell'input penna

Successivamente, verrà aggiunto un servizio WCF per il riconoscimento dell'input penna al progetto. Fare clic con il pulsante destro del mouse sul progetto InkRecognition. Web, scegliere **Aggiungi**, quindi fare clic su **nuovo elemento**. Selezionare il modello di servizio WCF Silverlight, modificare il nome in InkRecogitionService, quindi fare clic su **Aggiungi**. Nella figura seguente viene illustrata la finestra di dialogo **Aggiungi nuovo elemento** con il servizio WCF Silverlight selezionato e denominato.

![Finestra di dialogo Aggiungi nuovo elemento con servizio WCF Silverlight selezionato e denominato](images/project-4-add-wcf-service.png)<br/>
*Finestra di dialogo Aggiungi nuovo elemento con servizio WCF Silverlight selezionato e denominato*

Dopo aver aggiunto il servizio WCF Silverlight, si aprirà il code-behind del servizio, InkRecognitionService. cs. Sostituire il codice del servizio con il codice seguente.

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = "")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a>Aggiungere il riferimento al servizio al progetto client

Ora che è disponibile il servizio WCF Silverlight per InkRecognition, si utilizzerà il servizio dell'applicazione client. Fare clic con il pulsante destro del mouse sul progetto InkRecognition e selezionare **Aggiungi riferimento al servizio**. Nella finestra di dialogo **Aggiungi riferimento al servizio** visualizzata selezionare **individua** per individuare i servizi dalla soluzione corrente. InkRecognitionService verrà visualizzato nel riquadro servizi. Fare doppio clic su InkRecognitionService nel riquadro servizi, impostare lo spazio dei nomi su InkRecognitionServiceReference e quindi fare clic su **OK**. Nella figura seguente viene illustrata la finestra di dialogo **Aggiungi riferimento al servizio** con InkRecognitionService selezionato e lo spazio dei nomi modificato.

![Finestra di dialogo Aggiungi riferimento al servizio con inkrecognitionservice selezionato e spazio dei nomi modificato](images/project-5-discover-service-reference.png)<br/>
*Finestra di dialogo Aggiungi riferimento al servizio con inkrecognitionservice selezionato e spazio dei nomi modificato*

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a>Aggiungere la classe InkCollector al progetto InkRecognition

Fare clic con il pulsante destro del mouse sul progetto InkRecognition, scegliere **Aggiungi** e quindi fare clic su **nuovo elemento**. Dal menu **Visual C \#** Selezionare **\# classe c**. Denominare la classe InkCollector. Nella figura seguente viene illustrata la finestra di dialogo con la \# classe C selezionata e denominata.

![Finestra di dialogo Aggiungi nuovo elemento con \# classe c selezionata e denominata](images/project-6-add-ink-collector.png)<br/>
*Finestra di dialogo Aggiungi nuovo elemento con \# classe c selezionata e denominata*

Dopo aver aggiunto la classe InkCollector, viene aperta la definizione della classe. Sostituire il codice nell'agente di raccolta input penna con il codice seguente.

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a>Aggiornare XAML per la pagina predefinita e aggiungere un code-behind per il riconoscimento della grafia

Ora che è disponibile una classe che raccoglie l'input penna, sarà necessario aggiornare il codice XAML in page. XAML con il codice XAML seguente. Il codice seguente aggiunge una sfumatura gialla all'area di input, un controllo InkCanvas e un pulsante che attiverà il riconoscimento.

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

Sostituire la pagina code-behind, Page. XAML. cs, con il codice seguente che aggiungerà un gestore dell'evento per il pulsante **Recognize** .

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a>Rimuovere le direttive del trasporto protetto dalla configurazione client

Prima di poter utilizzare il servizio WCF, è necessario rimuovere tutte le opzioni di trasporto protette dalla configurazione del servizio perché i trasporti protetti non sono attualmente supportati nei servizi WCF di Silverlight 2,0. Dal progetto InkRecognition aggiornare le impostazioni di sicurezza in ServiceReferences. ClientConfig. Modificare il codice XML di sicurezza da

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

in

```XML
       <security mode="None"/>
```

A questo punto, l'applicazione deve essere eseguita. Nell'immagine seguente viene illustrato il modo in cui l'applicazione esamina awebpagewith parte della grafia immessa nella casella di riconoscimento.

![Applicazione all'interno di awebpagewith di una grafia immessa nella casella di riconoscimento](images/demo-1.png)<br/>
*Applicazione all'interno di awebpagewith di una grafia immessa nella casella di riconoscimento*

Nell'immagine seguente viene illustrato il testo riconosciuto nell'elenco a discesa **risultato** .

![Applicazione all'interno del testo riconosciuto awebpagewith nell'elenco a discesa risultato](images/demo-2.png)<br/>
*Applicazione all'interno del testo riconosciuto awebpagewith nell'elenco a discesa risultato*

 

 



