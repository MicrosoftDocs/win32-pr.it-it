---
description: Gestire la condivisione di assembly e il controllo delle versioni delle DLL nell'archivio di assembly side-by-side dai programmi. Scrivere manifesti di assembly e applicazioni autodescrittori per la condivisione di assembly e il reindirizzamento delle DLL.
ms.assetid: 2f841eb6-9a6c-4c9b-b057-a3da6cd6b0b0
title: Applicazioni isolate e assembly affiancati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9af477178aa3fd68563ee53017d80c00e103b4cb97a6fd16062d307375b29574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127491"
---
# <a name="isolated-applications-and-side-by-side-assemblies"></a>Applicazioni isolate e assembly affiancati

## <a name="purpose"></a>Scopo

Applicazioni isolate e assembly side-by-side è una soluzione Microsoft Windows che riduce i conflitti di controllo delle versioni nelle applicazioni Windows client. Con Windows, gli sviluppatori di applicazioni possono compilare applicazioni isolate completamente autodescrittorie e non interessate dalle modifiche apportate al Registro di sistema, ad altre applicazioni o ad altre versioni di assembly in esecuzione nel sistema. Gli autori e gli amministratori delle applicazioni possono usare i manifesti per gestire la condivisione di assembly side-by-side dopo la distribuzione su base globale o per applicazione. I clienti traggono vantaggio da applicazioni isolate più stabili e aggiornate in modo più affidabile.

## <a name="where-applicable"></a>Se applicabile

Le applicazioni isolate e la condivisione di assembly side-by-side possono essere usate per sviluppare applicazioni che condividono in modo sicuro gli assembly del sistema operativo. Gli sviluppatori possono usare questa tecnologia per correggere i conflitti di controllo delle versioni delle DLL causati da una versione incompatibile di un assembly condiviso.

Se l'applicazione deve ottenere in modo coerente la versione di un componente testato, è possibile isolarla in modo che sia sempre eseguita con la versione testata del componente nel computer dell'utente.

Le applicazioni isolate e gli assembly side-by-side sono destinati allo sviluppo di applicazioni in stile desktop.

## <a name="developer-audience"></a>Sviluppatori

Questa documentazione è destinata principalmente agli sviluppatori di software, agli sviluppatori di applicazioni e agli amministratori di rete:

-   Sviluppatori di software che vogliono creare applicazioni isolate che useranno gli assembly side-by-side resi disponibili da Microsoft e da altri editori di assembly side-by-side.
-   Sviluppatori di applicazioni interessati a creare assembly side-by-side per isolare le applicazioni.
-   Amministratori di rete che vogliono altre informazioni sulle applicazioni isolate.

Come riferimento principale per la condivisione di assembly side-by-side e le applicazioni isolate, questa documentazione fornisce informazioni generali sulla creazione di manifesti e assembly side-by-side, sull'installazione di applicazioni isolate e assembly side-by-side e sull'uso dell'API del contesto di attivazione.

## <a name="run-time-requirements"></a>Requisiti di runtime

Windows Server 2003 e versioni successive o Windows XP e versioni successive è necessario per usare assembly e manifesti side-by-side per isolare le applicazioni e usare l'API del contesto di attivazione.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                         | Descrizione                                                                    |
|---------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Riferimento](side-by-side-assemblies-reference.md)<br/> | Documentazione di applicazioni isolate e assembly side-by-side.<br/> |



 

 

 




