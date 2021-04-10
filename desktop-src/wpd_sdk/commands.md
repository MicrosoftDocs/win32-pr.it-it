---
description: Comandi
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Comandi (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974c6b2b68949e53ae778ed56adcfcb10d2edd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226036"
---
# <a name="commands-wpd-api"></a>Comandi (API WPD)

L'applicazione client e il driver comunicano per mezzo di comandi inviati dal client (tramite l'API di Windows Portable Device) al driver (tramite il Framework del driver User-Mode). Un comando può includere o meno un parametro e non può restituire un risultato. Un client può inviare un comando in modo esplicito, chiamando il metodo [**IPortableDevice:: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) o **IPortableDeviceService: SendCommand** oppure, in modo implicito, chiamando uno dei metodi delle interfacce client. Alcuni comandi possono essere inviati solo in modo esplicito; Questi sono indicati nella documentazione del comando. Le pagine di riferimento del comando descrivono lo scopo di un comando, nonché i parametri che prevede di ricevere e i parametri che dovrebbero restituire.

Un comando è identificato da una struttura **PropertyKey** . Questa operazione è costituita da due parti: una parte GUID (membro *fmtid* ) e una parte DWORD (il membro *PID* ). La parte GUID viene utilizzata per indicare la categoria a cui appartiene il comando (i comandi correlati appartengono alla stessa categoria e pertanto avranno lo stesso *fmtid*). La parte DWORD indica l'ID di comando e viene usata per distinguere i singoli comandi all'interno di una categoria di comandi (i valori *PID* per i comandi nella stessa categoria saranno diversi).

Nella tabella seguente sono elencate le categorie di comandi definiti da dispositivi portatili Windows. I produttori di dispositivi possono definire i propri comandi creando proprie categorie di comando e ID di comando. Tuttavia, un produttore non deve aggiungere comandi alle categorie elencate di seguito, perché sono riservate da Microsoft.

**Categorie di comandi**



| Categoria                         | Descrizione                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **\_categoria WPD \_ comune**                | Comandi comuni a tutti gli oggetti e i dispositivi.                                                                                    |
| **\_hint per \_ dispositivi di categoria WPD \_**         | Comandi usati per recuperare informazioni facoltative sul dispositivo che possono essere usate per migliorare l'esperienza dell'utente finale.                         |
| **\_SMS della categoria WPD \_**                   | Comandi usati per i dispositivi che supportano la funzionalità SMS (Short Message Service), che in genere è esposta nei telefoni cellulari. |
| **\_acquisizione di \_ \_ Immagini ancora della categoria \_ WPD** | Comandi usati per i dispositivi che supportano l'acquisizione di immagini ancora.                                                                    |
| **\_archiviazione categoria \_ WPD**               | Comandi utilizzati per gli oggetti funzionali di archiviazione.                                                                                  |



 

I comandi specifici definiti per ognuno di questi tipi sono forniti nelle tabelle seguenti, organizzati per tipo di comando.

**\_ \_ Categoria comune categoria WPD**



| Comando                                                                                | Descrizione        |
|----------------------------------------------------------------------------------------|--------------------|
| [**\_dispositivo di \_ \_ reimpostazione comune comando \_ WPD**](wpd-command-common-reset-device-command.md) | Reimposta il dispositivo. |



 

**Categoria \_ di \_ hint del dispositivo categoria WPD \_**



| Comando                                                                                                              | Descrizione                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**\_suggerimenti del \_ dispositivo comando WPD ottenere il \_ \_ \_ percorso del contenuto \_**](wpd-command-device-hints-get-content-location-command.md) | Recupera gli ID oggetto delle cartelle che possono ospitare un oggetto di un tipo specificato. |



 

**\_ \_ Categoria archiviazione categoria WPD**



| Comando                                                                     | Descrizione                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**\_espulsione \_ archiviazione comando WPD \_**](wpd-command-storage-eject-command.md)   | Espelle un supporto di archiviazione che può essere espulso in remoto dal driver. |
| [**\_formato di \_ archiviazione \_ comando WPD**](wpd-command-storage-format-command.md) | Formatta un oggetto funzionale di archiviazione nel dispositivo.                  |



 

**Categoria \_ SMS categoria WPD \_**



| Comando                                                         | Descrizione                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [**\_comando WPD \_ SMS \_ Send**](wpd-command-sms-send-command.md) | Avvia l'invio di un messaggio SMS da un oggetto funzionale SMS. |



 

**Categoria \_ WPD \_ still \_ Image \_ Capture**



| Comando                                                                                                   | Descrizione                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**il \_ comando WPD ha \_ ancora \_ avviato l'acquisizione dell'immagine \_ \_**](wpd-command-still-image-capture-initiate-command.md) | Avvia un'acquisizione di immagini ancora da un oggetto funzionale dell'immagine ancora. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 



