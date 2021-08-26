---
title: Linee guida per più utenti
description: Linee guida per lo sviluppo di applicazioni per più utenti in Servizi Desktop remoto ambiente.
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc598042530ab59c0c8932522185ce5a9d0d3dce04cabce44239c3c81b79d59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988851"
---
# <a name="multiple-user-guidelines"></a>Linee guida per più utenti

Le sezioni seguenti forniscono linee guida per lo sviluppo di applicazioni per più utenti in un Servizi Desktop remoto specifico.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Configurazione dell'applicazione](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

L'installazione di un'applicazione per un singolo utente può creare problemi in un ambiente Servizi Desktop remoto multiutente.

</dd> <dt>

[Archiviazione di informazioni specifiche dell'utente](storing-user-specific-information.md)
</dt> <dd>

Le applicazioni devono archiviare le informazioni specifiche dell'utente in percorsi specifici dell'utente, separatamente da informazioni globali che si applicano a tutti gli utenti.

</dd> <dt>

[Spazi dei nomi degli oggetti kernel](kernel-object-namespaces.md)
</dt> <dd>

Servizi Desktop remoto usa più spazi dei nomi per gli oggetti kernel. Uno spazio dei nomi globale viene usato principalmente dai servizi nelle applicazioni client/server.

</dd> <dt>

[Indirizzi IP e nomi di computer](ip-addresses-and-computer-names.md)
</dt> <dd>

Non è opportuno presupporre che il nome del computer o l' indirizzo IP assegnato al computer sia associato a un singolo utente poiché più utenti possono accedere contemporaneamente a un server Host sessione Desktop remoto.

</dd> </dl>

Come sempre, bloccare file e database apportando modifiche per evitare la perdita accidentale di dati.

L'applicazione non deve bloccare i file dell'applicazione di run-time che non sono file per utente. I file di run-time bloccati possono evitare l'esecuzione di più istanze dell'applicazione o dei processi nell'applicazione, ad esempio le procedure guidate. Un modo efficace per testare quali file sono file dell'applicazione in fase di esecuzione è tenere traccia dei file installati dal programma di installazione dell'applicazione. I file per utente vengono installati raramente dal programma di installazione. Pertanto, la maggior parte dei file installati dal programma di installazione sono file dell'applicazione di run-time.

 

 




