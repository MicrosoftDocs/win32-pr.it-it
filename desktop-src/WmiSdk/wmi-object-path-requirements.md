---
description: WMI utilizza i percorsi degli oggetti nelle proprietà di riferimento delle classi di associazione per identificare gli oggetti correlati, nonché utilizzare i percorsi degli oggetti nei parametri di input o output per diversi metodi.
ms.assetid: 07fee6f8-810e-4dec-8f0f-787756ee3beb
ms.tgt_platform: multiple
title: Requisiti del percorso dell'oggetto WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2b46195eae3e8351c9c611a34c28cc9d5dd58d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401683"
---
# <a name="wmi-object-path-requirements"></a>Requisiti del percorso dell'oggetto WMI

WMI utilizza i percorsi degli oggetti nelle proprietà di riferimento delle classi di associazione per identificare gli oggetti correlati, nonché utilizzare i percorsi degli oggetti nei parametri di input o output per diversi metodi. Poiché i percorsi degli oggetti vengono considerati come stringhe ai fini della ricerca e del confronto, il valore di un percorso dell'oggetto quando viene utilizzato come proprietà di riferimento è sempre la stringa stessa e non l'oggetto dereferenziato. I confronti tra stringhe che riguardano i percorsi degli oggetti non fanno distinzione tra maiuscole e minuscole.

Un percorso dell'oggetto può utilizzare la sintassi seguente:

-   Stringhe contenute tra virgolette singole.
-   Barra come separatore.
-   Barre rovesciate come separatori.
-   Costanti esadecimali per numeri interi.
-   Costanti booleane per le classi con chiavi che accettano valori booleani.
-   Notazione URL per rappresentare caratteri non stampabili, ad esempio %20 per uno spazio vuoto.

Inoltre, una stringa del percorso di un oggetto deve rispettare le restrizioni seguenti:

-   Un server locale utilizzato con un percorso di spazio dei nomi parziale. Pertanto, specificando la radice e lo spazio dei nomi predefinito sono implicati la radice e lo spazio dei nomi predefinito nel server locale.
-   Nessuno spazio vuoto all'interno di un elemento o tra gli elementi.
-   Le virgolette incorporate nei percorsi degli oggetti sono consentite, ma devono delimitare le virgolette con caratteri di escape, come in un'applicazione C o C++.
-   Solo i valori decimali vengono riconosciuti come parti numeriche di chiavi.

 

 



