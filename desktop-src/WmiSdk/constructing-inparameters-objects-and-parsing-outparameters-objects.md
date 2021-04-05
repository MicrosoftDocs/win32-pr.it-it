---
description: In genere, l'accesso diretto è adeguato per chiamare un metodo del provider WMI.
ms.assetid: be9332b5-8094-44a2-8632-af9957ecf36b
ms.tgt_platform: multiple
title: Creazione di oggetti InParameters e analisi di oggetti OutParameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a291d4fd44e69e87572684856bba587685e1f07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967973"
---
# <a name="constructing-inparameters-objects-and-parsing-outparameters-objects"></a>Creazione di oggetti InParameters e analisi di oggetti OutParameters

In genere, l'accesso diretto è adeguato per chiamare un [*metodo del provider*](gloss-p.md)WMI. L'accesso diretto comporta l'esecuzione di un metodo tramite la sintassi *Object. Method* . In alcuni casi, tuttavia, non è possibile usare l'accesso diretto. Inoltre, la chiamata asincrona di un metodo del provider da uno script richiede un tipo di chiamata [**ExecMethodAsync**](swbemobject-execmethodasync-.md) .

> [!Note]  
> Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona. Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).

 

L'ordine dei parametri di input e output del metodo viene definito nello schema Managed Object Format (MOF) per il metodo. WMI non impedisce la modifica dell'ordine dei parametri quando la classe viene ricompilata da [mofcomp](mofcomp.md). Utilizzando un oggetto [**InParameters**](swbemmethod-inparameters.md) , è possibile evitare problemi causati dallo schema modificato perché i parametri di input sono identificati in base al nome. Il parametro corretto può essere visualizzato esaminando il qualificatore **ID** di ogni parametro di input. Il primo parametro ha un valore **ID** pari a 0 (zero).

[**I metodi SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)e [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) forniscono una modalità alternativa per eseguire un metodo del provider nei casi in cui non è possibile eseguire direttamente un metodo. Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).

Per altre informazioni sui parametri, vedere [creazione di oggetti InParameters](constructing-inparameters-objects.md) e [analisi di oggetti OutParameters](parsing-outparameters-objects.md).

 

 



