---
description: Un filtro di acquisizione è un elemento di un'applicazione NPP che indica al driver Network Monitor (Nmnt.sys) quali frame di dati di rete mantenere e quali frame ignorare.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: Informazioni sui filtri di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7226bb7dc5bc214ab2e09504cc232e1bf591840f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311653"
---
# <a name="about-capture-filters"></a>Informazioni sui filtri di acquisizione

Un filtro di acquisizione è un elemento di un'applicazione NPP che indica al driver Network Monitor (Nmnt.sys) quali frame di dati di rete mantenere e quali frame ignorare. Il vantaggio dell'impostazione di un filtro di acquisizione è una maggiore efficienza. Non è necessario esaminare i frame acquisiti; il driver Network Monitor li esamina. Questo approccio elimina la copia dei frame, che fornisce un vantaggio per l'utilizzo della memoria.

## <a name="capture-filter-structure"></a>Acquisisci struttura filtro

I filtri di acquisizione sono costituiti da tre elementi:

-   Impostazioni ETYPE/SAP
-   Indirizzo
-   Corrispondenza criterio

Insieme, questi elementi valutano logicamente i frame da includere o escludere durante il funzionamento di un'applicazione NPP. Il filtro di acquisizione fornisce corrispondenze complesse ed esclusioni di elementi frame all'applicazione NPP.

Network Monitor implementa il filtro di acquisizione tramite una struttura di dati, [**capturefilter**](the-capturefilter-structure.md), passata a NPP e quindi passata al driver Network Monitor all'avvio dell'acquisizione.

Per ulteriori informazioni sulle operazioni di gestione dei BLOB e sulle funzionalità dei BLOB, vedere [provider di pacchetti di rete](network-packet-providers.md) e [BLOB Network Monitor](network-monitor-blobs.md).

 

 



