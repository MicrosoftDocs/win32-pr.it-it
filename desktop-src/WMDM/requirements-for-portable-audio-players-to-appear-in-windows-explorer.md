---
title: Requisiti per la visualizzazione dei lettori audio portatili in Windows Explorer
description: Requisiti per la visualizzazione dei lettori audio portatili in Windows Explorer
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Gestione dispositivi multimediali, lettori audio portatili
- Gestione dispositivi, lettori audio portatili
- guida per programmatori, lettori audio portatili
- provider di servizi, lettori audio portatili
- creazione di provider di servizi, lettori audio portatili
- lettori audio portatili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d91e844f564ead03ddb78cf57c13c81a56bc8934bbfbde51c105b5c7e1e2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055579"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a>Requisiti per la visualizzazione dei lettori audio portatili in Windows Explorer

L'estensione dello spazio dei nomi della shell del lettore audio portabile Windows utenti con un modo coerente per gestire i dispositivi audio gestiti da Windows Gestione dispositivi multimediali. Se si crea il provider di servizi e i componenti driver in base alle linee guida seguenti, il dispositivo verrà visualizzato nello spazio dei nomi della shell. Gli utenti potranno interagire con il contenuto del dispositivo in modo coerente in Windows Explorer per eseguire operazioni di base, ad esempio copia, eliminazione e ridenominazione.

I requisiti della shell seguenti per i componenti del provider di servizi e dei driver sono destinati a integrare le linee guida generali Windows Gestione dispositivi multimediali.

Funzionalità del dispositivo

Windows I provider di servizi di Gestione dispositivi multimediali devono essere espliciti nelle funzionalità supportate. Se una chiamata non è supportata, deve essere restituito un codice di errore. I campi appropriati devono essere impostati per la presenza o l'assenza di funzionalità al ritorno dalle funzioni seguenti:

-   [**IMDSPStorageGlobals::GetCapabilities**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [**IMDSPStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

I provider di servizi devono supportare le funzionalità seguenti per essere compatibili con la shell:

-   Copia nel dispositivo (con supporto per callback di annullamento e stato)
-   Eliminare un file dal dispositivo (con supporto per i callback di annullamento e stato)
-   Rinominare il file nel dispositivo
-   Creazione di report dello spazio (spazio totale, spazio disponibile, spazio inutilizzabile)
-   Plug and Play (vedere [Abilitazione di PnP per dispositivi](enabling-pnp-for-devices.md))
-   Formato (preferibilmente con supporto per callback di annullamento e stato)

Se i metadati sono supportati, i campi seguenti devono essere supportati per i singoli file. Se non sono disponibili dati, il campo deve essere inizializzato come stringa vuota:



| Campo        | Costante (definita in WMDM.idl) | Tag di metadati    |
|--------------|--------------------------------|-----------------|
| Titolo brano   | g \_ wszWMDMTitle                | WMDM/Title      |
| Numero di traccia | g \_ wszWMDMTrack                | WMDM/Track      |
| Artista       | g \_ wszWMDMAuthor               | WMDM/Author     |
| Album        | g \_ wszWMDMAlbumTitle           | WMDM/AlbumTitle |
| Year         | g \_ wszWMDMYear                 | WMDM/Anno       |
| Genre        | g \_ wszWMDMGenre                | WMDM/Genre      |



 

Concorrenza

I driver in modalità kernel Windows Gestione dispositivi multimediali devono essere affidabili nella gestione dell'accesso simultaneo. Ad esempio, un utente può accedere contemporaneamente al dispositivo tramite la shell e il lettore multimediale o semplicemente tramite più finestre nella shell. Nell'ambito della gestione della concorrenza, i driver non devono presupporre, solo perché il provider di servizi è caricato, che il dispositivo sia in uso. Devono invece implementare un meccanismo di blocco per serializzare l'accesso al dispositivo in base alle esigenze per le singole operazioni.

Interfaccia utente

I provider di servizi Windows Gestione dispositivi multimediali non devono visualizzare alcuna interfaccia utente. Eventuali errori devono essere restituiti dalle chiamate al metodo come Windows codici di errore di Gestione dispositivi multimediali, quando possibile.

Abilitazione nella shell

Se il pacchetto soddisfa tutti i requisiti della shell, è possibile abilitare la visualizzazione del dispositivo nella shell impostando il *valore ShowInShell* su 1 nei parametri del dispositivo. Per altre informazioni, vedere [Parametri del dispositivo](device-parameters.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un provider di servizi**](creating-a-service-provider.md)
</dt> </dl>

 

 




