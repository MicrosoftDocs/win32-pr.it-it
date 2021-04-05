---
title: Flag di registrazione
description: Flag di registrazione
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Plug-in di Windows Media Player, flag di registrazione
- plug-in, flag di registrazione
- plug-in dell'interfaccia utente, flag di registrazione
- Plug-in dell'interfaccia utente, flag di registrazione
- flag, plug-in dell'interfaccia utente
- Registro di sistema, plug-in dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac609b45866cd5f18edf61dffc2d3b7ac3c397ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "104046319"
---
# <a name="registration-flags"></a>Flag di registrazione

Quando la procedura guidata per il plug-in di Windows Media Player crea un nuovo progetto di plug-in dell'interfaccia utente, crea una chiave nel registro di sistema che contiene informazioni sul plug-in. Questa chiave viene creata nel percorso seguente:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



*ClassID* è l'ID della classe del plug-in.

Questa chiave include i valori seguenti.



| Nome                     | Tipo       | Descrizione                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funzionalità             | REG \_ DWORD | Valore DWORD costituito da almeno un flag del tipo di plug-in che può essere combinato con uno o più flag di funzionalità plug-in tramite operazioni binarie o.                             |
| Descrizione              | REG \_ SZ    | Stringa che contiene la descrizione del plug-in. La creazione guidata plug-in crea una risorsa di stringa e fornisce l'URL della risorsa (usando il protocollo RES) per questo valore.         |
| FriendlyName             | REG \_ SZ    | Stringa che contiene il nome leggibile dall'utente per il plug-in. La creazione guidata plug-in crea una risorsa di stringa e fornisce l'URL della risorsa (usando il protocollo RES) per questo valore. |
| UninstallPath (facoltativo) | REG \_ SZ    | Stringa che contiene il percorso di un file eseguibile che disinstalla il plug-in.                                                                                                        |



 

Per ulteriori informazioni sul protocollo RES, vedere Internet Development SDK.

Nella tabella seguente vengono illustrati in dettaglio i flag dei tipi di plug-in.



| Flag tipo di plug-in                | Valore | Descrizione                                       |
|----------------------------------|-------|---------------------------------------------------|
| **\_sfondo tipo di plug-in \_**     | 0x1   | Il plug-in dell'interfaccia utente non visualizza un'interfaccia utente. |
| **tipo di plug-in \_ \_ SEPARATEWINDOW** | 0x2   | Il plug-in dell'interfaccia utente è un plug-in di finestra separato.      |
| **tipo di plug-in \_ \_ DISPLAYAREA**    | 0x3   | Il plug-in dell'interfaccia utente è un plug-in dell'area di visualizzazione.         |
| **tipo di plug-in \_ \_ SETTINGSAREA**   | 0x4   | Il plug-in dell'interfaccia utente è un plug-in area impostazioni.        |
| **tipo di plug-in \_ \_ METADATAAREA**   | 0x5   | Il plug-in dell'interfaccia utente è un plug-in dell'area dei metadati.        |



 

Nella tabella seguente vengono illustrati in dettaglio i flag delle funzionalità plug-in.



| Flag funzionalità plug-in             | Valore      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **flag plug-in \_ \_ ACCEPTSMEDIA**       | 0x10000000 | Il plug-in dell'interfaccia utente può accettare matrici di puntatore a oggetti **multimediali** quando Windows Media Player chiama [**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .                                                                                                                                                                                                                                                           |
| **flag plug-in \_ \_ ACCEPTSPLAYLISTS**   | 0x8000000  | Il plug-in dell'interfaccia utente può accettare le matrici di puntatori a oggetti della **playlist** quando Windows Media Player chiama [**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .                                                                                                                                                                                                                                                        |
| **flag plug-in \_ \_ HASPRESETS**         | 0x4000000  | Il plug-in dell'interfaccia utente usa i set di impostazioni. Se il plug-in specifica questo flag, Windows Media Player eseguirà una query sul plug-in per ottenere informazioni sul set di impostazioni chiamando [**IWMPPluginUI:: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .                                                                                                                                                                                                      |
| **flag plug-in \_ \_ HASPROPERTYPAGE**    | 0x80000000 | Il plug-in dell'interfaccia utente fornisce una finestra di dialogo della pagina delle proprietà. Windows Media Player chiamerà [**IWMPPluginUI::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) se questo flag viene impostato quando viene richiamata la pagina delle proprietà.                                                                                                                                                                                                 |
| **flag plug-in \_ \_ nascosti**             | 0x02000000 | Il plug-in in background dell'interfaccia utente non viene visualizzato nel menu **plug-** in a cui si accede dai menu **Visualizza** o **strumenti** oppure dal pulsante **Seleziona opzioni di riproduzione ora** in gioco. Viene visualizzato nella scheda **plug-** in della finestra di dialogo Opzioni. Il plug-in in background che esegue l'icona viene visualizzato nella barra di stato. Questo flag non ha alcun effetto sui plug-in diversi dai plug-in di interfaccia utente in background.<br/> |
| **flag plug-in \_ \_ INSTALLAUTORUN**     | 0x40000000 | Windows Media Player esegue automaticamente il plug-in dell'interfaccia utente quando viene installato il plug-in.                                                                                                                                                                                                                                                                                                                               |
| **flag plug-in \_ \_ LAUNCHPROPERTYPAGE** | 0x20000000 | Windows Media Player chiama [**IWMPPluginUI::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) quando il plug-in dell'interfaccia utente viene eseguito per la prima volta. Se questo flag è specificato, è necessario specificare anche i flag di plug-in **\_ \_ HASPROPERTYPAGE** .<br/>                                                                                                                                                             |



 

Le costanti seguenti sono definite in wmpplug. h. Non modificare i valori associati a queste costanti.



| Nome                                    | Descrizione                               |
|-----------------------------------------|-------------------------------------------|
| **PLUG-in \_ INSTALLREGKEY**               | Percorso della chiave del registro di sistema del plug-in. |
| **PLUG-in \_ INSTALLREGKEY \_ FriendlyName** | Nome del valore del nome descrittivo.      |
| **Descrizione del plug-in \_ INSTALLREGKEY \_**  | Nome del valore di descrizione.        |
| **funzionalità del plug-in \_ INSTALLREGKEY \_** | Nome del valore delle funzionalità.       |
| **disinstallazione del plug-in \_ INSTALLREGKEY \_**    | Nome del valore del percorso di disinstallazione.     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[**IWMPPluginUI:: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[**Guida di riferimento alla programmazione di plug-in dell'interfaccia utente**](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





