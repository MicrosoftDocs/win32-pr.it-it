---
description: Quando si seleziona una scheda di interfaccia di rete (NIC) registrata elencata in un computer locale, è possibile usare un BLOB di filtro per ignorare le schede di interfaccia di rete a cui non si è interessati.
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: Specifica di un BLOB di filtro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486a5dfe318da50a921560c92b82a3a3bf05a9434a4ac609b7f135afd7bf5a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555351"
---
# <a name="specifying-a-filter-blob"></a>Specifica di un BLOB di filtro

Quando si seleziona una scheda di interfaccia di rete (NIC) registrata elencata in un computer locale, è possibile usare un [*BLOB*](f.md) di filtro per ignorare le schede di interfaccia di rete a cui non si è interessati. Ad esempio, è possibile limitare la ricerca di un tipo specifico di scheda (ad esempio ETHERNET) o di un indirizzo MAC specifico.

Durante la ricerca di una scheda di interfaccia di rete, ogni voce nel BLOB del filtro deve corrispondere a una voce equivalente nel BLOB NPP che rappresenta la scheda di interfaccia di rete. I BLOB di filtro possono anche essere [*OGGETTI BLOB speciali.*](s.md)

Quando viene [**chiamata la funzione GetNPPBlobFromUI,**](getnppblobfromui.md) il BLOB del filtro limita le schede di interfaccia di rete visualizzate nella finestra di **dialogo** Seleziona una rete. Quando viene [**chiamata la funzione GetNPPBlobTable,**](getnppblobtable.md) il BLOB di filtro limita le schede di interfaccia di rete restituite nella tabella BLOB.

Per usare il filtro, è necessario creare un BLOB di filtro, impostare i valori delle proprietà da filtrare (incluse eventuali voci BLOB speciali) e quindi specificare il filtro BLOB e una chiamata alla funzione [**GetNPPBlobTable**](getnppblobtable.md) o [**GetNPPBlobFromUI.**](getnppblobfromui.md)



| Per informazioni su                                 | Vedere                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| Come selezionare una scheda di interfaccia di rete registrata in un computer locale | [Selezione di una scheda di interfaccia di rete registrata](selecting-a-registered-nic.md)                                         |
| Recupero di una tabella BLOB NPP                       | [Selezione di una scheda di interfaccia di rete da una tabella BLOB NPP restituita](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



