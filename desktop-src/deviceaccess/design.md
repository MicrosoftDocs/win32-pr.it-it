---
title: Considerazioni sulla progettazione per i dispositivi personalizzati
description: Questo argomento descrive considerazioni di progettazione che consentono di determinare se il dispositivo necessita di un driver personalizzato.
ms.assetid: 8AADE304-4841-41E2-968B-DFCB5B954FF1
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 5639cf9fd51eeadc2dfb3ba84556ce6c339b6eb699e0cfa364bdee0bb03d3867
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029093"
---
# <a name="design-considerations-for-custom-devices"></a>Considerazioni sulla progettazione per i dispositivi personalizzati

Questo argomento descrive considerazioni di progettazione che consentono di determinare se il dispositivo necessita di un driver personalizzato.

- [Determinazione del tipo di driver da implementare](#determining-the-type-of-driver-to-implement)
- [Considerazioni sulla sicurezza](#security-considerations)
- [Argomenti correlati](#related-topics)

## <a name="determining-the-type-of-driver-to-implement"></a>Determinazione del tipo di driver da implementare

Questa tabella descrive quando è necessario sviluppare un driver personalizzato per il dispositivo e comunicare con esso usando il API di accesso al dispositivo e quando usare invece gli stack di dispositivi Windows forniti da .

| Per supportare | Implementazione |
|:---|:---|
| Dispositivi noti, tra cui: <ul><li>Sensore</li><li>Località</li><li>Webcam</li><li>Prossimità</li><li>Servizio messaggi brevi (SMS)</li><li>Mobile Broadband</li></ul><br/> | Per molti tipi di dispositivi noti, non è necessario un driver personalizzato, perché Windows include API e DDI (Class-Extension Device Driver Interface) che gestiscono la comunicazione tra il driver e Windows. Sensori, posizione e Windows dispositivi WPD (Portable Device) sono alcuni esempi di classi di dispositivi con questo supporto. Se si compila un driver che usa uno di questi DDI forniti da Windows per inviare e ricevere dati e comandi, non è necessario che l'app Windows Store usi il API di accesso al dispositivo per brokerare l'accesso o inviare codici di controllo di input/output (I/O) direttamente al driver. <br/> Quando un'app Windows Store richiede l'accesso a un dispositivo noto usando l'API runtime di Windows per la relativa classe di dispositivo, Windows 8 gestirà l'accesso al dispositivo in base al tipo di dispositivo. Le app avranno sempre accesso ad alcuni tipi noti di dispositivi (ad esempio accelerometri) che non rivelano informazioni personali. Altri tipi di dispositivi noti devono essere dichiarati nel manifesto dell'applicazione prima che un'app possa accedervi. L'utente deve concedere a un'app l'autorizzazione per accedere ai dispositivi che rivelano informazioni riservate, ad esempio i dispositivi di posizione, webcam e microfono, oppure può costare denaro all'utente, ad esempio i dispositivi a banda larga mobile. <br/> |
| Dispositivo WPD che implementa i servizi MTP.<br/> | È possibile usare il driver di classe MTP oppure è possibile compilare un driver usando il DDI WPD.<br/> Windows 8 fornisce il supporto per i servizi dei dispositivi MTP. E un'app può usare il [Windows. Devices.Portable](/uwp/api/Windows.Devices.Portable) Windows Runtime, l'API Com (Portable Device Component Object Model) o WPD Automation per accedere al dispositivo. L'app non deve usare il API di accesso al dispositivo.<br/> |
| Dispositivo che non dispone di un'estensione di Windows o di un driver di classe fornito dall'utente.<br/>  | In questo caso, consultare le app per dispositivi [UWP](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) per i dispositivi interni per i dispositivi specializzati per determinare se è necessario implementare l'accesso personalizzato ai driver usando il API di accesso al dispositivo.<br/> |

## <a name="security-considerations"></a>Considerazioni relative alla sicurezza

Gli articoli seguenti forniscono indicazioni per la scrittura di codice C++ sicuro:

- [Procedure consigliate per la sicurezza per C++](/cpp/security/security-best-practices-for-cpp)
- [Patterns & Practices Security Guidance for Applications]/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Argomenti correlati

[Esempio di accesso al](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)driver personalizzato, [app per dispositivi UWP per dispositivi interni,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Hardware Dev Center](/windows-hardware/drivers/)
