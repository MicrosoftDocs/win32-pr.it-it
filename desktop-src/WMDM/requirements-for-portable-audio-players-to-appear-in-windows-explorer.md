---
title: Requisiti per la visualizzazione dei lettori audio portatili in Esplora risorse
description: Requisiti per la visualizzazione dei lettori audio portatili in Esplora risorse
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Media Gestione dispositivi, lettori audio portatili
- Gestione dispositivi, lettori audio portatili
- Guida per programmatori, lettori audio portatili
- provider di servizi, lettori audio portatili
- creazione di provider di servizi, lettori audio portatili
- lettori audio portatili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a163bf04f4185bc1325aa12ea6acddd43191529
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298317"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a>Requisiti per la visualizzazione dei lettori audio portatili in Esplora risorse

L'estensione dello spazio dei nomi della shell portatile audio player consente agli utenti di Windows di gestire in modo coerente i dispositivi audio gestiti da Windows Media Gestione dispositivi. Se si creano i componenti del provider di servizi e del driver in base alle linee guida seguenti, il dispositivo viene visualizzato nello spazio dei nomi della shell. Gli utenti potranno interagire con il contenuto del dispositivo in modo coerente in Esplora risorse per eseguire operazioni di base, ad esempio la copia, l'eliminazione e la ridenominazione.

I requisiti della shell seguenti per i componenti del provider di servizi e dei driver hanno lo scopo di integrare le linee guida generali di Windows Media Gestione dispositivi.

Funzionalità del dispositivo

I provider di servizi Windows Media Gestione dispositivi devono essere espliciti nelle funzionalità supportate. Se una chiamata non è supportata, deve essere restituito un codice di errore. È necessario impostare i campi appropriati per la presenza o l'assenza di funzionalità al ritorno dalle funzioni seguenti:

-   [**IMDSPStorageGlobals:: GetCapabilities**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [**IMDSPStorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

I provider di servizi devono supportare le funzionalità seguenti per essere compatibili con la Shell:

-   Copia nel dispositivo (con supporto per callback di annullamento e di stato)
-   Elimina file dal dispositivo (con supporto per callback di annullamento e di stato)
-   Rinomina file nel dispositivo
-   Segnalazione spazio (spazio totale, spazio disponibile, spazio inutilizzabile)
-   Plug and Play (vedere [Abilitazione di PNP per i dispositivi](enabling-pnp-for-devices.md))
-   Formato (preferibilmente con supporto per callback di annullamento e di stato)

Se i metadati sono supportati, i campi seguenti devono essere supportati per i singoli file. Se non sono disponibili dati, il campo deve essere inizializzato come una stringa vuota:



| Campo        | Costante (definita in WMDM. idl) | Tag dei metadati    |
|--------------|--------------------------------|-----------------|
| Titolo del brano   | g \_ wszWMDMTitle                | WMDM/title      |
| Numero di traccia | g \_ wszWMDMTrack                | WMDM/Track      |
| Artista       | g \_ wszWMDMAuthor               | WMDM/autore     |
| Album        | g \_ wszWMDMAlbumTitle           | WMDM/AlbumTitle |
| Year         | g \_ wszWMDMYear                 | WMDM/anno       |
| Genre        | g \_ wszWMDMGenre                | WMDM/genre      |



 

Concorrenza

I driver in modalità kernel per Windows Media Gestione dispositivi devono essere affidabili per la gestione dell'accesso simultaneo. Ad esempio, un utente può accedere contemporaneamente al dispositivo tramite la shell e il lettore multimediale o semplicemente attraverso più finestre della shell. Come parte della gestione della concorrenza, i driver non dovrebbero presumere, solo perché il provider di servizi è caricato, che il dispositivo è in uso. Devono invece implementare un meccanismo di blocco per serializzare l'accesso al dispositivo in base alle esigenze per le singole operazioni.

Interfaccia utente

I provider di servizi per Windows Media Gestione dispositivi non devono visualizzare alcuna interfaccia utente. Eventuali errori devono essere restituiti dalle chiamate al metodo come specifici codici di errore di Windows Media Gestione dispositivi, laddove possibile.

Abilitazione nella shell

Se il pacchetto soddisfa tutti i requisiti della shell, è possibile abilitare il dispositivo in modo che venga visualizzato nella shell impostando il valore *ShowInShell* su 1 nei parametri del dispositivo. Per altre informazioni, vedere [parametri del dispositivo](device-parameters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> </dl>

 

 




