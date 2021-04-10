---
title: attributo String (RPC)
description: L'attributo \ string \ e la chiamata RPC (Remote Procedure Call).
ms.assetid: 794e03f2-b1e9-42dc-8536-9ced5c0e3dad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e413c0b3b8f5a379dc3448f07aed4a5a7a6aba07
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963359"
---
# <a name="string-attribute-rpc"></a>attributo String (RPC)

L' \[ [](/windows/desktop/Midl/string) \] attributo stringa indica che il parametro è un puntatore a una matrice di tipo [char](/windows/desktop/Midl/char-idl), [byte](/windows/desktop/Midl/byte)o **w \_ char**. Come con una matrice conforme, la dimensione di un parametro di **\[ stringa \]** viene determinata in fase di esecuzione. A differenza di una matrice conforme, lo sviluppatore non deve fornire la lunghezza associata alla matrice: l'attributo **\[ \] stringa** indica allo stub di determinare la dimensione della matrice chiamando **strlen**. Non è possibile utilizzare un attributo di **\[ \] stringa** contemporaneamente alla lunghezza di \[ [ \_](/windows/desktop/Midl/length-is) \] o dell' \[ [ultimo \_](/windows/desktop/Midl/last-is) attributo \] .

In la combinazione di attributi **\[ stringa \]** indica allo stub di passare la stringa solo dal client al server. La quantità di memoria allocata sul server corrisponde alla dimensione della stringa trasmessa più una.

Gli \[ attributi [out](/windows/desktop/Midl/out-idl), **String** \] indirizzano lo stub per passare la stringa solo dal server al client. La progettazione chiamata per valore del linguaggio C insiste sul fatto che tutti i parametri **\[ out \]** devono essere puntatori.

Il parametro **\[ out \]** deve essere un puntatore e, per impostazione predefinita, tutti i parametri del puntatore sono puntatori di riferimento. Il puntatore di riferimento non cambia durante la chiamata, ma punta alla stessa memoria di prima della chiamata. Per i puntatori di stringa, il vincolo aggiuntivo del puntatore di riferimento significa che il client deve allocare memoria valida sufficiente prima di effettuare la chiamata di procedura remota. Gli stub trasmettono la stringa che l' **\[ out, \]** gli attributi di stringa indicano nella memoria già allocata sul lato client.

Negli argomenti seguenti vengono descritti i prototipi dei parametri della procedura remota per le stringhe:

-   [\[in, out, \] prototipo di stringa](-in-out-string-prototype.md)
-   [\[in, String \] e \[ out, \] prototipo di stringa](-in-string-and-out-string-prototype.md)

 

 