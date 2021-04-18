---
description: Quando si seleziona una scheda di interfaccia di rete (NIC) registrata elencata in un computer locale, è possibile utilizzare un BLOB di filtro per ignorare le NIC a cui non si è interessati.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Specifica di un BLOB di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8754b8f7ea5388b730fd2dfb65e26e24a906d648
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307706"
---
# <a name="specifying-a-filter-blob"></a>Specifica di un BLOB di filtro

Quando si seleziona una scheda di interfaccia di rete (NIC) registrata elencata in un computer locale, è possibile utilizzare un [*BLOB di filtro*](f.md) per ignorare le NIC a cui non si è interessati. Ad esempio, è possibile limitare la ricerca di un tipo specifico di scheda (ad esempio ETHERNET) o di un indirizzo MAC specifico.

Durante la ricerca di una scheda di interfaccia di rete, ogni voce nel BLOB di filtro deve corrispondere a una voce equivalente nel BLOB di NPP che rappresenta la scheda di interfaccia di rete. I BLOB di filtro possono anche essere [*BLOB speciali*](s.md).

Quando viene chiamata la funzione [**GetNPPBlobFromUI**](getnppblobfromui.md) , il BLOB di filtro limita le schede di rete visualizzate nella finestra di dialogo **Seleziona una rete** . Quando viene chiamata la funzione [**GetNPPBlobTable**](getnppblobtable.md) , il BLOB di filtro limita le schede di rete restituite nella tabella BLOB.

Per usare il filtro, è necessario creare un BLOB di filtro, impostare i valori delle proprietà su cui applicare il filtro (incluse eventuali voci di BLOB speciali), quindi specificare il filtro BLOB e una chiamata alla funzione [**GetNPPBlobTable**](getnppblobtable.md) o [**GetNPPBlobFromUI**](getnppblobfromui.md) .



| Per informazioni su                                 | Vedere                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Come selezionare una scheda di interfaccia di rete registrata in un computer locale | [Selezione di una scheda di interfaccia di rete registrata](selecting-a-registered-nic.md)                                         |
| Recupero di una tabella BLOB di NPP                       | [Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP restituita](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



