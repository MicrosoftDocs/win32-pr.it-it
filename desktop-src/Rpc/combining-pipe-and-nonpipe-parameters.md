---
title: Combinazione di parametri pipe e nonpipe
description: Combinazione di parametri pipe e nonpipe in RPC (Remote Procedure Call).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76bc2f334325c87cbf8c4a09898cf0fe54153cd84f6f2809995e66cc08e843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022671"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a>Combinazione di parametri pipe e nonpipe

Quando si combinano tipi di pipe e altri tipi in una chiamata di procedura remota, i dati vengono trasmessi in base alla direzione del parametro :

-   Nella direzione **\[ , \]** i dati per tutti gli argomenti non di tipo pipe vengono trasmessi per primi, seguiti dai dati della pipe.
-   Nella direzione **\[ di uscita, \]** il server invia prima i dati della pipe. Al termine della routine di gestione, il server trasmette i dati non dipe.
-   Quando sono presenti argomenti della pipe **\[ in,out \]** combinati con argomenti non pipe **\[ in,out, \]** prima i dati di input vengono trasmessi nella loro interezza, come descritto in precedenza. I dati di output vengono quindi trasmessi come descritto in precedenza.

La restrizione seguente si applica a questa implementazione (MIDL 3.0) di pipe: quando si combinano tipi pipe e altri tipi in una singola chiamata di procedura remota, i parametri nonpipe devono avere una dimensione ben definita per consentire al compilatore MIDL di calcolare le dimensioni del buffer necessarie. Ad esempio, non è possibile combinare i parametri della pipe con un puntatore univoco o una struttura conforme, poiché non è possibile determinarne le dimensioni \[ [](/windows/desktop/Midl/unique) \] in fase di compilazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[inviare tramite pipe](/windows/desktop/Midl/pipe)
</dt> <dt>

[/Oi](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 