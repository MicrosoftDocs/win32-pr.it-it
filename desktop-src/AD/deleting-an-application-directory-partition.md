---
title: Eliminazione di una partizione di directory applicativa
description: Una partizione di directory applicativa viene eliminata eliminando l'oggetto crossRef che rappresenta la partizione di directory applicativa.
ms.assetid: bc7986c1-5a11-440c-924e-dc525b5cb78f
ms.tgt_platform: multiple
keywords:
- Eliminazione di un annuncio della partizione di directory applicativa
- AD, eliminazione delle partizioni di directory applicative
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd52ef99323ee7463a4733210314e02d911f0d66
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724575"
---
# <a name="deleting-an-application-directory-partition"></a>Eliminazione di una partizione di directory applicativa

Una partizione di directory applicativa viene eliminata eliminando l'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) che rappresenta la partizione di directory applicativa. Quando l'eliminazione dell'oggetto **crossRef** viene replicata in un controller di dominio che dispone di una replica della partizione di directory applicativa, il KCC eliminerà la replica locale della partizione di directory applicativa. Questa operazione provoca l'eliminazione di tutte le repliche della partizione di directory applicativa.

Quando l'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) viene eliminato, il server di Active Directory eliminerà l'oggetto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) creato al momento della creazione della partizione di directory applicativa, oltre a eliminare tutti gli oggetti nella partizione di directory applicativa. Nessuno degli oggetti nella partizione di directory applicativa viene contrassegnato per la rimozione definitiva al momento dell'eliminazione.

Quando viene eliminata una partizione di directory applicativa, è molto difficile ripristinarla. Per ripristinare una partizione di directory applicativa, è necessario ripristinare un backup con una replica della partizione di directory applicativa, trovare l'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) che rappresenta la partizione di directory applicativa e ripristinare l'oggetto **crossRef** in modo autorevole.

**Per eliminare una partizione di directory applicativa e le relative repliche, seguire questa procedura**

1.  Cercare nel contenitore partizioni un oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) con un valore di attributo [**NCName**](/windows/desktop/ADSchema/a-ncname) uguale al nome distinto della partizione di directory applicativa.
2.  Eliminare l'oggetto [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

Per ulteriori informazioni, vedere il [codice di esempio per l'eliminazione di una partizione di directory applicativa](example-code-for-deleting-an-application-directory-partition.md).

 

 