---
title: Registrazione client del canale virtuale
description: È necessario archiviare il nome della DLL client nel registro di sistema.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727895"
---
# <a name="virtual-channel-client-registration"></a>Registrazione client del canale virtuale

È necessario archiviare il nome della DLL client nel registro di sistema.

Nel registro di sistema aggiungere una sottochiave a una delle seguenti posizioni:

**HKEY \_ Software \_ utente corrente** \\  \\ **Microsoft** \\ **Terminal Server** \\  \\ **componenti aggiuntivi** predefiniti client

**HKEY \_ Software \_ utente corrente** \\ **software** \\ **Microsoft** \\ **Terminal Server** \\  \\ **componenti aggiuntivi** connessione client

> [!Note]  
> Nel percorso del registro di sistema, *Connection* rappresenta il nome di una connessione nella gestione connessione.

 

Le voci sotto il tasto **\\ \\ componenti aggiuntivi predefiniti** si applicano a tutte le connessioni. Le voci nella chiave dei **\\  \\ componenti aggiuntivi della connessione** si applicano solo alla connessione identificata dalla *connessione*. È possibile creare e gestire le connessioni mediante gestione connessione.

Alla sottochiave può essere assegnato qualsiasi nome. Deve contenere un valore **reg \_ SZ** o **reg \_ expand \_ SZ** e può includere facoltativamente un valore **reg \_ DWORD** . La sintassi del valore **reg \_ SZ** o **reg \_ expand \_ SZ** è la seguente.

``` syntax
Name = DLLname
```

Se **Name** è un valore **reg \_ expand \_ SZ** , può contenere variabili di ambiente non espanse che vengono espanse in fase di esecuzione.

Il valore di *dllname* può essere un percorso completo. Se *dllname* non contiene un percorso, viene utilizzata la strategia di ricerca dll standard. Per ulteriori informazioni, vedere la sezione Osservazioni per [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).

 

 