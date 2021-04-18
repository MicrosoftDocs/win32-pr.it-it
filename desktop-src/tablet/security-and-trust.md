---
description: .NET Framework prevede modello di sicurezza che tratta le applicazioni in modo diverso a seconda della relativa origine.
ms.assetid: 37fa870a-6f38-44ae-943e-27697f6b9fba
title: Sicurezza e attendibilità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4e3039f8aa93c2ae563a918177462cd09a217af
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "106320391"
---
# <a name="security-and-trust"></a>Sicurezza e attendibilità

.NET Framework prevede modello di sicurezza che tratta le applicazioni in modo diverso a seconda della relativa origine. Gli eseguibili e gli assembly provenienti dal computer di un utente vengono in genere eseguiti con attendibilità totale; gli stessi eseguibili e gli stessi assembly vengono eseguiti su Internet in genere con attendibilità parziale. Ciò consente di evitare che il codice dannoso possa leggere o modificare le informazioni a cui non dovrebbe accedere, ad esempio file locali, elementi negli Appunti e altre risorse. Se un eseguibile chiama un assembly, che a sua volta chiama un altro assembly che richiede un certo livello di attendibilità, viene applicato il livello di attendibilità più basso di tutti i componenti della catena. Tuttavia, un amministratore di un computer può impostare autorizzazioni specifiche che eseguono l'override delle autorizzazioni predefinite.

Una panoramica del modello di sicurezza viene fornita in [controlli Client-Side protetti, Light-Weight](/archive/msdn-magazine/2002/january/dhtml-and-net-host-secure-lightweight-client-side-controls-in-microsoft-internet-explorer)ed è possibile ottenere più approfondimenti sul modello di sicurezza in [pratica nella sicurezza dall'accesso di codice](/previous-versions/msp-n-p/ff648663(v=pandp.10)). Una panoramica efficace sulla sicurezza delle librerie, che è particolarmente importante per gli oggetti [**UserControl**](/uwp/api/Windows.UI.Xaml.Controls.UserControl?view=winrt-19041) in una pagina Web, è reperibile in [uso di librerie da codice parzialmente attendibile](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconusinglibrariesfrompartiallytrustedcode.asp)e altre informazioni sulla sicurezza sui controlli gestiti sono disponibili nella pagina relativa alla [scrittura di controlli gestiti protetti](/documentation/?url=%2flibrary%2fcpguide%2fhtml%2fcpconwritingsecuremanagedcontrols.asp%3fframe%3dtrue).

## <a name="permissions"></a>Autorizzazioni

La maggior parte degli oggetti e dei membri gestiti nell'API delle tecnologie Tablet PC presenta due requisiti:

-   L'esecuzione è sempre obbligatoria.
-   FullTrust è necessario quando viene eseguita l'azione di sicurezza [InheritanceDemand](/previous-versions/windows/) . Ciò significa che l'attendibilità totale è necessaria quando una classe derivata eredita una classe o esegue l'override di un metodo da Tablet PC SDK.

Nella tabella seguente sono elencate le classi e i membri che richiedono autorizzazioni aggiuntive. Le autorizzazioni per una determinata classe si applicano anche a tutti i membri non elencati in questa tabella.



| Classe o metodo                                                                       | Autorizzazioni                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-canpaste)                                                  | [UIPermissionClipboard. AllClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink. ClipboardCopy**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardcopy)                                    | [UIPermissionClipboard. OwnClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**Ink. ClipboardPaste**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdisp-clipboardpaste)                                  | [UIPermissionClipboard. AllClipboard](/dotnet/api/system.security.permissions.uipermissionclipboard?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                           |
| [**InkCollector**](inkcollector-class.md)                                            | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| InkCollector (IntPtr)                                                                  | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| InkCollector. handle                                                                   | [UIPermissionWindow. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) (vedere la nota di seguito)<br/> |
| InkEdit                                                                               | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [InkOverlay](/previous-versions/ms552322(v=vs.100))                                   | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| InkOverlay (IntPtr)                                                                    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e SecurityPermissionFlag. UnmanagedCode<br/>                                                                 |
| [InkOverlay. handle](/previous-versions/ms833109(v=msdn.10))                      | [UIPermissionWindow. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) (vedere la nota di seguito)<br/> |
| [InkPicture](/previous-versions/aa514604(v=msdn.10))                                   | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| [PenInputPanel](/previous-versions/aa514041(v=msdn.10))                             | Vedere la nota che segue.<br/>                                                                                                                                                                                     |
| [**InkRenderer**](inkrenderer-class.md)                                              | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-draw) [ **DrawStroke**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-drawstroke)        | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| Renderer. InkSpaceToPixel (IntPtr, Point), renderer. InkSpaceToPixel (IntPtr, Point \[ \] )    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| Renderer. PixelToInkSpace (IntPtr, Point), renderer. PixelToInkSpace (IntPtr, Point \[ \] )    | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**DynamicRenderer**](/previous-versions/windows/desktop/legacy/ms701168(v=vs.85))                                      | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1)<br/>                                                                                                          |
| DynamicRenderer (IntPtr)                                                               | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>         |
| [**RealTimeStylus**](realtimestylus-class.md)                                        | [UIPermissionWindow. SafeTopLevelWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true)<br/>                                                                                                          |
| RealTimeStylus (IntPtr), RealTimeStylus (IntPtr, Boolean), RealTimeStylus (IntPtr, tablet) | [UIPermissionWindow. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/)<br/>                  |



 

> [!Note]  
> In genere è preferibile usare un controllo anziché un handle (IntPtr) per i costruttori, perché i controlli richiedono un minor numero di autorizzazioni. Analogamente, è preferibile usare un oggetto Graphics anziché un handle per [renderer. disegnato](/previous-versions/ms828488(v=msdn.10)), [renderer. InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) e [renderer. PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)).

 

> [!Note]  
> Le proprietà [InkCollector. handle](/previous-versions/ms836504(v=msdn.10)) e [InkOverlay. handle](/previous-versions/ms833109(v=msdn.10)) non richiedono l'autorizzazione [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) se l'handle è per un controllo Windows Form, ma per altre finestre.

 

> [!Note]  
> Per la [Classe PenInputPanel](/previous-versions/aa514041(v=msdn.10)) , i metodi e le proprietà seguenti [richiedono SecurityPermissionFlag. AllFlags](/previous-versions/windows/): PenInputPanel (IntPtr), [AttachedEditWindow](/previous-versions/ms582240(v=vs.100)), [busy](/previous-versions/ms571975(v=vs.100)), [CommitPendingInput](/previous-versions/ms569650(v=vs.100)), [CurrentPanel](/previous-versions/ms571976(v=vs.100)), [DefaultPanel](/previous-versions/ms571977(v=vs.100)), EnableTsf [, controllo](/previous-versions/ms571978(v=vs.100))dell' [altezza](/previous-versions/ms571979(v=vs.100)), [HorizontalOffset](/previous-versions/ms571980(v=vs.100)), [InputFailed](/previous-versions/ms567738(v=vs.100)), [Left](/previous-versions/ms571981(v=vs.100)), [MoveTo](/previous-versions/ms569667(v=vs.100)), [PanelChanged](/previous-versions/ms567741(v=vs.100)), [PanelMoving](/previous-versions/ms567748(v=vs.100)), [Refresh](/previous-versions/ms569778(v=vs.100)), [Top](/previous-versions/ms571982(v=vs.100)), [VerticalOffset](/previous-versions/ms571983(v=vs.100)), [Visible](/previous-versions/ms571984(v=vs.100)), [VisibleChanged](/previous-versions/ms567754(v=vs.100))e [Width](/previous-versions/ms571985(v=vs.100)). [](/previous-versions/ms569656(v=vs.100))

 

## <a name="other-considerations"></a>Altre considerazioni

Di seguito sono riportate alcune considerazioni sulla sicurezza note:

-   Microsoft Internet Explorer 6 o versione successiva è necessario per consentire il corretto funzionamento dei controlli Web. Con Internet Explorer 5,5, vengono caricati solo i controlli gestiti iniziali; non è possibile caricare controlli aggiuntivi in modo dinamico in fase di esecuzione.
-   Se si utilizza Windows XP Service Pack 2 (SP2) e CLR 1.0, la presenza di controlli Web in Internet Explorer richiede l'aggiunta del sito come sito attendibile, anche se si trovano nell'area Intranet. Tuttavia, quando si esegue questa operazione, non verranno più eseguiti nell'area sito attendibile, sebbene vengano eseguiti nell'area Intranet. Questo problema è stato risolto con CLR 1.1.

 

 