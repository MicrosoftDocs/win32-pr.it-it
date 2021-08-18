---
description: Un filtro di acquisizione è un elemento di un'applicazione NPP che indica al driver Network Monitor (Nmnt.sys) quali frame di dati di rete mantenere e quali frame ignorare.
ms.assetid: 6ab17e18-bd97-42a8-b569-b205ac19ffd1
title: Informazioni sui filtri di acquisizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d0d1eee25915c30b8ddffc475545cbd7f7d04d0fdcecf4119480b737980cd9f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911361"
---
# <a name="about-capture-filters"></a>Informazioni sui filtri di acquisizione

Un filtro di acquisizione è un elemento di un'applicazione NPP che indica al driver Network Monitor (Nmnt.sys) quali frame di dati di rete mantenere e quali frame ignorare. Il vantaggio dell'impostazione di un filtro di acquisizione è una maggiore efficienza. Non è necessario esaminare i frame acquisiti. il Network Monitor driver li esamina. Questo approccio elimina la copia dei frame, che offre un vantaggio per l'uso della memoria.

## <a name="capture-filter-structure"></a>Acquisisci struttura filtro

I filtri di acquisizione sono costituiti da tre elementi:

-   Impostazioni Etype/SAP
-   Indirizzo
-   Corrispondenza dei criteri

Insieme, questi elementi valutano logicamente i frame da includere o escludere durante il funzionamento di un'applicazione NPP. Il filtro di acquisizione fornisce corrispondenze complesse ed esclusioni di elementi frame all'applicazione NPP.

Network Monitor il filtro di acquisizione tramite una struttura di dati, [**CAPTUREFILTER,**](the-capturefilter-structure.md)passata a NPP e quindi passata al driver Network Monitor all'avvio dell'acquisizione.

Per altre informazioni sulle operazioni NPP e sulle funzionalità BLOB, vedere [Provider](network-packet-providers.md) di pacchetti di rete [Network Monitor BLOB](network-monitor-blobs.md).

 

 



