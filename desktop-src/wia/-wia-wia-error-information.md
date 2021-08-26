---
description: Le API Windows di acquisizione di immagini (WIA) restituiscono il relativo stato di completamento in un valore restituito HRESULT.
ms.assetid: 4f3b4292-7aad-4a0a-9cd7-ef8438e57ab3
title: Informazioni sugli errori WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce8181cb4d3f578fa9322ecaa81d588423bb403be3b38a76c2dbac17a19fe010
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056961"
---
# <a name="wia-error-information"></a>Informazioni sugli errori WIA

Le API Windows di acquisizione di immagini (WIA) restituiscono il relativo stato di completamento in un valore restituito HRESULT. Le applicazioni verificano questi valori restituiti rispetto alla costante FACILITY WIA per determinare se l'errore richiede l'intervento dell'utente per cancellare, ad esempio un percorso carta inceppato, e \_ segnalarli all'utente. Inoltre, tutti gli errori a livello di driver vengono registrati in dettaglio nel registro eventi, usando le stringhe di errore fornite dal minidriver del dispositivo. Per un elenco dei codici di errore specifici di WIA, vedere [Codici di errore](-wia-error-codes.md).

 

 



