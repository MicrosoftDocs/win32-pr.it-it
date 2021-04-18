---
description: Interfacce (Windows Runtime C++)
ms.assetid: CB05B5F8-BE15-4BE0-A651-F6E8912D649D
title: Interfacce (Windows Runtime)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f627a77f91417b16d8bfc3e940036910003c40f0
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334006"
---
# <a name="interfaces"></a>Interfacce

## <a name="in-this-section"></a>Contenuto della sezione

| Interfaccia | Descrizione |
|-|-|
| [**IActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iactivatableclassregistration) | Consente di ottenere le informazioni di registrazione per una classe. |
| [**IActivationFactory**](/windows/win32/api/activation/nn-activation-iactivationfactory) | Consente l'attivazione delle classi tramite Windows Runtime. |
| [**IAgileReference**](/windows/desktop/api/objidl/nn-objidl-iagilereference) | Consente di recuperare un riferimento agile a un oggetto. |
| [**IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) | Consente la registrazione di un gestore di notifiche di chiusura dell'Apartment. |
| [**AsyncActionCompletedHandler**](asyncactioncompletedhandler.md) | Rappresenta il metodo chiamato al completamento di un'azione asincrona. |
| [**IAsyncAction**](/windows/win32/api/windows.foundation/nn-windows-foundation-iasyncaction) | Rappresenta un'azione asincrona. |
| [**IAsyncActionProgressHandler<TProgress>**](/previous-versions//br205782(v=vs.85)) | Rappresenta il metodo chiamato quando un'azione asincrona segnala lo stato di avanzamento. |
| [**IAsyncActionWithProgress<TProgress>**](/previous-versions//br205784(v=vs.85)) | Rappresenta un'azione asincrona che segnala lo stato di avanzamento. |
| [**IAsyncActionWithProgressCompletedHandler<TProgress>**](/previous-versions//br205785(v=vs.85)) | Rappresenta il metodo chiamato quando viene completata un'azione asincrona che segnala lo stato di avanzamento. |
| [**IAsyncInfo**](/windows/win32/api/asyncinfo/nn-asyncinfo-iasyncinfo) | Fornisce supporto per le operazioni asincrone. |
| [**IAsyncOperation<TResult>**](/previous-versions//br205802(v=vs.85)) | Rappresenta un'operazione asincrona che restituisce un risultato. |
| [**IAsyncOperationCompletedHandler<TResult>**](/previous-versions//br205803(v=vs.85)) | Rappresenta il metodo chiamato al completamento di un'operazione asincrona. |
| [**IAsyncOperationProgressHandler**](/previous-versions//br205805(v=vs.85)) | Rappresenta il metodo chiamato quando un'operazione asincrona segnala lo stato di avanzamento. |
| [**IAsyncOperationWithProgress**](/previous-versions//br205807(v=vs.85)) | Rappresenta un'operazione asincrona che restituisce un risultato e segnala lo stato. |
| [**IAsyncOperationWithProgressCompletedHandler<TResult, TProgress>**](/previous-versions//br205808(v=vs.85)) | Rappresenta il metodo chiamato quando viene completata un'operazione asincrona che segnala lo stato di avanzamento. |
| [**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative) | Rappresenta un frame di dati audio. |
| [**IAudioFrameNativeFactory**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenativefactory) | Crea istanze di [**IAudioFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-iaudioframenative). |
| [**IBuffer**](/previous-versions//hh438362(v=vs.85)) | Rappresenta una matrice di byte. |
| [**IBufferByteAccess**](/previous-versions//hh846267(v=vs.85)) | Rappresenta un buffer sotto forma di matrice di byte. |
| [**IClosable**](/windows/win32/api/windows.foundation/nn-windows-foundation-iclosable) | Definisce un metodo per il rilascio di risorse allocate. |
| [**ICompositionDrawingSurfaceInterop**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop) | Interfaccia di interoperatività nativa che consente il disegno su un oggetto Surface usando un rettangolo per definire l'area in cui disegnare. |
| [**ICompositionDrawingSurfaceInterop2**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiondrawingsurfaceinterop2) | Interfaccia di interoperatività nativa che consente di leggere il contenuto di una superficie di disegno di composizione o di una superficie di disegno virtuale di composizione. |
| [**ICompositionGraphicsDeviceInterop**](/windows/win32/api/windows.ui.composition.interop/nn-windows-ui-composition-interop-icompositiongraphicsdeviceinterop) | Interfaccia di interoperatività nativa che consente di ottenere e impostare il dispositivo di grafica. |
| [**IContactManagerInterop**](/previous-versions//dn302109(v=vs.85)) | Consente l'accesso ai metodi [**ContactManager**](/uwp/api/Windows.ApplicationModel.Contacts.ContactManager?view=winrt-19041) in un'app che gestisce più finestre. |
| [**ICoreApplication**](/previous-versions//hh438365(v=vs.85)) | Consente alle app di gestire le modifiche dello stato, gestire Windows e integrarsi con un'ampia gamma di Framework dell'interfaccia utente. |
| [**ICoreApplicationExit**](/previous-versions//hh438366(v=vs.85)) | Fornisce i mezzi per arrestare l'esecuzione delle app di Windows Store. |
| [**ICoreApplicationInitialization**](/previous-versions//hh438370(v=vs.85)) | Contiene un metodo Run utilizzato per avviare l'oggetto applicazione dal punto di ingresso di un'applicazione. |
| [**ICoreApplicationView**](/previous-versions//hh438372(v=vs.85)) | Rappresenta una visualizzazione di un'applicazione. |
| [**ICoreImmersiveApplication**](/previous-versions//hh438382(v=vs.85)) | Contiene i metodi per la gestione delle visualizzazioni in un'applicazione. |
| [**ICoreInputInterop**](/windows/desktop/api/corewindow/nn-corewindow-icoreinputinterop) | Abilita un'origine di input in un oggetto [**CoreInput**](https://www.bing.com/search?q=**CoreInput**) di un'app di Windows Store. |
| [**ICoreWindowInterop**](/windows/desktop/api/corewindow/nn-corewindow-icorewindowinterop) | Consente alle app di ottenere la finestra handleof della finestra ([**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041)) associata a questa interfaccia. |
| [**IDllServerActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-idllserveractivatableclassregistration) | Consente di ottenere le informazioni di registrazione per un server in-process. |
| [**IErrorReportingSettings**](/previous-versions//br205818(v=vs.85)) | Fornisce l'integrazione del debugger per applicazioni Windows Runtime. |
| [**IEventHandler<T>**](/previous-versions//hh438385(v=vs.85)) | Rappresenta il metodo che gestirà un evento che dispone di dati di evento di tipo **T**. |
| [**IExeServerActivatableClassRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iexeserveractivatableclassregistration) | Consente di ottenere le informazioni di registrazione per un server out-of-process. |
| [**IExeServerRegistration**](/windows/win32/api/activationregistration/nn-activationregistration-iexeserverregistration) | Rappresenta un server out-of-process registrato. |
| [**IFindReferenceTargetsCallback**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ifindreferencetargetscallback) | Definisce l'interfaccia per i callback di [**IReferenceTracker:: FindTrackerTargets**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nf-windows-ui-xaml-hosting-referencetracker-ireferencetracker-findtrackertargets). L'implementazione di questa interfaccia deve passare tutte le istanze di [**IReferenceTrackerTarget**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget) che trova al metodo **FoundTrackerTarget** . |
| [**IInputPaneInterop**](/windows/desktop/api/inputpaneinterop/nn-inputpaneinterop-iinputpaneinterop) | Consente l'accesso ai membri della classe [**InputPane**](/uwp/api/Windows.UI.ViewManagement.InputPane?view=winrt-19041) in un'applicazione desktop. |
| [**IInputStream**](/previous-versions//hh438387(v=vs.85)) | Consente di ottenere un'operazione di lettura asincrona su un flusso sequenziale di byte. |
| [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable) | Fornisce la funzionalità necessaria per tutte le classi Windows Runtime. |
| [**IIterable<T>**](/previous-versions//br205825(v=vs.85)) | Espone l'iteratore, che supporta l'iterazione semplice su una raccolta di un tipo specificato. |
| [**IIterator<T>**](/previous-versions//br205827(v=vs.85)) | Supporta l'iterazione in una raccolta. |
| [**IKeyValuePair<K, V>**](/previous-versions//br205831(v=vs.85)) | Rappresenta una coppia chiave-valore. |
| [**ILanguageExceptionErrorInfo**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo) | Consente di recuperare il puntatore [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) archiviato nelle informazioni sull'errore con la chiamata a RoOriginateLanguageException. |
| [**ILanguageExceptionErrorInfo2**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo2) | Consente alle proiezioni di linguaggio di fornire e recuperare informazioni sugli errori come con [**ILanguageExceptionErrorInfo**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionerrorinfo), con l'ulteriore vantaggio di lavorare oltre i limiti del linguaggio. |
| [**ILanguageExceptionTransform**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptiontransform) | Consente alle proiezioni di linguaggio di rendere disponibili per il sistema qualsiasi e tutto il contesto da un'eccezione che viene generata dal contesto di un gestore catch che rileva un'eccezione diversa. |
| [**ILanguageExceptionStackBackTrace**](/windows/desktop/api/restrictederrorinfo/nn-restrictederrorinfo-ilanguageexceptionstackbacktrace) | Consente alle proiezioni di fornire analisi dello stack personalizzate per l'eccezione. |
| [**IMap<K, V>**](/previous-versions//br205834(v=vs.85)) | Rappresenta una raccolta associativa. |
| [**IMapChangedEventArgs<K>**](/previous-versions//br205835(v=vs.85)) | Fornisce i dati per un evento [**MapChanged**](/uwp/api/windows.foundation.collections.iobservablemap-2?view=winrt-19041) . |
| [**IMapView<K, V>**](/previous-versions//br205838(v=vs.85)) | Rappresenta una visualizzazione non modificabile in un [**IMAP (K, V)**](/previous-versions//br205834(v=vs.85)). |
| [**IMemoryBufferByteAccess**](/previous-versions//mt297505(v=vs.85)) | Consente di accedere a un [**IMemoryBuffer**](/uwp/api/Windows.Foundation.IMemoryBuffer?view=winrt-19041) come matrice di byte. |
| [**IMetaDataAssemblyImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataassemblyimport) | Fornisce metodi per accedere ed esaminare il contenuto di un manifesto dell'assembly. |
| [**IMetaDataDispenser**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenser) | Fornisce metodi per creare un nuovo ambito di metadati o per aprirne uno esistente. |
| [**IMetaDataDispenserEx**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenserex) | Estende l'interfaccia [**IMetaDataDispenser**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatadispenser) per fornire la possibilità di controllare il funzionamento delle API dei metadati sull'ambito dei metadati corrente. |
| [**IMetaDataImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport) | Fornisce metodi per importare e modificare i metadati esistenti da un file eseguibile portabile (PE) o da un'altra origine, ad esempio una libreria dei tipi o un binario dei metadati di runtime autonomo. |
| [**IMetaDataImport2**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport2) | Estende l'interfaccia [**IMetaDataImport**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadataimport) per fornire la funzionalità di utilizzo di tipi generici. |
| [**IMetaDataTables**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables) | Fornisce metodi per l'archiviazione e il recupero dei metadati nelle tabelle. |
| [**IMetaDataTables2**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables2) | Estende [**IMetaDataTables**](/windows/win32/api/rometadataapi/nn-rometadataapi-imetadatatables) per includere metodi per l'utilizzo di flussi di metadati. |
| [**IObservableMap<K, V>**](/previous-versions//br205851(v=vs.85)) | Notifica ai gestori di eventi le modifiche dinamiche a una mappa, ad esempio quando gli elementi vengono aggiunti o rimossi. |
| [**IObservableVector<T>**](/previous-versions//br205854(v=vs.85)) | Notifica ai gestori di eventi le modifiche apportate al vettore. |
| [**IOplockBreakingHandler**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-ioplockbreakinghandler) | Questa interfaccia non è attualmente implementata. |
| [**IOutputStream**](/previous-versions//hh438390(v=vs.85)) | Consente di ottenere un'operazione di scrittura asincrona su un flusso sequenziale di byte. |
| [**IPdfRendererNative**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) | Rappresenta un'API ad alte prestazioni per la visualizzazione di una singola pagina di un file PDF (Portable Document Format). |
| [**IPackageDebugSettings**](/previous-versions//hh438393(v=vs.85)) | Consente agli sviluppatori del debugger di controllare il ciclo di vita di un'app di Windows Store, ad esempio quando viene sospesa o ripresa. |
| [**IPlayToManagerInterop**](/windows/desktop/api/playtomanagerinterop/nn-playtomanagerinterop-iplaytomanagerinterop) | Consente l'accesso ai metodi [**PlayToManager**](/uwp/api/Windows.Media.PlayTo.PlayToManager?view=winrt-19041) in un'app di Windows Store che gestisce più finestre. |
| [**IPrintManagerInterop**](/windows/desktop/api/printmanagerinterop/nn-printmanagerinterop-iprintmanagerinterop) | Consente l'accesso ai metodi [**PrintManager**](/uwp/api/Windows.Graphics.Printing.PrintManager?view=winrt-19041) in un'app di Windows Store che gestisce più finestre. |
| [**IPropertyValue**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvalue) | Rappresenta un valore in un Windows Runtime archivio delle proprietà. |
| [**IPropertyValueStatics**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvaluestatics) | Crea gli oggetti [**IPropertyValue**](/windows/win32/api/windows.foundation/nn-windows-foundation-ipropertyvalue) che è possibile archiviare in un archivio delle proprietà. |
| [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) | Consente di ottenere un Reader o un writer di byte asincrono posizionato in corrispondenza della posizione specificata in un flusso di byte di accesso casuale. |
| [**IRandomAccessStreamFileAccessMode**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-irandomaccessstreamfileaccessmode) | Consente di accedere alla modalità di accesso ai file usata quando è stato chiamato il metodo [**StorageFile. OpenAsync**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) per aprire il flusso di byte ad accesso casuale. |
| [**IReference<T>**](/previous-versions//br224583(v=vs.85)) | Consente di estendere il sistema di proprietà Windows Runtime per enumerazioni, strutture e tipi delegati definiti dall'utente. |
| [**IReferenceArray<T>**](/previous-versions//br224584(v=vs.85)) | Consente di estendere il sistema di proprietà Windows Runtime per le matrici di enumerazioni, strutture e tipi delegati definiti dall'utente. |
| [**IReferenceTracker**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker) | Definisce l'interfaccia implementata dal framework XAML per la gestione dei riferimenti agli oggetti XAML. |
| [**IReferenceTrackerHost**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackerhost) | Definisce un'interfaccia che fornisce i servizi globali utilizzati dal sistema Garbage Collection (GC) utilizzato dal framework XAML. |
| [**IReferenceTrackerManager**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackermanager) | Definisce l'interfaccia per un gestore di riferimenti a un oggetto XAML. Implementare questa interfaccia per gestire le istanze di [**IReferenceTracker**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetracker) sugli oggetti XAML. |
| [**IReferenceTrackerTarget**](/windows/win32/api/windows.ui.xaml.hosting.referencetracker/nn-windows-ui-xaml-hosting-referencetracker-ireferencetrackertarget) | Definisce un'interfaccia implementata da un oggetto Garbage Collector a cui viene fatto riferimento da XAML. |
| [**IRestrictedErrorInfo**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) | Rappresenta i dettagli di un errore, incluse le informazioni sull'errore limitate. |
| [**ISoftwareBitmapNative**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative) | Rappresenta una bitmap software. |
| [**ISoftwareBitmapNativeFactory**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnativefactory) | Crea istanze di [**ISoftwareBitmapNative**](/windows/desktop/api/windows.graphics.imaging.interop/nn-windows-graphics-imaging-interop-isoftwarebitmapnative). |
| [**IStorageFolderHandleAccess**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-istoragefolderhandleaccess) | Consente di accedere all'handle del sistema operativo di una cartella di archiviazione. |
| [**IStorageItemHandleAccess**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-istorageitemhandleaccess) | Consente di accedere all'handle del sistema operativo di un file di archiviazione. |
| [**IStringable**](/windows/win32/api/windows.foundation/nn-windows-foundation-istringable) | Fornisce un modo per rappresentare l'oggetto corrente come stringa. |
| [**ISurfaceImageSourceManagerNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcemanagernative) | Consente di eseguire operazioni bulk in tutti gli oggetti [**SurfaceImageSource**](/uwp/api/Windows.UI.Xaml.Media.Imaging.SurfaceImageSource?view=winrt-19041) creati nello stesso processo. |
| [**ISurfaceImageSourceNativeWithD2D**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenativewithd2d) | Fornisce l'implementazione di una superficie Microsoft DirectX condivisa che viene visualizzata in un [**SurfaceImageSource**](/uwp/api/Windows.UI.Xaml.Media.Imaging.SurfaceImageSource?view=winrt-19041) o [**VirtualSurfaceImageSource**](/uwp/api/Windows.UI.Xaml.Media.Imaging.VirtualSurfaceImageSource?view=winrt-19041). |
| [**ISurfaceImageSourceNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-isurfaceimagesourcenative) | Fornisce l'implementazione di una superficie a dimensione fissa condivisa per il disegno Direct2D. |
| [**ISuspendingDeferral**](isuspendingdeferral.md) | Gestisce un'operazione di sospensione dell'app ritardata. |
| [**ISuspendingEventArgs**](isuspendingeventargs.md) | Fornisce i dati per un evento di sospensione dell'app. |
| [**ISuspendingOperation**](isuspendingoperation.md) | Fornisce informazioni su un'operazione di sospensione dell'app. |
| [**ISwapChainBackgroundPanelNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainbackgroundpanelnative) | Fornisce l'interoperatività tra XAML e una catena di scambio DirectX. |
| [**ISwapChainPanelNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative) | Fornisce l'interoperatività tra XAML e una catena di scambio DirectX. A differenza di [**SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel?view=winrt-19041), un **SwapChainPanel** può comparire a qualsiasi livello nell'albero di visualizzazione XAML e più di 1 può essere presente in un determinato albero. |
| [**ISwapChainPanelNative2**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-iswapchainpanelnative2) | Fornisce l'interoperatività tra XAML e una catena di scambio DirectX. A differenza di [**SwapChainBackgroundPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel?view=winrt-19041), un **SwapChainPanel** può comparire a qualsiasi livello nell'albero di visualizzazione XAML e più di 1 può essere presente in un determinato albero. |
| [**ITypedEventHandler<TSender, TArgs>**](/previous-versions//hh438424(v=vs.85)) | Rappresenta il metodo che gestirà un evento da un mittente di tipo **TSender** e i dati dell'evento di tipo **T**. |
| [**IUnbufferedFileHandleOplockCallback**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleoplockcallback) | Definisce un metodo di callback che si desidera eseguire quando il blocco opportunistico per un handle ottenuto chiamando il metodo [**IUnbufferedFileHandleProvider:: OpenUnbufferedFileHandle**](/windows/desktop/api/windowsstoragecom/nf-windowsstoragecom-iunbufferedfilehandleprovider-openunbufferedfilehandle) è danneggiato. |
| [**IUnbufferedFileHandleProvider**](/windows/desktop/api/windowsstoragecom/nn-windowsstoragecom-iunbufferedfilehandleprovider) | Fornisce l'accesso agli handle da un flusso di byte ad accesso casuale creato dal metodo [**StorageFile. OpenAsync**](/uwp/api/Windows.Storage.StorageFile?view=winrt-19041) . |
| [**IVector<T>**](/previous-versions//br224590(v=vs.85)) | Rappresenta una raccolta di elementi ad accesso casuale. |
| [**IVectorChangedEventArgs**](ivectorchangedeventargs.md) | Fornisce i dati per un evento [**VectorChanged**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) . |
| [**IVectorView<T>**](/previous-versions//br224594(v=vs.85)) | Rappresenta una visualizzazione non modificabile in un [**IVector (T)**](/uwp/api/windows.foundation.collections.ivector-1?view=winrt-19041). |
| [**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative) | Rappresenta un frame di dati video. |
| [**IVideoFrameNativeFactory**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenativefactory) | Crea istanze di [**IVideoFrameNative**](/windows/desktop/api/windows.media.core.interop/nn-windows-media-core-interop-ivideoframenative). |
| [**IViewProvider**](/previous-versions//hh438426(v=vs.85)) | Rappresenta una visualizzazione in un'applicazione. |
| [**IViewProviderFactory**](/previous-versions//hh438427(v=vs.85)) | Crea un'istanza di viste che implementano l'interfaccia [**IViewProvider**](/previous-versions//hh438426(v=vs.85)) . |
| [**IVirtualSurfaceImageSourceNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative) | Fornisce l'implementazione di una superficie condivisa grande (maggiore della dimensione dello schermo) per il disegno DirectX. |
| [**IVirtualSurfaceUpdatesCallbackNative**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceupdatescallbacknative) | Fornisce un'interfaccia per l'implementazione dei comportamenti di disegno quando un [**VirtualSurfaceImageSource**](/windows/desktop/api/windows.ui.xaml.media.dxinterop/nn-windows-ui-xaml-media-dxinterop-ivirtualsurfaceimagesourcenative) richiede un aggiornamento. |
| [**IWeakReference**](/windows/win32/api/weakreference/nn-weakreference-iweakreference) | Rappresenta un riferimento debole a un oggetto. |
| [**IWeakReferenceSource**](/windows/win32/api/weakreference/nn-weakreference-iweakreferencesource) | Rappresenta un oggetto di origine a cui è possibile recuperare un riferimento debole. |
| [**MapChangedEventHandler<K, V>**](/previous-versions//br224612(v=vs.85)) | Rappresenta il metodo che gestisce l'evento [**MapChanged**](/uwp/api/windows.foundation.collections.iobservablemap-2?view=winrt-19041) di un mapping osservabile. |
| [**VectorChangedEventHandler<T>**](/previous-versions//br224626(v=vs.85)) | Rappresenta il metodo che gestisce l'evento [**VectorChanged**](/uwp/api/windows.foundation.collections.iobservablevector-1?view=winrt-19041) di un vettore osservabile. |
