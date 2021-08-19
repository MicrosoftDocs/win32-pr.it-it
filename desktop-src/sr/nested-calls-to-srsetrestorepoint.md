---
title: Chiamate annidate a SRSetRestorePoint
description: In questo argomento viene descritto il supporto per le chiamate annidate a SRSetRestorePoint tramite i tipi di evento BEGIN \_ NESTED SYSTEM CHANGE ed END NESTED SYSTEM \_ \_ \_ \_ \_ CHANGE.
ms.assetid: ee2dea47-f95d-4293-ac33-eff622b84db6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12286a69bdb83cb5fd119280e8996c6612e359bf93b9371b6a088a98bf6fd881
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857636"
---
# <a name="nested-calls-to-srsetrestorepoint"></a>Chiamate annidate a SRSetRestorePoint

In questo argomento viene descritto il supporto per le chiamate annidate a [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) tramite i tipi di evento BEGIN \_ NESTED SYSTEM CHANGE ed END NESTED SYSTEM \_ \_ \_ \_ \_ CHANGE.

Le applicazioni possono chiamare in modo [**sicuro SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) quando si usano questi tipi di evento. La prima chiamata alla funzione crea un punto di ripristino. Le chiamate annidate successive alla funzione non creano punti di ripristino. Si supponga, ad esempio, che un'applicazione esempli le **chiamate seguenti a SRSetRestorePoint:**<dl> Per il punto di ripristino A con dwEventType = BEGIN \_ NESTED \_ SYSTEM \_ CHANGE  
Per il punto di ripristino B con dwEventType = BEGIN \_ NESTED \_ SYSTEM \_ CHANGE  
Per il punto di ripristino B con dwEventType = END \_ NESTED \_ SYSTEM \_ CHANGE  
Per il punto di ripristino A con dwEventType = END \_ NESTED \_ SYSTEM \_ CHANGE  
</dl>

La seconda chiamata non crea un nuovo punto di ripristino perché la chiamata è annidata.

 

 




