---
description: Gestione delle espulsioni dei dischi
ms.assetid: c43dd795-749b-4ca7-8510-71d62e0076b3
title: Gestione delle espulsioni dei dischi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8964c8fd18395e932e1536e885bae1814d5952fd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875929"
---
# <a name="handling-disc-ejections"></a>Gestione delle espulsioni dei dischi

Quando l'utente espelle un DVD dall'unità, il navigatore DVD invia all'applicazione un messaggio di \_ rilascio del disco DVD di EC \_ \_ . L'applicazione può ignorare questo messaggio e consentire al navigatore DVD di gestire lo stato del grafo. Un'applicazione può inoltre gestire il \_ \_ metodo di rimozione del disco DVD EC \_ per implementare un comportamento personalizzato quando viene espulso un disco. Se si gestisce il messaggio, è necessario impostare il \_ flag DVD ResetOnStop su **true** con il metodo [**SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) , quindi chiamare [**IMediaControl:: Stop**](/windows/desktop/api/Control/nf-control-imediacontrol-stop) prima di chiudere l'applicazione o riprodurre un altro disco.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



