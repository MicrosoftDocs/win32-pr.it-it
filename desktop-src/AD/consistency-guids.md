---
title: GUID di coerenza
description: I GUID di coerenza sono una strategia di rilevamento che consente a un'applicazione di rilevare gli aggiornamenti parziali.
ms.assetid: 3418667f-4d5a-4a4b-b0f5-7744a21608f7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bcfb25d0f04a459217811a2ff0393fac47e3206
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044008"
---
# <a name="consistency-guids"></a>GUID di coerenza

I GUID di coerenza sono una strategia di rilevamento che consente a un'applicazione di rilevare gli aggiornamenti parziali. Un GUID di coerenza (identificatore univoco globale) viene applicato a ogni oggetto in un set correlato. Nell'implementazione, un'applicazione di origine genera un nuovo GUID e lo applica a ogni oggetto aggiornato nel set di oggetti correlati. Applica quindi il nuovo GUID al resto degli oggetti nel set e termina applicando il nuovo GUID all'oggetto "Master". In genere, l'oggetto "Master" sarà un contenitore padre degli altri oggetti nel set.

Alcune considerazioni importanti:

-   I GUID di coerenza combinati con conteggi di oggetti o checksum sono più efficaci dei soli GUID di coerenza, perché l'applicazione che legge gli oggetti potrebbe non essere in grado di stabilire quanti oggetti con il GUID devono essere presenti.
-   Le applicazioni devono generare i propri GUID (un'API Microsoft Win32, UuidCreate, fornisce questa funzione) e non usare i GUID generati dal sistema presenti nell'attributo **objectGUID** di un oggetto. Questo perché un GUID di coerenza deve cambiare ogni volta che viene aggiornato il set di oggetti. I GUID di identità degli oggetti trovati in **objectGUID** non cambiano mai dopo la creazione dell'oggetto.
-   I GUID di coerenza presuppongono che nessun oggetto venga condiviso tra set, quindi ogni set può avere un GUID di coerenza univoco.

 

 




