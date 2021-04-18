---
description: Le API Windows Image Acquisition (WIA) restituiscono lo stato di completamento in un valore restituito HRESULT.
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: Informazioni sull'errore WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31bcbba9e42d8b7a95b892eb8bba14a56ad758e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307315"
---
# <a name="wia-error-information"></a>Informazioni sull'errore WIA

Le API Windows Image Acquisition (WIA) restituiscono lo stato di completamento in un valore restituito HRESULT. Le applicazioni controllano questi valori restituiti rispetto alla \_ costante WIA della struttura per determinare se l'errore richiede l'intervento dell'utente da cancellare, ad esempio un percorso di carta inceppata, e segnalarli all'utente. Inoltre, tutti gli errori a livello di driver vengono registrati in dettaglio nel registro eventi, usando le stringhe di errore fornite dal dispositivo minidriver. Per un elenco di codici di errore specifici di WIA, vedere [codici di errore](-wia-error-codes.md).

 

 



