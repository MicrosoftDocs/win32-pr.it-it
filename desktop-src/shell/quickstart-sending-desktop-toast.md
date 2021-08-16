---
description: Questa guida introduttiva illustra come generare una notifica di tipo avviso popup da un'app desktop.
title: Invio di una notifica di tipo avviso popup dal desktop
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 79f8f65b18fd6774f318541b15d1649b7c25526f46bf3ab57f02edc4788687c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858655"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a>Avvio rapido: Invio di una notifica di tipo avviso popup dal desktop

Questa guida introduttiva illustra come generare una notifica di tipo avviso popup da un'app desktop.

## <a name="prerequisites"></a>Prerequisiti

-   Librerie
    -   C++: Runtime.object.lib
    -   C: \# Windows. Winmd
-   Un collegamento all'app, con [un System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), deve essere installato nel schermata Start. Si noti, tuttavia, che non è necessario che sia aggiunto al schermata Start. Per altre informazioni, vedere [How to enable desktop toast notifications through an AppUserModelID](enable-desktop-toast-with-appusermodelid.md).
-   Una versione di Microsoft Visual Studio che supporta almeno Windows 8

## <a name="instructions"></a>Istruzioni

### <a name="1-create-your-toast-content"></a>1. Creare il contenuto dell'avviso popup

> [!Note]  
> Quando si specifica un modello di avviso popup che include un'immagine, tenere presente che le app desktop possono usare solo immagini locali. Le immagini Web non sono supportate. Inoltre, il percorso del file di immagine locale deve essere specificato come percorso assoluto (non relativo).

 


```csharp
// Get a toast XML template
XmlDocument toastXml = ToastNotificationManager.GetTemplateContent(ToastTemplateType.ToastImageAndText04);

// Fill in the text elements
XmlNodeList stringElements = toastXml.GetElementsByTagName("text");
for (int i = 0; i < stringElements.Length; i++)
{
    stringElements[i].AppendChild(toastXml.CreateTextNode("Line " + i));
}

// Specify the absolute path to an image
String imagePath = "file:///" + Path.GetFullPath("toastImageAndText.png");
XmlNodeList imageElements = toastXml.GetElementsByTagName("image");

ToastNotification toast = new ToastNotification(toastXml);
```



### <a name="2-create-and-attach-the-event-handlers"></a>2. Creare e associare i gestori eventi

Registrare i gestori per gli eventi di tipo avviso popup: Attivato, Ignorato e Non riuscito. Un'app desktop deve almeno sottoscrivere l'evento Activated in modo che possa gestire l'attivazione prevista dell'app dall'avviso popup quando l'utente la seleziona.


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a>3. Inviare l'avviso popup

> [!IMPORTANT]
> È necessario includere [appUserModelID](../properties/props-system-appusermodel-id.md) del collegamento dell'app nel schermata Start ogni volta che si chiama [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041). Se non si riesce a eseguire questa operazione, l'avviso popup non verrà visualizzato.

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a>4. Gestire i callback

Portare la finestra dell'app in primo piano se riceve un callback "attivato" dalla notifica di tipo avviso popup. Quando un utente seleziona un avviso popup, l'aspettativa è che l'app verrà avviata in una visualizzazione correlata al contenuto dell'avviso popup.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di invio notifiche di tipo avviso popup da app desktop](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[Come abilitare le notifiche di tipo avviso popup sul desktop tramite un AppUserModelID](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[Schema XML di tipo avviso popup](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Panoramica delle notifiche di tipo avviso popup](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Avvio rapido: Invio di una notifica di tipo avviso popup](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Avvio rapido: Invio di una notifica push di tipo avviso popup](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Linee guida ed elenco di controllo per le notifiche di tipo avviso popup](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Come scegliere e usare un modello di avviso popup](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Come gestire l'attivazione da una notifica di tipo avviso popup](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Come acconsentire esplicitamente alle notifiche di tipo avviso popup](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Scelta di un modello di avviso popup](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Opzioni audio di tipo Avviso popup](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
