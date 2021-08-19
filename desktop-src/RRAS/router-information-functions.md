---
title: Funzioni relative alle informazioni sul router
description: Usare le funzioni seguenti per modificare le intestazioni e i blocchi delle informazioni del router. Un'intestazione di informazioni è costituita da metadati privati e blocchi di informazioni. I blocchi di informazioni sono matrici di strutture di informazioni di vari tipi.
ms.assetid: e88720aa-080b-4d87-a442-1b436c256ca6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029b36ef862f11c58492fd8ec9c7c6f292797c2e35e75592f385e18d6d0e1a25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788016"
---
# <a name="router-information-functions"></a>Funzioni relative alle informazioni sul router

Usare le funzioni seguenti per modificare le intestazioni e i blocchi delle informazioni del router. Un'intestazione di informazioni è costituita da metadati privati e blocchi di informazioni. I blocchi di informazioni sono matrici [di strutture di informazioni](router-information-structures.md) di vari [tipi.](router-information-enumerations.md)

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

Molte delle funzioni [di configurazione e amministrazione del router usano](understanding-mprinfo-functions-and-information-headers.md) intestazioni di informazioni.

 

 




