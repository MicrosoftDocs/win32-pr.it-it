---
description: Network Monitor fornisce una struttura PROPERTYINFO per definire le proprietà di un protocollo e una struttura PROPERTYINST e PROPERTYINSTEX per definire un'istanza di una proprietà.
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: Definizione di proprietà e strutture dell'istanza di proprietà
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55aa67efb5054d93184b56c53f84f9fac0893abf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756210"
---
# <a name="property-definition-and-property-instance-structures"></a>Definizione di proprietà e strutture dell'istanza di proprietà

Network Monitor fornisce una struttura [**PROPERTYINFO**](propertyinfo.md) per definire le proprietà di un protocollo e una struttura [**PROPERTYINST**](propertyinst.md)e [**PROPERTYINSTEX**](propertyinstex.md) per definire un'istanza di una proprietà.

![strutture di Network Monitor](images/property1.png)

Il parser alloca e compila la struttura [**PROPERTYINFO**](propertyinfo.md) per tutte le proprietà supportate da un protocollo. Il parser passa la struttura a Network Monitor dove la struttura viene aggiunta al database della [*Proprietà*](p.md)del protocollo. Le informazioni contenute nella struttura **PROPERTYINFO** vengono utilizzate durante l'analisi di un'istanza di una proprietà e durante la formattazione dei dati visualizzati nell'interfaccia utente di Network Monitor.

Network Monitor alloca le strutture [**PROPERTYINST**](propertyinst.md) e [**PROPERTYINSTEX**](propertyinstex.md) quando il parser connette una definizione di proprietà a un'istanza di una proprietà.

Nella procedura seguente vengono identificati i passaggi necessari per alleghire una definizione di proprietà.

**Per alleghi una definizione di proprietà**

1.  Identificare ogni proprietà presente in un'istanza del protocollo. Quando si aggiunge una definizione, Network Monitor passa i dati acquisiti al parser. I dati vengono passati in base a un'istanza di protocollo.
2.  Determinare il percorso della proprietà nell'istanza del protocollo.
3.  Alleghi una definizione di proprietà al percorso della proprietà.

Network Monitor implementa una struttura [**PROPERTYINST**](propertyinst.md) quando il parser usa i dati della proprietà così come esistono nell'acquisizione. Network Monitor implementa una struttura [**PROPERTYINSTEX**](propertyinstex.md) quando il parser deve modificare i dati della proprietà nell'acquisizione.

 

 



