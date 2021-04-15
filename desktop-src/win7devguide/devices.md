---
title: Dispositivi (Guida per sviluppatori di Windows 7)
description: I dispositivi rappresentano una parte fondamentale dell'esperienza del computer e Windows 7 offre nuove possibilità per gli sviluppatori di applicazioni che interagiscono con i dispositivi.
ms.assetid: faed8ec8-2f12-4090-a003-b14b3d26e02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cbfa699d129fd6d8343a0645fc6ed22aa9618ee
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104400163"
---
# <a name="devices-windows-7-developer-guide"></a>Dispositivi (Guida per sviluppatori di Windows 7)

I dispositivi rappresentano una parte fondamentale dell'esperienza del computer e Windows 7 offre nuove possibilità per gli sviluppatori di applicazioni che interagiscono con i dispositivi. La piattaforma di esperienza del dispositivo consente l'associazione di applicazioni e servizi con un particolare dispositivo, in modo che gli utenti possano ottenere il massimo vantaggio dalle periferiche immediatamente alla connessione. La piattaforma sensore fornisce un set di API per l'individuazione e la comunicazione con i dispositivi sensori che consentono una nuova generazione di applicazioni che sono consapevoli dei propri ambienti. La piattaforma location fornisce nuove API per l'uso dei dati della località da un ricevitore GPS (Global Positioning Systems) o altri servizi che abilitano il comportamento delle applicazioni specifiche per la posizione per gli utenti mobili. (Vedere [nozioni fondamentali sui dispositivi-Panoramica](https://www.microsoft.com/whdc/device/default.mspx)).

## <a name="device-experience-platform"></a>Piattaforma esperienza dispositivo

Windows 7 combina software e servizi per creare nuove esperienze entusiasmanti per telefoni cellulari, lettori multimediali portatili, fotocamere e stampanti. Windows 7 rende più semplice l'utilizzo di questi dispositivi direttamente dal desktop di Windows. Fornisce inoltre ai produttori di dispositivi una posizione preminente sul desktop di Windows, con opportunità di personalizzazione e una semplice interfaccia per presentare le funzionalità e i servizi supportati dal dispositivo.

Grazie alla piattaforma esperienza dispositivo, ogni sessione di Windows diventa un portale che consente ai clienti di ottenere più valore dai loro dispositivi. La piattaforma esperienza dispositivo consente agli utenti di connettersi al produttore del dispositivo, individuare e usare i servizi correlati e ottenere informazioni sugli accessori. Poiché l'esperienza del dispositivo è connessa ai servizi Web Microsoft, le società di dispositivi possono aggiornare l'esperienza anche dopo che i dispositivi sono stati spediti ai consumer. La piattaforma di esperienza del dispositivo può generare un'esperienza simile a un'applicazione per i dispositivi Windows con *logo* , ad esempio i telefoni cellulari.

La piattaforma di esperienza del dispositivo consente alle applicazioni di accedere ai dispositivi, ad esempio telefoni cellulari e lettori multimediali, che implementano i servizi tramite il *protocollo MTP (Media Transfer Protocol)* o il modello di driver dei [dispositivi portatili Windows](https://www.bing.com/search?q=Windows+Portable+Devices) .

Per abilitare la sincronizzazione delle informazioni personali tra un PC e un dispositivo, la piattaforma esperienza dispositivo ospita una nuova piattaforma di sincronizzazione per i dispositivi connessi e fornisce un'interfaccia utente per la selezione di applicazioni di destinazione per la sincronizzazione dei dati, ad esempio **contatti**, **Calendario** e **attività**. (Vedere [Windows Device Experience](https://www.microsoft.com/whdc/device/DeviceExperience/default.mspx)).

## <a name="windows-biometric-framework"></a>Windows Biometric Framework

Il Windows Biometric Framework (WBF) fornisce un'API che consente alle applicazioni di usare i dispositivi di impronta digitale per registrare, identificare e verificare le identità utente senza accedere direttamente ad alcun esempio o hardware di impronta digitale biometrica. È possibile usare WBF con i dispositivi di impronta digitale con driver WBDI (Biometric Device Interface) di Windows. WBF è estendibile tramite adattatori plug-in che gestiscono le comunicazioni dei sensori, le corrispondenze biometriche e l'archiviazione del modello. In questo modo si garantisce che WBF possa essere usato con un'ampia gamma di sensori di impronta digitale. In Windows 7, i lettori di impronta digitale possono usare WBF per l'autenticazione durante l' *UAC* e l'accesso a Windows. (Vedere [Windows Biometric Framework API](../secbiomet/biometric-service-api-portal.md)).

 

 
