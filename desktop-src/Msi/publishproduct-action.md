---
description: L'azione PublishProduct gestisce l'annuncio delle informazioni sul prodotto con il sistema. Questa azione pubblica il prodotto se il prodotto è in modalità di annuncio o se è in corso l'installazione o la reinstallazione di una funzionalità.
ms.assetid: aba1baf2-d282-4f76-87aa-67188b779535
title: Azione PublishProduct
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9edf95ccb736bb4a4388f36d87bfbfbe299573e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311726"
---
# <a name="publishproduct-action"></a>Azione PublishProduct

L'azione PublishProduct gestisce l'annuncio delle informazioni sul prodotto con il sistema. Questa azione pubblica il prodotto se il prodotto è in modalità di annuncio o se è in corso l'installazione o la reinstallazione di una funzionalità.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione PublishProduct deve essere successiva all'azione [PublishFeatures](publishfeatures-action.md) .

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione        |
|-------|-----------------------------------|
| \[1\] | Identificatore del prodotto pubblicizzato. |



 

 

 



