---
title: Considerazioni di progettazione per i dispositivi personalizzati
description: Questo argomento descrive le considerazioni di progettazione che consentono di determinare se il dispositivo necessita di un driver personalizzato.
ms.assetid: 8AADE304-4841-41E2-968B-DFCB5B954FF1
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: f503ae556009f3b4b9b88d9f895936218f402fc6
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734719"
---
# <a name="design-considerations-for-custom-devices"></a>Considerazioni di progettazione per i dispositivi personalizzati

Questo argomento descrive le considerazioni di progettazione che consentono di determinare se il dispositivo necessita di un driver personalizzato.

- [Determinazione del tipo di driver da implementare](#determining-the-type-of-driver-to-implement)
- [Considerazioni sulla sicurezza](#security-considerations)
- [Argomenti correlati](#related-topics)

## <a name="determining-the-type-of-driver-to-implement"></a>Determinazione del tipo di driver da implementare

Questa tabella descrive quando è necessario sviluppare un driver personalizzato per il dispositivo e comunicare con esso usando l'API di accesso ai dispositivi e quando si devono usare gli stack di dispositivi forniti da Windows.

| Per supportare | Implementazione |
|:---|:---|
| Dispositivi noti, tra cui: <ul><li>Sensore</li><li>Location</li><li>Webcam</li><li>Prossimità</li><li>SMS (Short Message Service)</li><li>Mobile Broadband</li></ul><br/> | Per molti tipi di dispositivi noti, non è necessario un driver personalizzato, perché Windows include API e interfacce del driver di dispositivo con estensione di classe (DDIs) che gestiscono la comunicazione tra il driver e le finestre. I dispositivi Sensor, location e Windows Portable Device (WPD) sono alcuni esempi di classi di dispositivi con questo supporto. Se si compila un driver che usa uno di questi DDIs forniti da Windows per inviare e ricevere dati e comandi, non è necessario che l'app di Windows Store usi l'API di accesso ai dispositivi per negoziare l'accesso o inviare i codici di controllo di input/output (I/O) direttamente al driver. <br/> Quando un'app di Windows Store richiede l'accesso a un dispositivo noto usando l'API Windows Runtime per la classe del dispositivo, Windows 8 gestirà l'accesso dei dispositivi in base al tipo di dispositivo. Le app otterranno sempre l'accesso ad alcuni tipi noti di dispositivi, ad esempio gli accelerometri, che non rivelano informazioni personali. Altri tipi di dispositivi noti devono essere dichiarati nel manifesto dell'applicazione prima che un'app possa accedervi. L'utente deve concedere l'autorizzazione a un'app per accedere ai dispositivi che visualizzano informazioni riservate, come la località, la webcam e i dispositivi Microphone, oppure possono comportare il costo dell'utente, ad esempio i dispositivi mobili a banda larga. <br/> |
| Un dispositivo WPD che implementa i servizi MTP.<br/> | È possibile usare il driver di classe MTP oppure è possibile compilare un driver usando l'interfaccia DDI WPD.<br/> Windows 8 fornisce supporto per i servizi del dispositivo MTP. Un'app può usare l'API di Windows Runtime [Windows. Devices. Portable](/uwp/api/Windows.Devices.Portable) , l'API del dispositivo portatile Component Object Model (com) o l'automazione WPD per accedere al dispositivo. L'app non deve usare l'API di accesso ai dispositivi.<br/> |
| Dispositivo che non dispone di un'estensione di classe o di un driver di classe forniti da Windows.<br/>  | In questo caso, consultare le [app per dispositivi UWP per dispositivi interni](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) per i dispositivi specializzati per determinare se è necessario implementare l'accesso personalizzato ai driver usando l'API di accesso ai dispositivi.<br/> |

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Gli articoli seguenti forniscono indicazioni per la scrittura di codice C++ sicuro:

- [Procedure di protezione ottimali per C++](/cpp/security/security-best-practices-for-cpp)
- [Modelli & procedure consigliate per la sicurezza per le applicazioni]/Previous-Versions/msp-n-p/ff650760 (v = PandP. 10))

## <a name="related-topics"></a>Argomenti correlati

[Esempio di accesso ai driver personalizzato](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [app per dispositivi UWP per dispositivi interni](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [hardware Dev Center](/windows-hardware/drivers/)
