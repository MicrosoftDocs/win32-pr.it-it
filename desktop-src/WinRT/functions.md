---
description: Riferimento per le funzioni di Windows Runtime C++.
ms.assetid: 3D60C81F-B1CC-4485-B7C3-B1C6E903865B
title: Funzioni (Windows Runtime)
ms.topic: article
ms.date: 05/10/2019
ms.openlocfilehash: 1ed2ea39385ac5cb7afc34770a5ee2d2a572bb8b
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334005"
---
# <a name="functions-windows-runtime-c-reference"></a>Funzioni (riferimenti per Windows Runtime C++)

## <a name="in-this-section"></a>Contenuto della sezione



| Funzione | Descrizione |
|-|-|
| [**CoDecodeProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-codecodeproxy) | Individua l'implementazione di un'interfaccia Component Object Model (COM) in un processo server data un'interfaccia a un oggetto proxy. |
| [**CreateControlInput**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinput) | Crea un oggetto [**ICoreInputSourceBase**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) nel thread UI del chiamante. |
| [**CreateControlInputEx**](/windows/desktop/api/corewindow/nf-corewindow-createcontrolinputex) | Crea un oggetto [**ICoreInputSourceBase**](/uwp/api/Windows.UI.Core.ICoreInputSourceBase?view=winrt-19041) in un thread di lavoro o nel thread dell'interfaccia utente.  |
| [**CreateDirect3D11DeviceFromDXGIDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11devicefromdxgidevice) | Crea un'istanza di IDirect3DDevice da un IDXGIDevice. |
| [**CreateDirect3D11SurfaceFromDXGISurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3d11surfacefromdxgisurface) | Crea un'istanza di IDirect3DSurface da un IDXGISurface. |
| [**CreateDirect3DDevice**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3ddevice) | Crea un'istanza di [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) da un [IDXGIDevice](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice). |
| [**CreateDirect3DSurface**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-createdirect3dsurface) | Crea un'istanza di [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) da un [IDXGISurface](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface). |
| [**CreateRandomAccessStreamOnFile**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamonfile) | Crea un Windows Runtime flusso di accesso casuale per un file. |
| [**CreateRandomAccessStreamOverStream**](/windows/win32/api/shcore/nf-shcore-createrandomaccessstreamoverstream) | Crea un Windows Runtime flusso di accesso casuale intorno a un'implementazione di base di [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) . |
| [**CreateStreamOverRandomAccessStream**](/windows/win32/api/shcore/nf-shcore-createstreamoverrandomaccessstream) | Crea un oggetto [**IStream**](/windows/win32/api/objidl/nn-objidl-istream) intorno a un oggetto Windows Runtime [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) . |
| [**CreateXamlUIPresenter**](createxamluipresenter.md) | Funzione creatrice statica che può creare un [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) per una superficie di rendering in un'applicazione desktop. |
| [**DbgRaiseAssertionFailure**](/previous-versions//jj635749(v=vs.85)) | Genera un'asserzione per il debug.  |
| [**GetDXGIInterface (IDirect3DDevice ^, DXGI_TYPE**) * *](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface) | Recupera un'interfaccia DXGI da un'istanza di [IDirect3DDevice](/uwp/api/windows.graphics.directx.direct3d11.idirect3ddevice) . |
| [**GetDXGIInterface (IDirect3DSurface ^, DXGI_TYPE**) * *](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterface-r1) | Recupera un'interfaccia DXGI da un'istanza di [IDirect3DSurface](/uwp/api/windows.graphics.directx.direct3d11.idirect3dsurface) . |
| [**GetDXGIInterfaceFromObject**](/windows/desktop/api/windows.graphics.directx.direct3d11.interop/nf-windows-graphics-directx-direct3d11-interop-getdxgiinterfacefromobject) | Recupera un'interfaccia DXGI da un oggetto. |
| [**GetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-getrestrictederrorinfo) | Ottiene l'oggetto informazioni sull'errore limitato impostato da una chiamata precedente a [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) nel thread logico corrente. |
| [**\_USERFREE HString**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree) | Libera le risorse sul lato server quando vengono chiamate dai file stub RPC. |
| [**\_USERFREE64 HString**](/windows/win32/api/inspectable/nf-inspectable-hstring_userfree64) | Libera le risorse sul lato server quando vengono chiamate dai file stub RPC.  |
| [**\_USERMARSHAL HString**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal) | Esegue il marshalling di un oggetto [**HString**](hstring.md) nel buffer RPC. |
| [**\_USERMARSHAL64 HString**](/windows/win32/api/inspectable/nf-inspectable-hstring_usermarshal64) | Esegue il marshalling di un oggetto [**HString**](hstring.md) nel buffer RPC. |
| [**\_USERSIZE HString**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize) | Calcola la dimensione in transito dell'oggetto [**HString**](hstring.md) e ottiene il relativo handle e i dati. |
| [**\_USERSIZE64 HString**](/windows/win32/api/inspectable/nf-inspectable-hstring_usersize64) | Calcola la dimensione in transito dell'oggetto [**HString**](hstring.md) e ottiene il relativo handle e i dati. |
| [**\_USERUNMARSHAL HString**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal) | Esegue l'unmarshalling di un oggetto [**HString**](hstring.md) dal buffer RPC. |
| [**\_USERUNMARSHAL64 HString**](/windows/win32/api/inspectable/nf-inspectable-hstring_userunmarshal64) | Esegue l'unmarshalling di un oggetto [**HString**](hstring.md) dal buffer RPC. |
| [**IsErrorPropagationEnabled**](/windows/win32/api/roerrorapi/nf-roerrorapi-iserrorpropagationenabled) | Indica se si verifica l'evento [**CoreApplication. UnhandledErrorDetected**](/uwp/api/Windows.ApplicationModel.Core.CoreApplication?view=winrt-19041) per gli errori restituiti dal delegato registrato come funzione di callback per un evento API Windows Runtime o il completamento di un metodo asincrono. |
| [**DllGetActivationFactory**](/previous-versions//br205771(v=vs.85)) | Recupera la factory di attivazione da una DLL che contiene attivabile Windows Runtime classi. |
| [**MetaDataGetDispenser**](/windows/win32/api/rometadata/nf-rometadata-metadatagetdispenser) | Crea una classe del dispenser. |
| [**PdfCreateRenderer**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfcreaterenderer) | Ottiene un'istanza dell'interfaccia [**IPdfRendererNative**](/windows/desktop/api/windows.data.pdf.interop/nn-windows-data-pdf-interop-ipdfrenderernative) per la visualizzazione di una singola pagina di un file PDF (Portable Document Format). |
| [**PdfRenderParams**](/windows/desktop/api/windows.data.pdf.interop/nf-windows-data-pdf-interop-pdfrenderparams) | Popola un [**\_ \_ params di rendering PDF**](/windows/desktop/api/windows.data.pdf.interop/ns-windows-data-pdf-interop-pdf_render_params) struttura. Una \_ \_ struttura di parametri di rendering PDF rappresenta un set di proprietà per l'output di una singola pagina di un file PDF. |
| [**RoActivateInstance**](/windows/win32/api/roapi/nf-roapi-roactivateinstance) | Attiva la classe Windows Runtime specificata. |
| [**RoCaptureErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rocaptureerrorcontext) | Salva il contesto di errore corrente in modo che sia disponibile per le chiamate successive alla funzione [**RoFailFastWithErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) . |
| [**RoClearError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roclearerror) | Rimuove le informazioni sugli errori esistenti dal blocco dell'ambiente del thread corrente (TEB). |
| [**RoFailFastWithErrorContext**](/windows/win32/api/roerrorapi/nf-roerrorapi-rofailfastwitherrorcontext) | Genera un'eccezione non continuabile nel processo corrente. |
| [**RoFailFastWithErrorContextInternal2**](./roerrorapi/nf-roerrorapi-rofailfastwitherrorcontextinternal2.md) | Genera un'eccezione non continuabile nel processo corrente e consente anche di includere un contesto di errore aggiuntivo non ancora acquisito dal sistema operativo. |
| [**RoFreeParameterizedTypeExtra**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rofreeparameterizedtypeextra) | Libera l'handle allocato da [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid). |
| [**RoGetActivatableClassRegistration**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetactivatableclassregistration) | Consente di recuperare le informazioni di registrazione della classe. |
| [**RoGetActivationFactory**](/windows/win32/api/roapi/nf-roapi-rogetactivationfactory) | Ottiene la factory di attivazione per la classe di runtime specificata. |
| [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) | Crea un riferimento agile per un oggetto specificato dall'interfaccia specificata. |
| [**RoGetApartmentIdentifier**](/windows/win32/api/roapi/nf-roapi-rogetapartmentidentifier) | Ottiene un identificatore univoco per l'Apartment corrente. |
| [**RoGetBufferMarshaler**](/windows/win32/api/robuffer/nf-robuffer-rogetbuffermarshaler) | Fornisce un gestore di marshalling IBuffer standard per implementare la semantica associata all'interfaccia IBuffer quando viene sottoposta a marshalling. |
| [**RoGetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-rogeterrorreportingflags) | Ottiene il comportamento di Reporting corrente delle funzioni di errore Windows Runtime. |
| [**RoGetMetaDataFile**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-rogetmetadatafile) | Individua e recupera il file di metadati che descrive l'interfaccia ABI (Application Binary Interface) per il TypeName specificato. |
| [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) | Calcola l'identificatore di interfaccia (IID) dell'interfaccia o del tipo delegato risultante quando viene creata un'istanza di un'interfaccia o un delegato con parametri con gli argomenti di tipo specificati. |
| [**RoGetServerActivatableClasses**](/windows/win32/api/roregistrationapi/nf-roregistrationapi-rogetserveractivatableclasses) | Recupera le classi attivabile registrate per un determinato server eseguibile (EXE), registrato con l'ID del pacchetto del processo chiamante. |
| [**RoInitialize**](/windows/win32/api/roapi/nf-roapi-roinitialize) | Inizializza il Windows Runtime sul thread corrente con il modello di concorrenza specificato. |
| [**RoInspectThreadErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectthreaderrorinfo) | Ottiene l'oggetto Error che rappresenta lo stack di chiamate nel punto in cui ha avuto origine l'errore. |
| [**RoInspectCapturedStackBackTrace**](/windows/win32/api/roerrorapi/nf-roerrorapi-roinspectcapturedstackbacktrace) | Consente ai debugger di controllare uno stack di chiamate da un processo di destinazione. |
| [**RoOriginateError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerror) | Segnala un errore e una stringa informativa a un debugger collegato. |
| [**RoOriginateErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginateerrorw) | Segnala un errore e una stringa informativa a un debugger collegato. |
| [**RoOriginateLanguageException**](/windows/win32/api/roerrorapi/nf-roerrorapi-rooriginatelanguageexception) | Segnala un errore, una stringa informativa e un oggetto Error a un debugger collegato. |
| [**RoParameterizedTypeExtraGetTypeSignature**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-roparameterizedtypeextragettypesignature) | Ottiene la firma del tipo utilizzata per calcolare l'IID dall'ultima chiamata a [**RoGetParameterizedTypeInstanceIID**](/windows/win32/api/roparameterizediid/nf-roparameterizediid-rogetparameterizedtypeinstanceiid) con l'handle specificato. |
| [**RoParseTypeName**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roparsetypename) | Analizza un nome di tipo e i parametri di tipo esistenti, nel caso di tipi con parametri. |
| [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) | Registra un array Factory di attivazione out-of-process per un server Windows Runtime exe. |
| [**RoRegisterForApartmentShutdown**](/windows/win32/api/roapi/nf-roapi-roregisterforapartmentshutdown) | Registra un callback [**IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) da richiamare quando l'Apartment corrente viene arrestato. |
| [**RoReportUnhandledError**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportunhandlederror) | Attiva il gestore degli errori globale quando si verifica un'eccezione non gestita. |
| [**RoReportFailedDelegate**](/windows/win32/api/roerrorapi/nf-roerrorapi-roreportfaileddelegate) | Attiva il gestore degli errori globale quando si verifica un errore del delegato. |
| [**RoResolveNamespace**](/windows/win32/api/rometadataresolution/nf-rometadataresolution-roresolvenamespace) | Determinare gli elementi figlio, i tipi e i sottospazi dei nomi diretti dello spazio dei nomi Windows Runtime specificato, da qualsiasi linguaggio di programmazione supportato dal Windows Runtime. |
| [**RoResolveRestrictedErrorInfoReference**](/windows/win32/api/roerrorapi/nf-roerrorapi-roresolverestrictederrorinforeference) | Restituisce il puntatore all'interfaccia [**IRestrictedErrorInfo**](/windows/desktop/api/RestrictedErrorInfo/nn-restrictederrorinfo-irestrictederrorinfo) in base al riferimento specificato. |
| [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) | Rimuove una matrice di Factory di attivazione registrate dalla Windows Runtime. |
| [**RoSetErrorReportingFlags**](/windows/win32/api/roerrorapi/nf-roerrorapi-roseterrorreportingflags) | Imposta il comportamento di Reporting delle funzioni di errore Windows Runtime. |
| [**RoTransformError**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerror) | Segnala un errore modificato e una stringa informativa a un debugger collegato. |
| [**RoTransformErrorW**](/windows/win32/api/roerrorapi/nf-roerrorapi-rotransformerrorw) | Segnala un errore trasformato e una stringa informativa a un debugger collegato. |
| [**RoUninitialize**](/windows/win32/api/roapi/nf-roapi-rouninitialize) | Chiude il Windows Runtime sul thread corrente. |
| [**RoUnregisterForApartmentShutdown**](/windows/win32/api/roapi/nf-roapi-rounregisterforapartmentshutdown) | Annulla la registrazione di un'interfaccia [**IApartmentShutdown**](/windows/desktop/api/objidl/nn-objidl-iapartmentshutdown) registrata in precedenza. |
| [**SetRestrictedErrorInfo**](/windows/win32/api/roerrorapi/nf-roerrorapi-setrestrictederrorinfo) | Imposta l'oggetto informazioni sull'errore limitato per il thread corrente. |
| [**WindowsCompareStringOrdinal**](/windows/win32/api/winstring/nf-winstring-windowscomparestringordinal) | Confronta due oggetti [**HString**](hstring.md) specificati e restituisce un intero che ne indica la posizione relativa in un ordinamento. |
| [**WindowsConcatString**](/windows/win32/api/winstring/nf-winstring-windowsconcatstring) | Concatena due stringhe specificate. |
| [**WindowsCreateString**](/windows/win32/api/winstring/nf-winstring-windowscreatestring) | Crea un nuovo [**HString**](hstring.md) in base alla stringa di origine specificata. |
| [**WindowsCreateStringReference**](/windows/win32/api/winstring/nf-winstring-windowscreatestringreference) | Crea un nuovo riferimento a una stringa basata sulla stringa specificata. |
| [**WindowsDeleteString**](/windows/win32/api/winstring/nf-winstring-windowsdeletestring) | Decrementa il conteggio dei riferimenti di un buffer di stringa. |
| [**WindowsDeleteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowsdeletestringbuffer) | Elimina un buffer di stringa preallocato se non è stato promosso a [**HString**](hstring.md). |
| [**WindowsDuplicateString**](/windows/win32/api/winstring/nf-winstring-windowsduplicatestring) | Crea una copia della stringa specificata. |
| [**WindowsGetStringLen**](/windows/win32/api/winstring/nf-winstring-windowsgetstringlen) | Ottiene la lunghezza, in caratteri Unicode, della stringa specificata. |
| [**WindowsGetStringRawBuffer**](/windows/win32/api/winstring/nf-winstring-windowsgetstringrawbuffer) | Ottiene il buffer di supporto per la stringa specificata. |
| [**WindowsInspectString**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring) | Consente ai debugger di visualizzare il valore di un Windows Runtime [**HString**](hstring.md) in un altro spazio di indirizzi, in modalità remota o da un dump.  |
| [**WindowsInspectString2**](/windows/win32/api/winstring/nf-winstring-windowsinspectstring2) | Consente ai debugger di visualizzare il valore di un Windows Runtime [**HString**](hstring.md) in un altro spazio di indirizzi, in modalità remota o da un dump.  |
| [**WindowsIsStringEmpty**](/windows/win32/api/winstring/nf-winstring-windowsisstringempty) | Indica se la stringa specificata è una stringa vuota. |
| [**WindowsPreallocateStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspreallocatestringbuffer) | Alloca un buffer di caratteri modificabile per l'utilizzo nella creazione [**HString**](hstring.md) . |
| [**WindowsPromoteStringBuffer**](/windows/win32/api/winstring/nf-winstring-windowspromotestringbuffer) | Crea un [**HString**](hstring.md) dal [**\_ buffer HString**](hstring-buffer.md)specificato. |
| [**WindowsReplaceString**](/windows/win32/api/winstring/nf-winstring-windowsreplacestring) | Sostituisce tutte le occorrenze di un set di caratteri nella stringa specificata con un altro set di caratteri per creare una nuova stringa. |
| [**WindowsStringHasEmbeddedNull**](/windows/win32/api/winstring/nf-winstring-windowsstringhasembeddednull) | Indica se la stringa specificata contiene caratteri null incorporati. |
| [**WindowsSubstring**](/windows/win32/api/winstring/nf-winstring-windowssubstring) | Recupera una sottostringa dalla stringa specificata. La sottostringa inizia in corrispondenza della posizione del carattere specificata. |
| [**WindowsSubstringWithSpecifiedLength**](/windows/win32/api/winstring/nf-winstring-windowssubstringwithspecifiedlength) | Recupera una sottostringa dalla stringa specificata. La sottostringa inizia in corrispondenza della posizione del carattere specificata e ha la lunghezza specificata. |
| [**WindowsTrimStringEnd**](/windows/win32/api/winstring/nf-winstring-windowstrimstringend) | Rimuove tutte le occorrenze finali di un set di caratteri specificato dalla stringa di origine. |
| [**WindowsTrimStringStart**](/windows/win32/api/winstring/nf-winstring-windowstrimstringstart) | Rimuove tutte le occorrenze iniziali di un set di caratteri specificato dalla stringa di origine. |



 

 

 
