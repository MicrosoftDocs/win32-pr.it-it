---
description: Network Monitor fornisce una struttura PROPERTYINFO per definire le proprietà di un protocollo e una struttura PROPERTYINST e PROPERTYINSTEX per definire un'istanza di una proprietà.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Definizione di proprietà e strutture di istanze di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8289c16bf501d36936b1aba6f292787e1b9a41babdb1225d3c0d53885c0ba31a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119676816"
---
# <a name="property-definition-and-property-instance-structures"></a>Definizione di proprietà e strutture di istanze di proprietà

Network Monitor fornisce una [**struttura PROPERTYINFO**](propertyinfo.md) per definire le proprietà di un protocollo e una [**struttura PROPERTYINST**](propertyinst.md)e [**PROPERTYINSTEX**](propertyinstex.md) per definire un'istanza di una proprietà.

![strutture di monitoraggio di rete](images/property1.png)

Il parser alloca e inserisce la [**struttura PROPERTYINFO**](propertyinfo.md) per tutte le proprietà supportate da un protocollo. Il parser passa la struttura a Network Monitor in cui la struttura viene aggiunta al database delle [*proprietà del protocollo*](p.md). Le informazioni nella **struttura PROPERTYINFO** vengono usate durante l'analisi di un'istanza di una proprietà e durante la formattazione dei dati visualizzati nell'interfaccia utente Network Monitor dati.

Network Monitor alloca le strutture [**PROPERTYINST**](propertyinst.md) e [**PROPERTYINSTEX**](propertyinstex.md) quando il parser associa una definizione di proprietà a un'istanza di una proprietà.

La procedura seguente identifica i passaggi necessari per associare una definizione di proprietà.

**Per associare una definizione di proprietà**

1.  Identificare ogni proprietà presente in un'istanza del protocollo. Quando si collega una definizione, Network Monitor passa i dati acquisiti al parser. I dati vengono passati in base all'istanza del protocollo.
2.  Determinare il percorso della proprietà nell'istanza del protocollo.
3.  Associare una definizione di proprietà al percorso della proprietà.

Network Monitor implementa una [**struttura PROPERTYINST**](propertyinst.md) quando il parser usa i dati delle proprietà esistenti nell'acquisizione. Network Monitor implementa una [**struttura PROPERTYINSTEX**](propertyinstex.md) quando il parser deve modificare i dati delle proprietà nell'acquisizione.

 

 



