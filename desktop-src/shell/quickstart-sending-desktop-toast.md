---
description: Questa Guida introduttiva illustra come generare una notifica di tipo avviso popup da un'applicazione desktop.
title: Invio di una notifica di tipo avviso popup dal desktop
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 1D20ED75-E24A-4e60-91AB-CFCBE902A68E
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbSyntax
ms.openlocfilehash: 36f9da25c20d99da74be30046fc5f9f4789dfd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882793"
---
# <a name="quickstart-sending-a-toast-notification-from-the-desktop"></a>Guida introduttiva: invio di una notifica di tipo avviso popup dal desktop

Questa Guida introduttiva illustra come generare una notifica di tipo avviso popup da un'applicazione desktop.

## <a name="prerequisites"></a>Prerequisiti

-   Librerie
    -   C++: Runtime. Object. lib
    -   C \# : Windows. winmd
-   Un collegamento all'app, con [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md), deve essere installato nella schermata Start. Si noti, tuttavia, che non è necessario che venga aggiunto alla schermata Start. Per ulteriori informazioni, vedere [come abilitare le notifiche di tipo avviso popup sul desktop tramite un AppUserModelID](enable-desktop-toast-with-appusermodelid.md).
-   Una versione di Microsoft Visual Studio che supporta almeno Windows 8

## <a name="instructions"></a>Istruzioni

### <a name="1-create-your-toast-content"></a>1. creare il contenuto del popup

> [!Note]  
> Quando si specifica un modello di avviso popup che include un'immagine, tenere presente che le app desktop possono usare solo le immagini locali; le immagini Web non sono supportate. Inoltre, il percorso del file di immagine locale deve essere specificato come percorso assoluto (non relativo).

 


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



### <a name="2-create-and-attach-the-event-handlers"></a>2. creare e alleghi i gestori eventi

Registrare i gestori per gli eventi di tipo avviso popup: activated, unmissed e failed. Un'applicazione desktop deve almeno sottoscrivere l'evento attivato, in modo che possa gestire l'attivazione prevista dell'app dal popup quando viene selezionata dall'utente.


```csharp
toast.Activated += ToastActivated;
toast.Dismissed += ToastDismissed;
toast.Failed += ToastFailed;
```



### <a name="3-send-the-toast"></a>3. inviare il popup

> [!IMPORTANT]
> È necessario includere il [AppUserModelID](../properties/props-system-appusermodel-id.md) del collegamento dell'app nella schermata Start ogni volta che si chiama [**CreateToastNotifier**](/uwp/api/Windows.UI.Notifications.ToastNotificationManager?view=winrt-19041). Se non si riesce a eseguire questa operazione, il popup non verrà visualizzato.

 


```csharp
ToastNotificationManager.CreateToastNotifier(appID).Show(toast);
```



### <a name="4-handle-the-callbacks"></a>4. gestire i callback

Portare la finestra dell'app in primo piano se riceve un callback "attivato" dalla notifica di tipo avviso popup. Quando un utente seleziona un avviso popup, si prevede che l'app verrà avviata a una visualizzazione relativa al contenuto del popup.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Esempio di invio notifiche di tipo avviso popup da app desktop](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/DesktopToasts)
</dt> <dt>

[Come abilitare le notifiche di tipo avviso popup sul desktop tramite un AppUserModelID](enable-desktop-toast-with-appusermodelid.md)
</dt> <dt>

[XML Schema popup](/uwp/schemas/tiles/toastschema/schema-root)
</dt> <dt>

[Panoramica delle notifiche di tipo avviso popup](/previous-versions/windows/apps/hh779727(v=win.10))
</dt> <dt>

[Guida introduttiva: invio di una notifica di tipo avviso popup](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Guida introduttiva: invio di notifiche push di tipo avviso popup](/previous-versions/windows/hh761487(v=win.10))
</dt> <dt>

[Linee guida ed elenco di controllo per notifiche di tipo avviso popup](/windows/uwp/design/shell/tiles-and-notifications/)
</dt> <dt>

[Come scegliere e usare un modello di avviso popup](/previous-versions/windows/apps/hh465448(v=win.10))
</dt> <dt>

[Come gestire l'attivazione da una notifica di tipo avviso popup](/previous-versions/windows/apps/hh761468(v=win.10))
</dt> <dt>

[Come acconsentire esplicitamente per le notifiche di tipo avviso popup](/previous-versions/windows/apps/hh781238(v=win.10))
</dt> <dt>

[Scelta di un modello di avviso popup](/previous-versions/windows/apps/hh761494(v=win.10))
</dt> <dt>

[Opzioni audio popup](/previous-versions/windows/apps/hh761492(v=win.10))
</dt> </dl>

 

 
