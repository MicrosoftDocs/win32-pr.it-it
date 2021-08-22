---
description: A differenza dell'eliminazione di un'istanza dinamica, l'eliminazione di una classe è una procedura semplice.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Eliminazione di una classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aad3e44292aa1ca6b534151a82f36df50802e04db788d8cfb8aaeb477c23164f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412091"
---
# <a name="deleting-a-class"></a>Eliminazione di una classe

A differenza dell'eliminazione di un'istanza dinamica, l'eliminazione di una classe è una procedura semplice. Tuttavia, come illustrato in precedenza, le classi di base o derivate vengono eliminate raramente. Un'istanza viene invece eliminata più comunemente. [L'API scripting per WMI](scripting-api-for-wmi.md) usa gli stessi metodi per eliminare un oggetto classe o un'istanza. Per altre informazioni, vedere [Eliminazione di un'istanza](deleting-an-instance.md)di . Per informazioni sulla rimozione di classi e istanze dal repository WMI, vedere il comando del preprocessore [**pragma deleteclass.**](pragma-deleteclass.md)

[L'API COM per WMI](com-api-for-wmi.md) dispone di metodi diversi per l'eliminazione di un'istanza e l'eliminazione di un oggetto.

La procedura seguente descrive come eliminare una classe base o una classe derivata.

**Per eliminare una classe di base o una classe derivata**

-   Chiamare il [**metodo IWbemServices::D eleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) o [**IWbemServices::D eleteClassAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync)

    Come suggerisce il nome, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) elimina un'istanza in modo asincrono mentre [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) elimina un'istanza in modo sincrono. Per usare **DeleteClassAsync,** è necessario implementare anche un [**oggetto IWbemObjectSink.**](iwbemobjectsink.md)

> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile usare la comunicazione semisincrona anziché asincrona. Per altre informazioni, vedere [Chiamata di un metodo](calling-a-method.md).

 

 

 



