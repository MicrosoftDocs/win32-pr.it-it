---
title: Interfaccia utente delle versioni precedenti rimosse per i volumi locali
description: Interfaccia utente delle versioni precedenti rimosse per i volumi locali
ms.assetid: 0BD3D046-EB06-4C9A-952C-306AC99396C6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25d898be8d079ee713e0fa3e508e552b3cd4009
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104474486"
---
# <a name="previous-versions-ui-removed-for-local-volumes"></a>Interfaccia utente delle versioni precedenti rimosse per i volumi locali

## <a name="platform"></a>Piattaforma

**Client** -Windows 8 


## <a name="description"></a>Descrizione

Nelle versioni precedenti di Windows gli utenti potevano ripristinare le versioni precedenti dei singoli file dalle "copie shadow" dei volumi locali. Queste copie shadow vengono create dalla funzionalità "versioni precedenti" tramite il servizio Copia Shadow del volume (VSS). In Windows 7, gli utenti possono configurare e pianificare le copie shadow in interfaccia utente di protezione del sistema disponibili tramite le proprietà del sistema.

Tuttavia, le versioni precedenti sono state usate raramente e hanno comportato un impatto negativo sulle prestazioni complessive di Windows. di conseguenza la funzionalità è stata rimossa. In Windows 8 queste funzionalità non sono più disponibili:

-   Possibilità di esplorare, cercare o ripristinare versioni precedenti dei file tramite l'interfaccia utente di versioni precedenti
-   La possibilità di configurare o pianificare versioni precedenti dei file tramite l'interfaccia utente di protezione del sistema

Tuttavia, gli utenti possono comunque utilizzare la scheda versioni precedenti quando si accede a condivisioni file in un server Windows.

## <a name="manifestation"></a>Manifestazione

L'opzione versioni precedenti non è più disponibile per i volumi locali nel menu proprietà di Esplora risorse.

## <a name="solution"></a>Soluzione

Gli sviluppatori che hanno la necessità di creare copie shadow dei volumi locali possono comunque eseguire questa operazione chiamando le API VSS nel codice personalizzato.

 

 




