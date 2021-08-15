---
title: Dispositivi (Windows 7 Developer Guide)
description: I dispositivi sono una parte fondamentale dell'esperienza pc e Windows 7 offre nuove possibilità agli sviluppatori di applicazioni che interagiscono con i dispositivi.
ms.assetid: faed8ec8-2f12-4090-a003-b14b3d26e02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775389f1a3548e2e94b8b2c25f9b46560cef5fc61a5e486f5dff28871da9f9e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086734"
---
# <a name="devices-windows-7-developer-guide"></a>Dispositivi (Windows 7 Developer Guide)

I dispositivi sono una parte fondamentale dell'esperienza pc e Windows 7 offre nuove possibilità agli sviluppatori di applicazioni che interagiscono con i dispositivi. Device Experience Platform consente l'associazione di applicazioni e servizi a un dispositivo specifico, in modo che gli utenti possano ottenere il massimo vantaggio dalle periferiche immediatamente dopo la connessione. Sensor Platform offre un set di API per l'individuazione e la comunicazione con i dispositivi dei sensori che consentiranno una nuova generazione di applicazioni in grado di riconoscere i propri ambienti. La piattaforma di posizione offre nuove API per l'uso dei dati di posizione di un ricevitore GPS (Global Positioning Systems) o di altri servizi che abilitano il comportamento dell'applicazione specifico della posizione per gli utenti mobili. Vedere [Nozioni fondamentali sui dispositivi - Panoramica.](https://www.microsoft.com/whdc/device/default.mspx)

## <a name="device-experience-platform"></a>Piattaforma per l'esperienza del dispositivo

Windows 7 combina software e servizi per creare nuove esperienze interessanti per telefoni cellulari, lettori multimediali portatili, fotocamere e stampanti. Windows 7 semplifica l'uso di questi dispositivi direttamente dal Windows desktop. Fornisce inoltre ai creatori di dispositivi un posizionamento importante sul desktop Windows, con opportunità di personalizzazione e una semplice interfaccia per presentare le funzionalità e i servizi supportati dal dispositivo.

Tramite Device Experience Platform, ogni sessione Windows diventa un portale per i clienti per ottenere più valore dai propri dispositivi. Device Experience Platform consente agli utenti di connettersi al produttore del dispositivo, individuare e usare i servizi correlati e ottenere informazioni sugli accessori. Poiché l'esperienza del dispositivo è connessa ai servizi Web di Microsoft, le aziende di dispositivi possono aggiornarne l'esperienza anche dopo che i dispositivi sono stati spediti agli utenti. Device Experience Platform può generare un'esperienza simile a *un'applicazione* Windows i dispositivi del logo, ad esempio un telefono cellulare.

Device Experience Platform consente alle applicazioni di accedere a dispositivi come telefoni cellulari e lettori multimediali che implementano servizi tramite il protocollo *MTP (Media Transfer Protocol)* o il modello di driver [Windows Portable Devices.](https://www.bing.com/search?q=Windows+Portable+Devices)

Per abilitare la sincronizzazione delle informazioni personali tra un PC e un dispositivo, Device Experience Platform ospita una nuova piattaforma di sincronizzazione per i dispositivi connessi e fornisce un'interfaccia utente per la selezione delle applicazioni di destinazione per la sincronizzazione dei dati, ad esempio Contatti **,** **Calendario** e **Attività**. Vedere [l Windows asserzione del dispositivo.](https://www.microsoft.com/whdc/device/DeviceExperience/default.mspx)

## <a name="windows-biometric-framework"></a>Windows Biometric Framework

Windows Biometric Framework (WBF) fornisce un'API che consente alle applicazioni di usare dispositivi di impronta digitale per registrare, identificare e verificare le identità degli utenti senza ottenere l'accesso diretto a hardware o campioni di impronte digitali biometriche. È possibile usare WBF con dispositivi con impronta digitale Windows driver WBDI (Biometric Device Interface). WBF è estendibile tramite adattatori plug-in che gestiscono le comunicazioni dei sensori, la corrispondenza biometrica e l'archiviazione dei modelli. Ciò garantisce che WBF possa essere usato con un'ampia gamma di sensori di impronta digitale. In Windows 7, i lettori di impronte digitali  possono usare WBF per l'autenticazione durante il controllo dell'account utente Windows accesso. (Vedere [Windows'API Biometric Framework.](../secbiomet/biometric-service-api-portal.md)

 

 
