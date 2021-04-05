---
title: Registrazione di plug-in DSP
description: Registrazione di plug-in DSP
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Plug-in di Windows Media Player, voci del registro di sistema
- plug-in, voci del registro di sistema
- plug-in di elaborazione dei segnali digitali, voci del registro di sistema
- Plug-in DSP, voci del registro di sistema
- Registro di sistema, plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64e7afd43cf242d57c0a9375c4cbda56e457ef1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103956195"
---
# <a name="registering-dsp-plug-ins"></a>Registrazione di plug-in DSP

Per rendere disponibile il plug-in DSP in Windows Media Player è necessario creare le sottochiavi e le voci del registro di sistema seguenti nel computer dell'utente.


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



Nella sintassi del registro di sistema precedente, i simboli in corsivo sono segnaposto per i nomi e identificatori univoci globali (GUID) specifici per il plug-in DSP. Nella tabella seguente vengono descritti i segnaposto.



| Segnaposto               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PluginClsid*             | GUID che rappresenta l'identificatore di classe per la classe primaria del plug-in DSP. Si tratta della classe che implementa **IMediaObject**, **IPluginEnable** e possibilmente **ISpecifyPropertyPages**. In un plug-in in modalità duale, questa classe implementa anche **IMFTransform** e **IMFGetService**. Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *PluginClassFriendlyName* | Nome descrittivo per la classe primaria del plug-in DSP. Esempio: "classe ProsewareDSP"<br/>                                                                                                                                                                                                                                                                                                                                 |
| *PluginModuleName*        | Percorso completo della DLL che implementa il plug-in DSP. Esempio: "C: \\ Program Files \\ Proseware \\ProsewareDsp.dll"<br/>                                                                                                                                                                                                                                                                                     |
| *Threading*               | Stringa che specifica il modello di threading per il plug-in. Se il plug-in verrà eseguito con Windows Media Player 11 in Windows Vista, questa voce del registro di sistema deve essere uguale a "both". Se il plug-in viene eseguito in Windows XP o in sistemi operativi precedenti, la voce del registro di sistema può essere uguale a "Apartment" o "both".                                                                                           |



 

Se il plug-in DSP implementa un'interfaccia personalizzata e se il plug-in viene eseguito in Windows Media Player 11 in Windows Vista, è necessario creare le sottochiavi e le voci del registro di sistema seguenti nel computer dell'utente.


```C++
[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid]
@=PSFactoryBuffer

[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid\InprocServer32]
@=ProxyStubModuleName
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId]
@=CustomInterfaceName

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\NumMethods]
@=NumberOfMethods

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\ProxyStubClsid32]
@=ProxyStubClsid
```



Nella sintassi del registro di sistema precedente, i simboli in corsivo sono segnaposto per nomi, valori numerici e identificatori univoci globali (GUID) specifici per il plug-in DSP. Nella tabella seguente vengono descritti i segnaposto.



| Segnaposto           | Descrizione                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ProxyStubClsid*      | GUID che rappresenta l'identificatore di classe per la classe che implementa i proxy e gli stub per le interfacce personalizzate del plug-in DSP. Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *ProxyStubModuleName* | Percorso completo della DLL che implementa le interfacce del proxy e dello stub per il plug-in DSP. Esempio: "C: \\ Program Files \\ Proseware \\ProsewareDspPS.dll"<br/>                                                                                               |
| *CustomInterfaceId*   | GUID che rappresenta l'identificatore di interfaccia per un'interfaccia personalizzata implementata dal plug-in DSP. Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                           |
| *CustomInterfaceName* | Nome di un'interfaccia personalizzata implementata dal plug-in DSP. Esempio: "IProsewareDsp"<br/>                                                                                                                                                                  |
| *NumberOfMethods*     | Numero di metodi, inclusi i metodi ereditati, definiti da un'interfaccia personalizzata. Esempio: "5"<br/>                                                                                                                                                                  |



 

Se il plug-in DSP fornisce una pagina delle proprietà, è necessario creare le sottochiavi e le voci del registro di sistema seguenti nel computer dell'utente.


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



Nella sintassi del registro di sistema precedente, i simboli in corsivo sono segnaposto per i nomi e identificatori univoci globali (GUID) specifici per il plug-in DSP. Nella tabella seguente vengono descritti i segnaposto.



| Segnaposto                 | Descrizione                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PropPageClsid*             | GUID che rappresenta l'identificatore di classe per la classe di pagine delle proprietà fornita dal plug-in DSP. Il GUID deve essere nel formato del registro di sistema, completo di parentesi graffe.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *PropPageClassFriendlyName* | Nome descrittivo per la classe della pagina delle proprietà. Esempio: "classe della pagina delle proprietà di ProsewareDSP"<br/>                                                                                                                                     |
| *PluginModuleName*          | Percorso completo della DLL che implementa il plug-in DSP. Esempio: "C: \\ Program Files \\ Proseware \\ProsewareDsp.dll"<br/>                                                                                               |



 

**Chiamata di IWMPPluginRegistrar**

Oltre alle sottochiavi del registro di sistema e alle voci descritte nelle tabelle e negli elenchi precedenti, è necessario creare alcune voci e chiavi del registro di sistema chiamando [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin). Questo metodo esegue la registrazione necessaria per consentire a Windows Media Player di riconoscere il plug-in e presentarlo come opzione all'utente.

Chiamare **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin** nella funzione **DllRegisterServer** del plug-in e chiamare [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) nella funzione **DllUnregisterServer** del plug-in. Per ottenere un puntatore a un'interfaccia **IWMPMediaPluginRegistrar** , chiamare **COCREATEINSTANCE**, passando CLSID \_ WMPMediaPluginRegistrar come ID classe. La costante CLSID \_ WMPMediaPluginRegistrar è definita in wmpservices. h.

**Registrazione nella procedura guidata del plug-in DSP**

La procedura guidata plug-in DSP, inclusa nella Windows SDK, genera codice di esempio basato su Active Template Library (ATL). La funzione **DllRegisterServer** del plug-in di esempio chiama la funzione **RegisterServer** di ATL, che crea le sottochiavi e le voci del registro di sistema in base a due file di script del registro di sistema nel progetto di Visual Studio. Il file *ProjectName*. RGS contiene lo script per la registrazione della classe principale del plug-in e il file *NomeProgetto* . RGS contiene lo script per la registrazione della classe della pagina delle proprietà del plug-in. La funzione **DllRegisterServer** del plug-in di esempio chiama anche **IWMPPluginRegistrar:: WMPRegisterPlayerPlugin**.

La procedura guidata plug-in DSP genera anche il codice per un componente stub proxy che è un file con estensione dll autoregistrato. Il codice di registrazione per il file si trova in dlldata. cpp. Le **\_ routine dlldata** della macro si espandono in modo da includere un'implementazione di **DllRegisterServer**.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica per gli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**IWMPMediaPluginRegistrar**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





