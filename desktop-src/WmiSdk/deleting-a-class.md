---
description: A differenza dell'eliminazione di un'istanza dinamica, l'eliminazione di una classe è una procedura semplice.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Eliminazione di una classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3d9ce149b5eff0f5202cb25c5f7d16fdf44291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315734"
---
# <a name="deleting-a-class"></a>Eliminazione di una classe

A differenza dell'eliminazione di un'istanza dinamica, l'eliminazione di una classe è una procedura semplice. Tuttavia, come illustrato in precedenza, le classi base o derivate vengono eliminate raramente. Un'istanza viene invece eliminata più di frequente. L' [API di scripting per WMI](scripting-api-for-wmi.md) utilizza gli stessi metodi per eliminare un oggetto classe o un'istanza di. Per ulteriori informazioni, vedere [eliminazione di un'istanza](deleting-an-instance.md). Per informazioni sulla rimozione di classi e istanze dal repository WMI, vedere il comando per il preprocessore [**pragma deleteclass**](pragma-deleteclass.md) .

Per l' [API com per WMI](com-api-for-wmi.md) sono disponibili metodi diversi per l'eliminazione di un'istanza di e l'eliminazione di un oggetto.

Nella procedura riportata di seguito viene descritto come eliminare una classe base o una classe derivata.

**Per eliminare una classe base o una classe derivata**

-   Chiamare il metodo [**IWbemServices::D eleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) o [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) .

    Come suggerisce il nome, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) Elimina un'istanza in modo asincrono mentre [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) Elimina un'istanza in modo sincrono. Per usare **DeleteClassAsync**, è necessario implementare anche un oggetto [**IWbemObjectSink**](iwbemobjectsink.md) .

> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

 

 

 



