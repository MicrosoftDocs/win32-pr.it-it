---
title: Flag di registrazione
description: Flag di registrazione
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Windows Media Player plug-in, flag di registrazione
- plug-in, flag di registrazione
- plug-in dell'interfaccia utente, flag di registrazione
- plug-in dell'interfaccia utente, flag di registrazione
- flag, plug-in dell'interfaccia utente
- Registro di sistema, plug-in dell'interfaccia utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbd34ed98236f8a02c936d52b092b82be60b986fb7b16edce1f3b1cbb91d6a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002811"
---
# <a name="registration-flags"></a>Flag di registrazione

Quando la Windows Media Player guidata plug-in crea un nuovo progetto di plug-in dell'interfaccia utente, nel Registro di sistema viene creata una chiave che contiene informazioni sul plug-in. Questa chiave viene creata nel percorso seguente:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



*ClassId* è l'ID classe del plug-in.

Questa chiave include i valori seguenti.



| Nome                     | Tipo       | Descrizione                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funzionalità             | REG \_ DWORD | Valore DWORD costituito da almeno un flag di tipo plug-in che può essere combinato con uno o più flag di funzionalità plug-in tramite operazioni OR binarie.                             |
| Descrizione              | REG \_ SZ    | Stringa contenente la descrizione del plug-in. La procedura guidata plug-in crea una risorsa stringa e fornisce l'URL della risorsa (usando il protocollo res) per questo valore.         |
| FriendlyName             | REG \_ SZ    | Stringa che contiene il nome leggibile dall'utente per il plug-in. La procedura guidata plug-in crea una risorsa stringa e fornisce l'URL della risorsa (usando il protocollo res) per questo valore. |
| UninstallPath (facoltativo) | REG \_ SZ    | Stringa che contiene il percorso di un file eseguibile che disinstalla il plug-in.                                                                                                        |



 

Per altre informazioni sul protocollo res, vedere Internet Development SDK.

La tabella seguente contiene informazioni dettagliate sui flag del tipo di plug-in.



| Flag del tipo di plug-in                | Valore | Descrizione                                       |
|----------------------------------|-------|---------------------------------------------------|
| **SFONDO DEL \_ TIPO DI \_ PLUG-IN**     | 0x1   | Il plug-in dell'interfaccia utente non visualizza un'interfaccia utente. |
| **TIPO \_ DI \_ PLUG-IN SEPARATEWINDOW** | 0x2   | Il plug-in dell'interfaccia utente è un plug-in di finestra separato.      |
| **AREA \_ DI VISUALIZZAZIONE DEL TIPO DI \_ PLUG-IN**    | 0x3   | Il plug-in dell'interfaccia utente è un plug-in dell'area di visualizzazione.         |
| **IMPOSTAZIONI \_ DEL TIPO DI \_ PLUG-INAREA**   | 0x4   | Il plug-in dell'interfaccia utente è un plug-in dell'area impostazioni.        |
| **AREA METADATI \_ DEL \_ TIPO DI PLUG-IN**   | 0x5   | Il plug-in dell'interfaccia utente è un plug-in dell'area dei metadati.        |



 

La tabella seguente contiene informazioni dettagliate sui flag delle funzionalità del plug-in.



| Flag di funzionalità plug-in             | Valore      | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FLAG \_ DEL \_ PLUG-IN ACCEPTSMEDIA**       | 0x10000000 | Il plug-in dell'interfaccia utente può accettare matrici di puntatori a oggetti multimediali Windows Media Player [**chiama IWMPPluginUI::SetProperty.**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)                                                                                                                                                                                                                                                            |
| **I \_ FLAG DEL \_ PLUG-IN ACCETTANOPLAYLIST**   | 0x8000000  | Il plug-in dell'interfaccia utente può accettare matrici di puntatori a oggetti **Playlist** Windows Media Player [**chiama IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .                                                                                                                                                                                                                                                        |
| **FLAG \_ DEL \_ PLUG-IN HASPRESETS**         | 0x4000000  | Il plug-in dell'interfaccia utente usa i set di impostazioni. Se il plug-in specifica questo flag, Windows Media Player queryrà il plug-in per ottenere informazioni sul set di impostazioni chiamando [**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .                                                                                                                                                                                                      |
| **FLAG \_ DEL \_ PLUG-IN HASPROPERTYPAGE**    | 0x80000000 | Il plug-in dell'interfaccia utente fornisce una finestra di dialogo della pagina delle proprietà. Windows Media Player chiama [**IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) se questo flag è impostato quando viene richiamata la pagina delle proprietà.                                                                                                                                                                                                 |
| **FLAG DEL \_ \_ PLUG-IN NASCOSTI**             | 0x02000000 | Il plug-in dell'interfaccia utente in background non viene visualizzato  nel menu **Plug-in** a cui si accede dai **menu** Visualizza o Strumenti o dal pulsante Delle opzioni Seleziona riproduzione in Riproduzione in esecuzione.  Viene visualizzato nella **scheda Plug-in della** finestra di dialogo Opzioni. In questo modo l'icona In esecuzione plug-in in background viene visualizzata nella barra di stato. Questo flag non ha alcun effetto sui plug-in oltre ai plug-in dell'interfaccia utente in background.<br/> |
| **FLAG \_ DEL \_ PLUG-IN INSTALLAUTORUN**     | 0x40000000 | Windows Media Player esegue automaticamente il plug-in dell'interfaccia utente quando viene installato.                                                                                                                                                                                                                                                                                                                               |
| **FLAG \_ DEL \_ PLUG-IN LAUNCHPROPERTYPAGE** | 0x20000000 | Windows Media Player chiama [**IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) quando il plug-in dell'interfaccia utente viene eseguito per la prima volta. Se questo flag viene specificato, è necessario specificare anche **PLUGIN \_ FLAGS \_ HASPROPERTYPAGE.**<br/>                                                                                                                                                             |



 

Le costanti seguenti sono definite in wmpplug.h. Non modificare i valori associati a queste costanti.



| Nome                                    | Descrizione                               |
|-----------------------------------------|-------------------------------------------|
| **\_INSTALLREGKEY DEL PLUG-IN**               | Percorso della chiave del Registro di sistema del plug-in. |
| **PLUGIN \_ INSTALLREGKEY \_ FRIENDLYNAME** | Nome del valore del nome descrittivo.      |
| **DESCRIZIONE \_ DEL PLUG-IN INSTALLREGKEY \_**  | Nome del valore della descrizione.        |
| **FUNZIONALITÀ \_ INSTALLREGKEY DEL \_ PLUG-IN** | Nome del valore delle funzionalità.       |
| **\_PLUG-IN INSTALLREGKEY \_ UNINSTALL**    | Nome del valore del percorso di disinstallazione.     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[**Interfaccia utente di riferimento per la programmazione di plug-in**](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





