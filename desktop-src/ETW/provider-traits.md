---
description: I tratti del provider sono un metodo per il fissaggio di più dati a una registrazione del singolo provider.
ms.assetid: 97755D64-BF57-4C0D-8ED4-040FC375C4AF
title: Tratti del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c67b25857070edb6419be9a2898d2667f3a179d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980394"
---
# <a name="provider-traits"></a>Tratti del provider

I tratti del provider sono un metodo per il fissaggio di più dati a una registrazione del singolo provider. Possono essere usati per provider TraceLogging o basati su manifesto. Questo include attualmente il supporto per l'aggiunta di un nome di provider e/o di un gruppo di provider a una registrazione del singolo provider. È probabile che più tipi di tratto vengano aggiunti in futuro. Queste informazioni vengono archiviate nel kernel come BLOB binario di un formato set.

I tratti possono essere impostati una sola volta per una registrazione. Eventuali ulteriori tentativi di impostare i tratti della registrazione avranno esito negativo.

Per impostare i tratti del provider in un provider basato su manifesto, chiamare la funzione [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) con la classe di informazioni EventProviderSetTraits. Il buffer EventInformation deve contenere un BLOB binario nel formato seguente:

``` syntax
{
   UINT16 TraitsSize   // Total size of the traits including this field
   CHAR[] ProviderName // Null terminated utf-8 provider name
   TRAIT[] Traits      // Zero or more individual traits
}
```

I singoli tratti devono avere il formato seguente:

``` syntax
TRAIT {
      UINT16 TraitSize // Size of this individual trait including this field
      UINT8 Type       // ETW_PROVIDER_TRAIT_TYPE
      BYTE[] Data
      }
```

Dal tratto singolo, il \_ tipo di tratto del provider ETW \_ \_ è definito come segue:

``` syntax
typedef enum {
    EtwProviderTraitTypeGroup = 1,
    EtwProviderTraitTypeMax
} ETW_PROVIDER_TRAIT_TYPE;
```

I provider TraceLogging impostano automaticamente i tratti del provider quando viene chiamata la funzione [**TraceLoggingRegister**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingregister) . Il nome del provider TraceLogging sarà sempre incluso nei relativi tratti. Un gruppo può essere impostato su un provider TraceLogging usando la macro [**TraceLoggingOptionGroup**](/windows/win32/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup) nella definizione del provider.

## <a name="custom-traits"></a>Tratti personalizzati

Sebbene la maggior parte dei 255 tipi di tratti possibili non siano ancora definiti, i tipi di tratto 1-127 sono riservati per la definizione da parte di Microsoft. I valori di tipo indicizzato più elevati rimanenti possono essere utilizzati dagli sviluppatori esterni nel modo in cui si adattano. Chiunque stia valutando di aggiungere i propri tratti personalizzati al provider deve provare a mantenerne le dimensioni totali in 256 byte per i motivi seguenti:

-   I tratti sono inclusi in ogni evento scritto per il provider. I tratti di grandi dimensioni potrebbero causare file di log di dimensioni molto elevate.
-   I tratti vengono archiviati nel pool di kernel non di paging per la durata del provider.

## <a name="provider-groups"></a>Gruppi di provider

Un gruppo di provider è un'entità controllabile definita dal GUID, molto simile a un provider stesso. La differenza principale consiste nel fatto che, mentre un GUID del provider viene utilizzato per controllare le registrazioni del solo provider, un gruppo controllerà tutte le registrazioni dei membri. Se ad esempio si Abilita un gruppo di provider con una parola chiave e un livello specificati, tutte le registrazioni dei membri dei gruppi vengono abilitate con la parola chiave e il livello specificati.

L'appartenenza al gruppo può essere limitata da autorizzazioni. Se il chiamante di [**EventSetInformation**](/windows/desktop/api/Evntprov/nf-evntprov-eventsetinformation) non dispone delle autorizzazioni per l'aggiunta al gruppo specificato, l'appartenenza verrà negata.

In alcuni casi è possibile che il controller della sessione di traccia desideri escludere alcuni provider dalla relativa abilitazione di un gruppo. Questa operazione può essere eseguita impostando un elenco non consentiti. Un elenco non consentito è un elenco di GUID del provider che non verranno abilitati in base alle impostazioni di gruppo per una singola sessione di registrazione. Gli elenchi non consentiti possono essere modificati dinamicamente con [**TraceSetInformation**](/windows/win32/api/evntrace/nf-evntrace-tracesetinformation) e la classe di informazioni TraceSetDisallowList.

Sebbene la maggior parte delle azioni di abilitazione possa essere eseguita per i gruppi di provider in modo analogo ai singoli provider, esistono alcune eccezioni. Le eccezioni sono le seguenti:

-   I gruppi di provider non possono essere controllati da sessioni di traccia private.
-   I filtri nome evento, ID evento e payload non sono applicabili ai gruppi di provider perché presuppongono informazioni specifiche di un singolo provider.

 

 
