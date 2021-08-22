---
description: I tratti del provider sono un metodo per collegare più dati alla registrazione di un singolo provider.
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: Tratti del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2131ee4900fca40b26e8675b3eb4aade4e740fd49d1ed06098a21682ed55ff25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069891"
---
# <a name="provider-traits"></a>Tratti del provider

I tratti del provider sono un metodo per collegare più dati alla registrazione di un singolo provider. Possono essere usati per provider basati su manifesto o TraceLogging. Questo include attualmente il supporto per l'aggiunta di un nome provider e/o di un gruppo di provider a una registrazione di un singolo provider. È probabile che in futuro verranno aggiunti più tipi di tratti. Queste informazioni vengono archiviate nel kernel come BLOB binario di un formato impostato.

I tratti possono essere impostati una sola volta per una registrazione. Eventuali altri tentativi di impostare i tratti in tale registrazione avranno esito negativo.

Per impostare i tratti del provider in un provider basato su manifesto, chiamare la [**funzione EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) con la classe di informazioni EventProviderSetTraits. Il buffer EventInformation deve contenere un BLOB binario nel formato seguente:

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

I singoli tratti devono essere nel formato seguente:

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

Dal singolo tratto, ETW \_ PROVIDER TRAIT TYPE è definito \_ \_ come:

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

I provider TraceLogging impostano automaticamente i tratti del provider quando viene chiamata la funzione [**TraceLoggingRegister.**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) Il nome del provider TraceLogging verrà sempre incluso nei tratti. È possibile impostare un gruppo in un provider TraceLogging usando la macro [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) nella definizione del provider.

## <a name="custom-traits"></a>Tratti personalizzati

Anche se la maggior parte dei 255 tipi di tratti possibili non è ancora definita, i tipi di tratto da 1 a 127 sono riservati per la definizione da parte di Microsoft. I restanti valori di tipo indicizzato più elevati possono essere usati dagli sviluppatori esterni secondo le esigenze. Chiunque consideri l'aggiunta di tratti personalizzati al provider deve provare a mantenere le dimensioni totali dei tratti sotto i 256 byte per i motivi seguenti:

-   I tratti sono inclusi in ogni evento scritto per il provider. Tratti di grandi dimensioni possono causare file di log di dimensioni molto grandi.
-   I tratti vengono archiviati nel pool di kernel non di paging per la durata del provider.

## <a name="provider-groups"></a>Gruppi di provider

Un gruppo di provider è un'entità controllabile definita da GUID in modo molto simile a un provider stesso. La differenza principale è che mentre un GUID del provider viene usato per controllare solo le registrazioni del provider, un gruppo controlla tutte le registrazioni dei membri. Ad esempio, se si abilita un gruppo di provider con una parola chiave e un livello specifici, verranno abilitate tutte le registrazioni dei membri dei gruppi con tale parola chiave e livello.

L'appartenenza al gruppo può essere limitata dalle autorizzazioni. Se il chiamante di [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) non ha le autorizzazioni per partecipare al gruppo specificato, l'appartenenza verrà negata.

In alcuni casi il controller della sessione di traccia potrebbe voler escludere alcuni provider dall'abilitazione di un gruppo. Questa operazione può essere eseguita impostando un elenco di elementi non consentiti. Un elenco di elementi non consentiti è un elenco di GUID del provider che non verranno abilitati in base alle impostazioni di gruppo per una singola sessione di registrazione. Gli elenchi non consentiti possono essere modificati dinamicamente con [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) e la classe di informazioni TraceSetDisallowList.

Anche se la maggior parte delle azioni di abilitazione può essere eseguita per i gruppi di provider in modo analogo ai singoli provider, esistono alcune eccezioni. Le eccezioni sono le seguenti:

-   I gruppi di provider non possono essere controllati da sessioni di traccia private.
-   I filtri Nome evento, ID evento e Payload non sono applicabili ai gruppi di provider perché presuppongono informazioni specifiche di un singolo provider.

 

 
