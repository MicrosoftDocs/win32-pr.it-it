---
description: Comandi
ms.assetid: f579745a-5327-4c8b-bfa7-fe81d9657a3b
title: Comandi (API WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a723e9eff52bf0b0b301d1fba672db5887afebef701a312786aeafb4decb733f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431114"
---
# <a name="commands-wpd-api"></a>Comandi (API WPD)

L'applicazione client e il driver comunicano tramite comandi inviati dal client (tramite l'API dispositivo portatile Windows) al driver (tramite User-Mode Driver Framework). Un comando può includere o meno un parametro e può o meno restituire un risultato. Un client può inviare un comando in modo esplicito chiamando il metodo [**IPortableDevice::SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand) o **IPortableDeviceService:SendCommand** oppure in modo implicito chiamando uno dei metodi delle interfacce client. Alcuni comandi possono essere inviati solo in modo esplicito. queste informazioni sono presenti nella documentazione del comando. Le pagine di riferimento dei comandi descrivono lo scopo di un comando, nonché i parametri che si aspetta di ricevere e i parametri che dovrebbe restituire.

Un comando è identificato da una **struttura PROPERTYKEY.** È costituito da due parti: una parte GUID (il membro *fmtid)* e una parte DWORD (il *membro pid).* La parte GUID viene usata per indicare la categoria a cui appartiene il comando (i comandi correlati appartengono alla stessa categoria e di conseguenza avranno lo stesso *fmtid*). La parte DWORD indica l'ID del comando e viene usata per distinguere i singoli comandi all'interno di una categoria di comandi (i *valori pid* per i comandi nella stessa categoria saranno diversi).

La tabella seguente elenca le categorie di comandi Windows dispositivi portatili. I produttori di dispositivi possono definire i propri comandi creando categorie di comandi e ID di comando personalizzati. Tuttavia, un produttore non deve aggiungere comandi alle categorie elencate di seguito, poiché sono riservati da Microsoft.

**Categorie di comandi**



| Categoria                         | Descrizione                                                                                                                             |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **CATEGORIA WPD \_ \_ COMUNE**                | Comandi comuni a tutti gli oggetti e i dispositivi.                                                                                    |
| **HINT PER DISPOSITIVI \_ DELLA CATEGORIA WPD \_ \_**         | Comandi usati per recuperare informazioni facoltative sul dispositivo che possono essere usate per migliorare l'esperienza dell'utente finale.                         |
| **SMS DI CATEGORIA WPD \_ \_**                   | Comandi usati per i dispositivi che supportano la funzionalità SMS (Short Message Service), che viene in genere esposta nei telefoni cellulari. |
| **ACQUISIZIONE DI IMMAGINI ANCORA \_ \_ NELLA \_ CATEGORIA \_ WPD** | Comandi usati per i dispositivi che supportano l'acquisizione di immagini statiche.                                                                    |
| **ARCHIVIAZIONE DI CATEGORIE WPD \_ \_**               | Comandi usati per gli oggetti funzionali di archiviazione.                                                                                  |



 

I comandi specifici definiti per ognuno di questi tipi sono disponibili nelle tabelle seguenti, organizzate in base al tipo di comando.

**Categoria COMUNE CATEGORIA WPD \_ \_**



| Comando                                                                                | Descrizione        |
|----------------------------------------------------------------------------------------|--------------------|
| [**DISPOSITIVO DI \_ REIMPOSTAZIONE COMUNE \_ DEL COMANDO \_ WPD \_**](wpd-command-common-reset-device-command.md) | Reimposta il dispositivo. |



 

**Categoria HINT \_ DISPOSITIVO CATEGORIA WPD \_ \_**



| Comando                                                                                                              | Descrizione                                                                      |
|----------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**WPD \_ COMMAND \_ DEVICE \_ HINTS \_ GET \_ CONTENT \_ LOCATION**](wpd-command-device-hints-get-content-location-command.md) | Recupera gli ID oggetto delle cartelle che possono contenere un oggetto di un tipo specificato. |



 

**Categoria DI ARCHIVIAZIONE DELLA CATEGORIA WPD \_ \_**



| Comando                                                                     | Descrizione                                                         |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**WPD \_ COMMAND \_ STORAGE \_ EJECT**](wpd-command-storage-eject-command.md)   | Espelle un supporto di archiviazione che può essere espulso in remoto dal driver. |
| [**FORMATO DI ARCHIVIAZIONE \_ DEI COMANDI WPD \_ \_**](wpd-command-storage-format-command.md) | Formatta un oggetto funzionale di archiviazione nel dispositivo.                  |



 

**Categoria \_ SMS categoria WPD \_**



| Comando                                                         | Descrizione                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| [**INVIO \_ SMS DEL \_ COMANDO WPD \_**](wpd-command-sms-send-command.md) | Avvia l'invio di un messaggio SMS da parte di un oggetto funzionale SMS. |



 

**Categoria WPD \_ \_ STILL IMAGE CAPTURE \_ \_ Category**



| Comando                                                                                                   | Descrizione                                                         |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**COMANDO WPD \_ \_ STILL IMAGE CAPTURE \_ \_ \_ INITIATE**](wpd-command-still-image-capture-initiate-command.md) | Avvia un'acquisizione di immagini ancorate da un oggetto funzionale dell'immagine ancorata. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida di riferimento alla programmazione**](programming-reference.md)
</dt> </dl>

 

 



