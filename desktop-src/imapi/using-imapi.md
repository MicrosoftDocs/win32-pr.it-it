---
title: Uso di IMAPI
description: Gli argomenti seguenti illustrano l'uso dell'API di mastering delle immagini.
ms.assetid: c42043db-612f-488f-a6ae-a8caea8ac42b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7bf19d619f6ed5ab9a2d6b0deb1ca6a42b71a0b0941a96f54cccfa87c14b5f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092431"
---
# <a name="using-imapi"></a>Uso di IMAPI

Gli argomenti seguenti illustrano l'uso dell'API di mastering delle immagini.

## <a name="usage-scenarios"></a>Scenari di utilizzo

La documentazione seguente fornisce indicazioni dettagliate per scenari IMAPI comuni.



| Scenario                                                                                                         | Descrizione                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Controllo del supporto unità](checking-drive-support.md)                                                             | Illustra il rilevamento del supporto per un'unità multimediale.<br/>                                                                                                   |
| [Controllo del supporto multimediale](checking-media-support.md)                                                             | Illustra il rilevamento del supporto per i supporti.<br/>                                                                                                           |
| [Ingoiazione di un'immagine disco](burning-a-disc.md)                                                                       | Illustra il mastering (sgomento di un disco) con IMAPI.<br/>                                                                                                       |
| [Aggiunta di un'immagine d'avvio](adding-a-boot-image.md)                                                                   | Si basa sull'esempio [Disampliare](burning-a-disc.md) un'immagine disco aggiungendo il codice per includere un'immagine di avvio nella sezione di avvio del disco.<br/>               |
| [Creazione di un disco multisessione](creating-a-multisession-disc.md)                                                 | Illustra la creazione di un disco multisessione tramite IMAPI.<br/>                                                                                              |
| [Monitoraggio dello stato di avanzamento con gli eventi](monitoring-progress-with-events.md)                                           | Illustra l'uso di interfacce specifiche per consentire l'implementazione di un gestore eventi in modo che le informazioni sullo stato di avanzamento possano essere ricevute. <br/>        |
| [Prevenzione della disconnessione o della sospensione durante un masterizzazione](preventing-logoff-or-suspend-during-a-burn.md)                     | Contiene informazioni dettagliate sulle considerazioni sullo sviluppo di applicazioni da tenere in relazione agli scenari che coinvolgono l'utente "Disconnessione" e "Sospendi" in Windows.<br/> |
| [Fornire le autorizzazioni utente per i dispositivi di media che esegnano contenuti multimediali](providing-user-permissions-for-media-burning-devices.md) | Informazioni dettagliate sul processo necessario per assicurarsi che un utente abbia le autorizzazioni appropriate per usare i dispositivi di supporto in Windows XP e Windows Server 2003.<br/>             |



 

## <a name="application-compatibility"></a>Compatibilità delle applicazioni

La documentazione seguente contiene informazioni importanti da tenere in considerazione durante lo sviluppo di un'applicazione che utilizza IMAPI.



| Informazioni aggiuntive                                                   | Descrizione                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Layout multisessione IMAPI](imapi-multisession-layout.md) | Dettagli sul layout del disco utilizzato da IMAPI per implementare più sessioni. Queste informazioni vengono usate per garantire l'interoperabilità tra IMAPI e altri software dannosi, nonché per consentire la creazione di immagini disco multisessione compatibili con IMAPI.<br/> |



 

 

 





