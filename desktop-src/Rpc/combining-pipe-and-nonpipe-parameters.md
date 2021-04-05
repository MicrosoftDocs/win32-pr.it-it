---
title: Combinazione di parametri pipe e nonpipe
description: Combinazione di parametri pipe e non pipe in RPC (Remote Procedure Call).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0776f995dacb4d477724b0ee1e5c2fa969723199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872814"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a>Combinazione di parametri pipe e nonpipe

Quando si combinano i tipi di pipe e altri tipi in una chiamata di procedura remota, i dati vengono trasmessi in base alla direzione del parametro:

-   Nella direzione, i dati per tutti gli argomenti non pipe vengono trasmessi per primi, seguiti dai dati della pipe. **\[ \]**
-   Nella direzione di **\[ uscita \]** , il server invia prima i dati della pipe. Dopo la restituzione della routine del Manager, il server trasmette i dati non pipe.
-   Quando ci sono **\[ in, gli \] argomenti di pipe in uscita** combinati con **\[ in, out \]** di argomenti non pipe, prima i dati di input vengono trasmessi integralmente, come descritto in precedenza. I dati di output vengono quindi trasmessi come descritto in precedenza.

La restrizione seguente si applica a questa implementazione (MIDL 3,0) delle pipe: quando si combinano i tipi di pipe e altri tipi in una singola chiamata di procedura remota, i parametri non pipe devono avere una dimensione ben definita per consentire al compilatore MIDL di calcolare la dimensione del buffer necessaria. Non è ad esempio possibile combinare parametri pipe con un \[ [](/windows/desktop/Midl/unique) \] puntatore univoco o una struttura conforme, poiché non è possibile determinare le dimensioni in fase di compilazione.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[inviare tramite pipe](/windows/desktop/Midl/pipe)
</dt> <dt>

[/Oi](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 