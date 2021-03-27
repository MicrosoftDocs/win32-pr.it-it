---
description: Viene illustrato come utilizzare le API della shell \_ NotifyIcon e shell \_ NotifyIconGetRect per visualizzare un'icona di notifica.
title: Esempio NotificationIcon
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 9F31DB2D-4B12-4f65-AC91-25B4B5B1CB46
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1569d162aef358130910081bee80354cb64f690d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104979834"
---
# <a name="notificationicon-sample"></a>Esempio NotificationIcon

Viene illustrato come utilizzare le API della shell [**\_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) e [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) per visualizzare un'icona di notifica.

In questo argomento sono contenute le sezioni seguenti.

-   [Descrizione](#description)
-   [Requisiti](#requirements)
-   [Download dell'esempio](#downloading-the-sample)
-   [Compilazione dell'esempio](#building-the-sample)
-   [Esecuzione dell'esempio](#running-the-sample)

## <a name="description"></a>Descrizione

Oltre all'utilizzo della shell [**\_ NotifyIcon**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) e della [**Shell \_ NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) per visualizzare un'icona di notifica, in questo esempio viene illustrato come visualizzare una finestra del riquadro a comparsa, un menu di scelta rapida e una notifica dell'aerostato avanzati.

> [!Note]  
> [**Shell \_ di NotifyIconGetRect**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicongetrect) è disponibile solo in Windows 7 e versioni successive.

 

## <a name="requirements"></a>Requisiti



| Prodotto                                | Versione minima del prodotto |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>Download dell'esempio

| Location      | URL percorso                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [Esempio NotificationIcon](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/NotificationIcon) |

## <a name="building-the-sample"></a>Compilazione dell'esempio

Per compilare l'esempio dal prompt dei comandi:

1.  Aprire la finestra del prompt dei comandi e passare alla directory del progetto **NotificationIcon** .
2.  Immettere `msbuild NotificationIcon.sln`.

Per compilare l'esempio usando Microsoft Visual Studio (scelta consigliata):

1.  Aprire Esplora risorse e passare alla directory del progetto **NotificationIcon** .
2.  Fare doppio clic sull'icona per il file NotificationIcon. sln per aprire il progetto in Visual Studio.
3.  Scegliere **Compila soluzione** dal menu **Compila** .

## <a name="running-the-sample"></a>Esecuzione dell'esempio

1.  Passare alla directory contenente il nuovo eseguibile, utilizzando il prompt dei comandi o Esplora risorse.
2.  Nella riga di comando, immettere `NotificationIcon.exe` . In alternativa, in Esplora risorse fare doppio clic sull'icona per NotificationIcon.exe.

> [!Note]  
> Le icone di notifica specificate con un GUID sono protette dallo spoofing convalidando la registrazione di una sola applicazione. Questa registrazione viene eseguita la prima volta che si chiama la shell \_ NotifyIcon (NIM \_ Add,...) e viene archiviato il nome del percorso completo dell'applicazione chiamante. Se successivamente si sposta il file binario in un percorso diverso, il sistema non consentirà di aggiungere di nuovo l'icona. Per ulteriori informazioni, vedere la pagina relativa all' [**\_ NotifyIcon della shell**](/windows/desktop/api/Shellapi/nf-shellapi-shell_notifyicona) .

 

 

 



