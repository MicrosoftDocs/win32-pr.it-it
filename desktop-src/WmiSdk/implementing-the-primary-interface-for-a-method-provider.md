---
description: Un provider di metodi deve implementare IWbemServices come interfaccia primaria. Tuttavia, un provider di metodi puri richiede solo l'implementazione del metodo IWbemServices::ExecMethodAsync.
ms.assetid: 39466513-48f3-4bf6-a3ab-e9d2c387480c
ms.tgt_platform: multiple
title: Implementazione dell'interfaccia primaria per un provider di metodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fcc698155ad0a9e786636045654b08d1cd2b7dfabd946b2d3ee9e8192485
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119244231"
---
# <a name="implementing-the-primary-interface-for-a-method-provider"></a>Implementazione dell'interfaccia primaria per un provider di metodi

Un provider di metodi deve [**implementare IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) come interfaccia primaria. Tuttavia, un provider di metodi puri richiede solo l'implementazione del [**metodo IWbemServices::ExecMethodAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)

Poiché altri provider usano [**IWbemServices,**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices)l'interfaccia contiene molti metodi irrilevanti per un provider di metodi puri. Il provider di metodi puri deve fornire un'implementazione stub che restituisce WBEM E PROVIDER NOT CAPABLE per tutti gli altri metodi \_ \_ \_ \_ **IWbemServices** oltre a [**ExecMethodAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) Tuttavia, molti provider di metodi fungono anche da provider di istanze o di classi. I provider di metodi di combinazione e di istanza devono supportare più metodi **IWbemServices.**

 

 



