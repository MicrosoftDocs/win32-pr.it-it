---
title: Funzioni per informazioni sul router
description: Usare le funzioni seguenti per modificare le intestazioni e i blocchi delle informazioni sul router. Un'intestazione informazioni è costituita da blocchi di informazioni e metadati privati. I blocchi di informazioni sono matrici di strutture di informazioni di diversi tipi.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f694d2dcd140d8af8950fa7a2a4ae5049a679ff8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104043983"
---
# <a name="router-information-functions"></a>Funzioni per informazioni sul router

Usare le funzioni seguenti per modificare le intestazioni e i blocchi delle informazioni sul router. Un'intestazione informazioni è costituita da blocchi di informazioni e metadati privati. I blocchi di informazioni sono matrici di [strutture di informazioni](router-information-structures.md) di diversi [tipi](router-information-enumerations.md).

Le funzioni seguenti modificano le intestazioni delle informazioni:

-   [**MprInfoCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfocreate)
-   [**MprInfoDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfodelete)
-   [**MprInfoDuplicate**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoduplicate)
-   [**MprInfoRemoveAll**](/windows/desktop/api/Mprapi/nf-mprapi-mprinforemoveall)

Le funzioni seguenti modificano i blocchi di informazioni all'interno di un'intestazione di informazioni:

-   [**MprInfoBlockAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockadd)
-   [**MprInfoBlockFind**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockfind)
-   [**MprInfoBlockQuerySize**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockquerysize)
-   [**MprInfoBlockRemove**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockremove)
-   [**MprInfoBlockSet**](/windows/desktop/api/Mprapi/nf-mprapi-mprinfoblockset)

Molte delle [funzioni di amministrazione e configurazione del router](understanding-mprinfo-functions-and-information-headers.md) utilizzano le intestazioni delle informazioni.

 

 




