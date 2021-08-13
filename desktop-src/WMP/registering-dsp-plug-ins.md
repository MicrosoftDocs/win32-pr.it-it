---
title: Registrazione dei plug-in DSP
description: Registrazione dei plug-in DSP
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Windows Media Player plug-in, voci del Registro di sistema
- plug-in, voci del Registro di sistema
- plug-in di elaborazione del segnale digitale, voci del Registro di sistema
- plug-in DSP, voci del Registro di sistema
- registro, plug-in DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7671c59dfe64094afbc5f0537bcae237b3812699f4db1a06519054b14ef295f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570381"
---
# <a name="registering-dsp-plug-ins"></a>Registrazione dei plug-in DSP

Per rendere disponibile il plug-in DSP in Windows Media Player è necessario creare le seguenti sottochiavi e voci del Registro di sistema nel computer dell'utente.


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



Nella sintassi del Registro di sistema precedente i simboli in corsivo sono segnaposto per i nomi e gli identificatori univoci globali (GUID) specifici del plug-in DSP. Nella tabella seguente vengono descritti questi segnaposto.



| Segnaposto               | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PluginClsid*             | GUID che rappresenta l'identificatore di classe per la classe primaria del plug-in DSP. Si tratta della classe che implementa **IMediaObject**, **IPluginEnable** ed eventualmente **ISpecifyPropertyPages**. In un plug-in in modalità doppia questa classe implementa anche **IMFTransform** e **IMFGetService.** Questo GUID deve essere nel formato del Registro di sistema, con le parentesi graffe.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *PluginClassFriendlyName* | Nome descrittivo per la classe primaria del plug-in DSP. Esempio: "ProsewareDSP Class"<br/>                                                                                                                                                                                                                                                                                                                                 |
| *PluginModuleName*        | Percorso completo della DLL che implementa il plug-in DSP. Esempio: "C: \\ Programmi \\ Proseware \\ProsewareDsp.dll"<br/>                                                                                                                                                                                                                                                                                     |
| *Threading*               | Stringa che specifica il modello di threading per il plug-in. Se il plug-in verrà eseguito con Windows Media Player 11 in Windows Vista, questa voce del Registro di sistema deve essere uguale a "Entrambi". Se il plug-in verrà eseguito in Windows XP o nei sistemi operativi precedenti, questa voce del Registro di sistema può essere uguale a "Apartment" o "Both".                                                                                           |



 

Se il plug-in DSP implementa un'interfaccia personalizzata e se il plug-in verrà eseguito in Windows Media Player 11 in Windows Vista, è necessario creare le sottochiavi e le voci del Registro di sistema seguenti nel computer dell'utente.


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



Nella sintassi del Registro di sistema precedente i simboli in corsivo sono segnaposto per nomi, valori numerici e IDENTIFICATORI UNIVOCI globali (GUID) specifici del plug-in DSP. Nella tabella seguente vengono descritti questi segnaposto.



| Segnaposto           | Descrizione                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ProxyStubClsid*      | GUID che rappresenta l'identificatore di classe per la classe che implementa i proxy e gli stub per le interfacce personalizzate del plug-in DSP. Questo GUID deve essere nel formato del Registro di sistema, con le parentesi graffe.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *ProxyStubModuleName* | Percorso completo della DLL che implementa le interfacce proxy e stub per il plug-in DSP. Esempio: "C: \\ Programmi \\ Proseware \\ProsewareDspPS.dll"<br/>                                                                                               |
| *CustomInterfaceId*   | GUID che rappresenta l'identificatore di interfaccia per un'interfaccia personalizzata implementata dal plug-in DSP. Questo GUID deve essere nel formato del Registro di sistema, con le parentesi graffe.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                           |
| *CustomInterfaceName* | Nome di un'interfaccia personalizzata implementata dal plug-in DSP. Esempio: "IProsewareDsp"<br/>                                                                                                                                                                  |
| *NumberOfMethods*     | Numero di metodi, inclusi i metodi ereditati, definiti da un'interfaccia personalizzata. Esempio: "5"<br/>                                                                                                                                                                  |



 

Se il plug-in DSP fornisce una pagina delle proprietà, è necessario creare le seguenti sottochiavi e voci del Registro di sistema nel computer dell'utente.


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



Nella sintassi del Registro di sistema precedente i simboli in corsivo sono segnaposto per i nomi e gli identificatori univoci globali (GUID) specifici del plug-in DSP. Nella tabella seguente vengono descritti questi segnaposto.



| Segnaposto                 | Descrizione                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PropPageClsid*             | GUID che rappresenta l'identificatore di classe per la classe della pagina delle proprietà fornita dal plug-in DSP. Questo GUID deve essere nel formato del Registro di sistema, con le parentesi graffe.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *PropPageClassFriendlyName* | Nome descrittivo per la classe della pagina delle proprietà. Esempio: "ProsewareDSP Property Page Class"<br/>                                                                                                                                     |
| *PluginModuleName*          | Percorso completo della DLL che implementa il plug-in DSP. Esempio: "C: \\ Programmi \\ Proseware \\ProsewareDsp.dll"<br/>                                                                                               |



 

**Chiamata di IWMPPluginRegistrar**

Oltre alle sottochiavi e alle voci del Registro di sistema descritte negli elenchi e nelle tabelle precedenti, è necessario creare alcune chiavi e voci del Registro di sistema chiamando [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin). Questo metodo esegue la registrazione necessaria per consentire Windows Media Player riconoscere il plug-in e presentarlo come opzione all'utente.

Chiamare **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** nella funzione **DllRegisterServer** del plug-in e [chiamare IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) nella funzione **DllUnregisterServer del** plug-in. Per ottenere un puntatore a **un'interfaccia IWMPMediaPluginRegistrar,** chiamare **CoCreateInstance** passando il CLSID \_ WMPMediaPluginRegistrar come ID classe. La costante CLSID \_ WMPMediaPluginRegistrar è definita in wmpservices.h.

**Registrazione nella Procedura guidata plug-in DSP**

La procedura guidata del plug-in DSP, inclusa in Windows SDK, genera codice di esempio basato su Active Template Library (ATL). La funzione **DllRegisterServer** del plug-in di esempio chiama la funzione **RegisterServer** di ATL, che crea le sottochiavi e le voci del Registro di sistema in base a due file script del Registro di sistema nel Visual Studio progetto. Il file *ProjectName*.rgs contiene lo script per la registrazione della classe principale del plug-in e il file *ProjectName* PropPage.rgs contiene lo script per la registrazione della classe della pagina delle proprietà del plug-in. La funzione **DllRegisterServer** del plug-in di esempio chiama anche **IWMPPluginRegistrar::WMPRegisterPlayerPlugin**.

La procedura guidata del plug-in DSP genera anche il codice per un componente proxy-stub che è un file di .dll autoregistrazione. Il codice di registrazione per il file si trova in dlldata.cpp. La macro **DLLDATA \_ ROUTINES si espande** per includere un'implementazione di **DllRegisterServer.**

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Panoramica per gli sviluppatori di plug-in DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**IWMPMediaPluginRegistrar**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





